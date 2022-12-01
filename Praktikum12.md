# 12. praktikumis tehtud töö.

Autor: Walther Kraam

|Küsimus, praktikumi juhendis siniselt ja nimetatud, et tuleb vastata|Vastus|
|---|---|
|1. Nimetage 3 kõige suuremat pilveteenuste pakkujat|<ul><li>1. Microsoft <li>2. Amazon <li>3. Salesforce</ul>|
|2. Nimetage 5 eelist, mis on pilveteenustel võrreldes enda teenuste füüsilistel masinatel majutamisega?|<ul><li>1.andmed on pilves, ehk need on tavaliselt backupitud ja manageeritud <li>2.saad ligi igal pool, kus on internet <li>3. jõudlus on skaleeritav<li>4. pole masinat, mis võtaks ruumi<li>5. turvalisus</ul>|
|3. Nimetage 3 situatsiooni, kus pole pilveteenuse kasutamine mõistlik?|<ul><li>1. Kui ei soovi andmeid veebiga ühendada <li>2. Kui on vaja lokaalselt midagi ajada <li>3. Kui veebiühendus pole pilveteenusega piisavalt stabiilne või odav.</ul>|
|4. Mis on vahet IAAS ja SAAS ja PAAS tenustel?|<ul><li>IAAS: võimaldab kasutajal kasutada andmemahtu, arvutusvõimekust, ning ka "networking resources"<li>PAAS: IAAS+OP. süsteemid ning arenduse tarkvarad, databaasid, analüütika<li>SAAS: PAAS+lubatud on ka veebiaplikatsioonide hostimine nagu GMail ja OneDrive</ul>|
|5. Kas teate ka mõnda Eesti ettevõtet, kes pakub pilves IAAS hostimise teenust?|Riigipilve IaaS, UT pilv|
|6. Mis on Azure Resource Group|loogiline grupp, kus saab rakendada azure resursse.|
|7. Mis on Azure Subscription|loogiline element, mis määrab ära, et milline kasutaja kui palju millist resurssi millises grupis kasutada saab, et makseid all hoida.|
|8. Mis on Azure Resource|virtuaalmasinad, databaasid, andmed|
|9. Tehke VM loomise vaatest screenshot Näidis 1|![9 2](https://user-images.githubusercontent.com/75208899/205152814-7f4fa905-e0b7-40b1-8d12-921bb632dcce.png)|
|10. Tehke kohast, kus on näidatud, et teil on Auto Shutdown enablitud kuvatõmmis|![10 2](https://user-images.githubusercontent.com/75208899/205152845-851cc13b-3458-4e35-8bd0-ba56e9b8ca03.png)|
|11. Tehke enda virtuaalmasinas Settings->System->About vaatest kuvatõmmis|![11 1](https://user-images.githubusercontent.com/75208899/205151450-f0397c41-6e9a-4af6-acc2-c01ea97c7ae1.png)|
|12. Pange kirja 3 kasutegurit WSLi juures|<ul><li>1. Managing Servers and Devices <li>2. Remote Scripting <li>3. Working with Windows files</ul>|
|13. Tehke kuvatõmmis sellest, kui olete listinud WSL-is enda kodukusta sisu|![13 1](https://user-images.githubusercontent.com/75208899/205155931-2feddd84-05c8-48c5-8ea2-29c80f641688.png)|
|14. Tehke valmis WSLi skript, mis leiab üles minu talletatud paroolid. PS! need on talletatud ainult md failidesse.|skript on allpool tabelit!|

### Ülesanne 14. skript

    #!/bin/bash
    katalog=$(ls)
    for el in $katalog
    do
            if [ ${el##*.} = "md" ]
            then
                    if [ $(wc -c $el | cut -c1) -gt 0 ]
                    then
                            echo "$(cat $el)"
                    fi
            fi
    done

Täiendatud: 1/12/2022
