# 5. praktikumis tehtud töö.

Autor: Walther Kraam

|Küsimus, praktikumi juhendis siniselt ja nimetatud, et tuleb vastata|Vastus|
|---|---|
|1. Missuguseid õigusi (r,w,x) on Unixis omanikul (u) minimaalselt vaja (d - directory, f - fail). Grupiõigusi (g) ja ülejäänute others (o) õigusi ei ole siin vaja määrata ainult kausta/faili omaniku (user) õigusi.|<li>RW<li>10<li>10<li>11<li>11|
|2. Miks <code>chmod a=x skriptifail</code> ei ole piisav õigus shelli skriptifaili käivitamiseks? Millist õigust lisaks käivitamisele veel vaja läheb skriptifaili käivitamiseks? Põhjendage lühidalt?|vaja läheb kõiki teisi premissione ka, sest kuidas saab käivitada faili, kui sellele pole ligipääsu|
|3. Miks on igal kasutajal omanimeline grupp?|sest linuxis antakse gruppidele õigusi, mitte kasutajatele|
|4. Milliseid on minimaalsed õigused (rwx), mis on vajalikud teie tavakasutajal (kuulub gruppi majasisene) (mitte <code>root</code> või <code>peeter</code> kasutajal, kausta ja faili omanikud) <code>uusfail.txt</code> sisu kuvamiseks|100<br>piltide lingid:[id](https://github.com/wkraam/OPSysteemid/blob/main/Praktikumite%20failid/Praktikum5/id.png), [ls -la](https://github.com/wkraam/OPSysteemid/blob/main/Praktikumite%20failid/Praktikum5/ls-la.png), [cat](https://github.com/wkraam/OPSysteemid/blob/main/Praktikumite%20failid/Praktikum5/cat.png)|
|5. Tehke screenshot tulemusest, kus oleks näha <code>hinded.txt</code> failiõigused <code>ls -la hinded.txt</code> ja jukuisa käivituskäsk koos väljundiga ning lisage see oma viki lehele.|[pilt](https://github.com/wkraam/OPSysteemid/blob/f4e9647bfe6b1efcaea8b2ce18deaf95dd9aac9b/Praktikumite%20failid/Praktikum5/Screenshot%20from%202022-10-12%2017-03-56.png)|
|6. Kas <code>setuid</code> või <code>setgid</code> kasutamine võib vähendada süsteemi turvalisust? Kui JAH, siis kuidas? kui EI, siis miks ei vähenda?|JAH, kui setuid või setgid on lisatud mingile süsteemiprotsessile, siis kasutajal, kellel ei ole root õigusi on nüüd võimalus käsitleda faili kui root kasutaja|
|7. Kirjutage oma viki lehele kõik kasutajaid, kes saavad sticky bit õigustega yhiskaust kataloogist nüüd peeter kasutaja loodud faile kustutada.|root, peeter, opetaja|
|8. Uurige käsuga <code>ls -la</code> faili hinded.txt õigusi - mida märkate? Seejärel uurige õigusi täpsemalt, kasutades käsku <code>getfacl</code> ning kopeerige see tulemus oma vikilehele.| ls -la käsku käiates on nähe, et hinded.txt failiõiguste taha on tekkinud '+' märk <code># file: hinded.txt <br># owner: opetaja <br># group: opetaja <br>user::rw- <br>group::--- <br>group:direktor:rw- <br>mask::rw- <br>other::--- </code>|
|9. Kes saab chattr +i parameetriga faili sisu modifitseerida (kirjutada)? Milliste käskudega saate kustutada testfail-2 nimelise +i parameetriga faili.|siis kui tal on parameeter i küljes ei saa mitte keegi selle failiga mitte midagi peale hakata, peale selle, et root kasutaja saab selle flagi sealt ära eemaldada js siis on see jälle fail, mida saab kustutada, muuta|

Täiendatud: 12/10/2022
