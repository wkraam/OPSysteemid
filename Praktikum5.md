# 5. praktikumis tehtud töö.

|Küsimus, praktikumi juhendis siniselt ja nimetatud, et tuleb vastata|Vastus|
|---|---|
|Missuguseid õigusi (r,w,x) on Unixis omanikul (u) minimaalselt vaja (d - directory, f - fail). Grupiõigusi (g) ja ülejäänute others (o) õigusi ei ole siin vaja määrata ainult kausta/faili omaniku (user) õigusi.|<li>RW<li>10<li>10<li>11<li>11|
|Miks <code>chmod a=x skriptifail</code> ei ole piisav õigus shelli skriptifaili käivitamiseks? Millist õigust lisaks käivitamisele veel vaja läheb skriptifaili käivitamiseks? Põhjendage lühidalt?|vaja läheb kõiki teisi premissione ka, sest kuidas saab käivitada faili, kui sellele pole ligipääsu|
|Miks on igal kasutajal omanimeline grupp?|sest linuxis antakse gruppidele õigusi, mitte kasutajatele|
|Milliseid on minimaalsed õigused (rwx), mis on vajalikud teie tavakasutajal (kuulub gruppi majasisene) (mitte <code>root</code> või <code>peeter</code> kasutajal, kausta ja faili omanikud) <code>uusfail.txt</code> sisu kuvamiseks|100|
