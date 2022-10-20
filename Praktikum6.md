# 6. Praktikumis tehtud töö

Autor: Walther Kraam

|Küsimus|Vastus|
|---|---|
|1.Käivita <code>gedit</code> käsurealt, nüüd peata programmi töö ajutiselt CTRL+Z klahvikombinatsiooniga, veendu et <code>gediti</code> aken on hangunud, seejärel saada talle <code>SIGCONT</code> signaal ning veendu, et <code>gediti</code> aken toimib jälle. Pane oma vikilehele ekraanitõmmis käskude käivitamisest oma terminaliaknas.|[pilt]()|
|2.Käivita <code>gedit</code> taustal & võtmega, saada sellele <code>SIGHUP</code> signaal ja veendu, et aken sulgus. Seejärel käivita <code>gedit nohup</code> käsuga, saada sellele uuesti <code>SIGHUP</code> signaal ning veendu, et <code>gedit</code> jääb käima. Nüüd sisesta käsk millega saad nohup käivitatud gedit protsessi sulgeda. Pane oma vikilehele ekraanitõmmis käskude käivitamisest oma terminaliaknas, sh tõestuseks protsessi kadumise või allesjäämise kohta ps käsu väljund.|[pilt]()|
|3.Koosta ja lisa wikisse käsujada, mis kuvab (modifitseerib) <code>ps -axu &#124; grep daemon</code> väljundi nii et tulemuseks oleksid ainult programminimed koos lisaparameetritega|<code>ps -axu &#124; grep daemon &#124; awk '{print $11, $12}' &#124; tr -d [' ']</code> [pilt]()|
|4.Koosta ja lisa wikisse käsujada <code>(ip a &#124; grep ...&#124; ... &#124; cut ... jne)</code>, mis kuvab ekraanile vastuseks ainult arvuti ip aadressi (enamasti 10.0.2.15) ip a käsu väljundi põhjal.|<code>ip a &#124; grep inet &#124; head -3 &#124; tail +3 &#124; tr -s " " &#124; cut -d" " -f3 &#124; cut -d"/" -f1</code>[pilt]()|

Täiendatud: 20/10/2022
