#  9. Praktikumis tehtud töö

Autor: Walther Kraam

|Küsimus|Vastus|
|---|---|
|1. Võrrelge Administrator ja SYSTEM privileege ning kirjutage vähemalt üks tegevus mille jaoks on vaja SYSTEM õigusi.|SeShutdownPrivilege Administratoris on see DISABLED, SYSTEM privileegidega ENABLED|
|2. Ekraanivaade turvalise kausta seadetest (ainult üks kasutaja saab teha kõike ja Ülemus ainult lugeda)|![image](https://user-images.githubusercontent.com/75208899/200809887-a5cafeda-3b7c-4b4c-ac63-0ac9f64d68d5.png)|
|3. Kirjuta praktikumi aruandesse vähemalt 3 soovitust (muudatust), mida Microsoft soovitab Windowsi turve seadete juures parandada, suurendamaks Windows operatsioonisüsteemi turvalisust.|1. windows soovitab sisse logida Windowsi kasutajaga, et kasutaja turvalisust suurendada ja muid eelistusi kasutada saaks. 2. Windows veel soovitab mainepõhist kaitset sisse lülitada rakenduse- ja brauserisätetes. 3. Soovitab windows lunavaratõrjeks sisse lülitada OneDrive et sinna teeks Windows Bakcuppe|
|4. Sobiv kasutajakonto kontrolli seadistus koos põhjendusega (Süsteem ja turve)|Teavita mind siis kui mingi rakendus proovib arvutis muudatusi teha(ära hämarda tausta) - valisin selle, sest riistvara suhtkoht vana ja läheb kaua aega, et see hämardaks tagatausta, ning ma kasutan endale tuntuid rakendusi, ei pea vajalikuks igat asja confirmida, see muutub liiga tülikaks, samas pole väga kindel, et seda täielikult maha võtta.|
|5. Kirjelda 3 Local Security Policy lisaseadistust turvalisuse tagamiseks, koos põhjendustega.|Enforce password history	5 passwords remembered - et kui on aeg passwordi vahetada, siis ei sisestatak eelmist salasõna ning 5 sest ega peale 5 salasõna vahetust inimene eriti ei mäleta vana salasõna ja on selles harjumuses, et iga kord panna uus salasõna <br> Minimum password length	8 characters - et salasõna oleks turvaline, kui lihtsalt tühik<br> Interactive logon: Machine inactivity limit	900 seconds - peale 900 sekundit või 15 minutit windows forceb logoffi|
|6. Minimaalselt 2 ekraanivaadet testimise käigus esinenud keeluteavitustest, koos selgitusega mida ning millise kasutajaga tehti.||
|7. Ekraanivaade Event Vieweri aknast, kus näha ebaõnnestunud sisselogimiskatsete logikirje||
|8. Tehke ekraanivaade DisplayLastLogonInfo registrivõtmest koos väärtusega 1.||

Täiendatud: 09/11/2022
