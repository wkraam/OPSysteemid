# 7. Praktikumis tehtud töö

Autor: Walther Kraam

|Küsimus|Vastus|
|---|---|
|1. Miks andmekandjad vajavad lähtestamist? (sisukas vastus võiks omada põhjendust)|Et OP süsteem saaks oma kasutatud partitsiooni tabeli panna kettale, ning olla kindel, et ketas on tühi kirjutades kõik bitid 0'dega üle - tehes formaat kiirformaadi asemel. Kiirformaat ütleb lihtsalt operatsioonisüsteemile, et ketas on tühi, kuigi seal veel võib andmeid peal olla.|
|2. Millised on GPT kasutamise eelised ja puudused võrreldes MBR'iga? (välja tuua vähemalt 3 eelist)|Erinevused: MBRil on võimalus ainult neljale partitsioonile, GPT'l on lõppmatu arv. MBRil on suurim kettasuurus 2TB kuid GPTl on 9400000000 TB max. MBRil on võimalus kasutada 32-/64-bit operatsioonisüsteeme, GPT'l ainult 64.bitiseid|
|3. Link hdd.png pildile|https://kodu.ut.ee/~kraam/hdd.png|
|4. Lisage ls -la /mnt/ut/public_html käsu väljundi pilt aruandesse|[pilt]([#link](https://github.com/wkraam/OPSysteemid/blob/19946b74d423edb1e99b2e984e151d83919592b4/Praktikumite%20failid/Screenshot%20from%202022-10-26%2019-07-23.png))|
|5. Mida mõjutasid mount käsu parameetrid "-o ro" ja "-t auto"?|"-o ro"- launch option = read only. "-t auto"- näitab, millist failisüsteemi kasutada ning auto üritab ise aru saada, millist kasutada|
|6. mount käsu väljundist leidke üles, mis väärtusega Ubuntu asendas auto parameetri?|ext4|
|7. Tehke ekraanipilt /etc/fstab faili sisust pärast iseseisva ülesande lahendamist (või muu tõestus/seadistamise juhend, et 4TB ketas haagitaks automaatselt kausta /mnt/bigdata Ubuntu käivitamisel).|[pilt](https://github.com/wkraam/OPSysteemid/blob/19946b74d423edb1e99b2e984e151d83919592b4/Praktikumite%20failid/Screenshot%20from%202022-10-26%2020-24-49.png)|

Täiendatud: 20/10/2022
