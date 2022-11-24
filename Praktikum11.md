# 11. Praktikumis tehtud töö

Autor: Walther Kraam
 
    $SaveFileName = "waltherKraamPraktikum11.txt"

    if (Test-Path ".\waltherKraamPraktikum11.txt"){
        Clear-Content -Path ".\waltherKraamPraktikum11.txt"

    }else{
        New-Item -Path . -Name $SaveFileName
    }

    #ül1 - masina nimi, PS ver. ning win. ver.
    #$PSVersionTable.PSVersion.ToString()
    $winVersion = (Get-CimInstance Win32_OperatingSystem).version
    #$winVersion
    $machineName = hostname
    #$machineName

    @{'PowerShell version' = $PSVersionTable.PSVersion.ToString();'Windows version' = $winVersion ;'Host name' = $machineName} | Out-File $SaveFileName -Append

    #ül2 - võrguandmed: IP, network mask, gateway, DHCP enabled, MAC address
    Get-WmiObject Win32_NetworkAdapterConfiguration -Filter "IPEnabled='True'" | Select-Object IPAddress, IPSubnet, DefaultIPGateway, DHCPEnabled, MACAddress | Sort-Object DHCPEnabled | Format-List * | Out-File $SaveFileName -Append

    #ül3 - CPU info ja RAM ammount
    $RAM = Get-WmiObject Win32_ComputerSystem | Select-Object TotalPhysicalMemory | Format-List
    $RAM | Out-File $SaveFileName -Append

    $prose = Get-WmiObject Win32_Processor | Select-Object Name, NumberOfLogicalProcessors, MaxClockSpeed, AddressWidth | Format-List
    $prose | Out-File $SaveFileName -Append

    #ül4 - GPU properties: gpu name, driver ver., kuupäev?, reolution
    $GPU = Get-WmiObject Win32_VideoController | Select-Object Caption, DriverVersion, DriverDate, VideoModeDescription | Format-List
    $GPU | Out-File $SaveFileName -Append

    #ül5 - HDD info: partition table, mitu GB on arvuti kettad mahutuvuselt, C: ketta vaba ruum
    Get-CimInstance -ClassName Win32_LogicalDisk | Select-Object -Property DeviceID,@{'Name' = 'FreeSpace (GB)'; Expression= { [int]($_.FreeSpace / 1GB) }} | Where-Object {$_.DeviceID -match "C:"} | Format-List | Out-File $SaveFileName -Append
    Get-Disk | Select-Object Model ,PartitionStyle, @{'Name' = 'Space (GB)'; Expression= { [int]($_.Size / 1GB)}} | Format-List | Out-File $SaveFileName -Append

    #ül6 - PCI draiverite inf: kirjeldus, tootja, versioon
    Get-WmiObject –Class Win32_PnpSignedDriver | Where-Object {$_.DeviceID –like „PCI*“} | Select-Object Description, DriverVersion, DriverProviderName | Sort-Object Description -Unique | Format-Table | Out-File $SaveFileName -Append

    #ül7 - Users: name, description, LocalAccount?, Disabled?
    Get-WmiObject Win32_UserAccount | Select-Object Name, Description, LocalAccount, Disabled | Format-List | Out-File $SaveFileName -Append

    #ül8 - käimas olevate protsesside arv 
    Get-Process | Measure-Object -Line | Select-Object @{'Name' = 'Hetkel käimas olevate protsesside arv'; Expression= { [int]($_.Lines)}} | Format-List | Out-File $SaveFileName -Append

    #ül9 - viimased 10 protsessi: pid, name, starttime
    Get-Process | Where-Object {$_.StartTime -ne $null} | Sort-Object -Property StartTime -Descending| Format-Table Id, Name, StartTime -AutoSize | Select-Object -First 10 | Format-Table | Out-File $SaveFileName -Append

    #ül10 - arvuti kuupäev ja kellaaeg
    Get-Date | Out-File $SaveFileName -Append
    
### Kasutatud WMI klassid - nende kirjeldus:
* Win32_OperatingSystem - annab infot arvutisse installitud Windowsi kohta
* Win32_NetworkAdapterConfiguration - selles klassis on atribuudid ja muutujad, mis näitavad kuidas võrguadapterid töötavad
* Win32_ComputerSystem - esindab arvutit, kuhu on Windows installitud
* Win32_Processor - selles klassis on infot protsessori(te) kohta, mis on arvutisse installeeritud
* Win32_VideoController - selles klassis on infot video-protsessori(te) kohta, mis on arvutisse installeeritud
* Win32_LogicalDisk - selles klassis on infot loogiliste diskide kohta 
* Win32_PnpSignedDriver - see klass annab infot installitud draiverite kohta
* Win32_UserAccount - see klass annab infot kasutajate kohta, kes on arvutis
    
Täiendatud: 17/11/2022
