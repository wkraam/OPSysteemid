# Praktikumis 4 tehtud töö
Autor: Walther Kraam

|**Küsimus**|**Linux**|**Windows**|**Linuxis kasutatud käsk**|**Windowsis kasutatud tööriist**|
|---|---|---|---|---|
|1. Mitu protsessi kokku arvutis käib?|197|264| <code>ps -aux &#124; wc -l</code> |Task Manager -> Performance|
|2. Milline on kõige esimesena käivitatud protsess?|/sbin/init splash|Registry|<code>ps -efww</code> -> STIME ning CMD veerg|Process Explorer -> Start time tab|
|3. Milliste kasutajate protsesse arvutis käib?|walther, whoopsie, systemd-t, syslog, rtkit, root, avahi, colord, kernoops, messagebu|NT AUTHORITY\LOCAL SERVICE, NETWORK SERVICE, SYSTEM; WALTHER\wkraa; Window Manager\DWM-1; Front Driver Host\UMFD-0 ja UMFD-1 |htop -> sort by user|Process explorer User Name tab|
|4. Kui kaua on arvuti järjest töötanud(uptime)|1:23|2:00:34:05|<code>uptime</code>|Task Manager -> Performance|
|5. Milline protsess käivitati kõige hiljem (viimasena)?|[kworker/u4:0|Registry|<code>ps aux</code>|Process Explorer -> sort by start time|
|6. Milline on kõige rohkem protsessoriaega võttev protsess?|/usr/bin/gnome-shell|System Idle Process|<code>ps -eo pcpu,pid,user,args &#124; sort -r -k1 &#124; less"</code>|Process Explorer -> sort by CPU Time|
|7. Milline on kõige rohkem virtuaalmälu (aadressiruumi, commit, Virtual Size) võttev protsess?|/usr/bin/gnome-shell|WebStorm.exe|htop|Resource monitor|
|8. Milline on kõige rohkem füüsilist mälu (working set) võttev protsess?|/usr/bin/gnome-shell|Memory Compression|htop|Resource monitor|
|9. Kui palju füüsilisest mälust (Physical Memory) on vaba?|3.4 GiB|1.2 GB|free -h|Task Manager|
|10. Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt?|70%, 21 GB|14.1%, 61.2 GB|<code>df -h</code>|WinDirStat|
|11. Milline on kõige suurem kõvakettal olev fail ja kõige suurem kaust?|Suurim kaust: /usr, Suurim fail: /var/lib/snapd/seed/snaps/gnome-3-34-1804_36.snap|Suurim kaust: Users, Suurim fail: Üks .iso fail|<code>sudo du -aBM / 2>/dev/null &#124; sort -n -r &#124; head -n 50</code>|WinDirStat|
|12. Võrrelge terminali käskude: <code>sha1sum /dev/zero &#124; sha1sum /dev/zero</code> ja <code>sha1sum /dev/urandom &#124; sha1sum /dev/urandom</code> protsessori nõudlust.  Uurige millisele CPU alamtegevusele us, sy, id, wa, st jne kulub enim protsessori aega ja mitu protsenti kulub kummagi käsu korral? (Ainult Linuxis)|siis kui jooksutada ette antud koode, siis enamus protsessiaega läheb "sha1sum" jookutamiseks|-|<code>top</code>|-|
|13. Milline protsess kõige rohkem salvestusseadmele kirjutab, kõige rohkem salvestusseadmelt loeb? Millisesse faili antud protsess kõige rohkem kirjutab, millisest failist kõige rohkem loeb? (Ainult Windowsis)|-|Kõige rohkem kirjutab System ning loeb RuntimeBroker.exe|-|Resource monitor|
|14. Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga? (Ainult Windowsis)|-|1. kohalik IP-aadress: 172.19.153.115 <br>2. kohalik port: 60303<br>3. ühenduse teise poole IP-aadress: 35.186.224.25<br>4. teise poole port: 443<br>5. latents: 298 ms<br>6. võrguliikluse kogumaht: 5268 B/sec|-|Resource monitor|
|15. Sõber kurdab, et tema arvuti on oluliselt aeglasem kui varasemalt. Millise programmiga ja millise parameetrite abil saate tuvastada milline protsess või teenus muudab arvuti aeglaseks?|Alustaks Task Managerist ja vaataks sealt, mis kui palju resursi kasutab, kui see vastust ei anna, siis kasutaks Resource monitori, et täpsemat ideed saada.|top commandiga saad jälgida CPU ja mälu kasutust, ning FREE käsuga näeb, kas talletusruumi on üldse olemas ja kui palju.|-|-|


* [Ül. 12 ja 14 ekraanitõmmised](https://github.com/wkraam/OPSysteemid/blob/main/Praktikumite%20failid/Praktikum4).

Muudetud 04.10.2022
