#  10. Praktikumis tehtud töö

Autor: Walther Kraam

## Kolmas harjutus
### Kood
    #!/bin/sh
    echo "Sisesta nimi: "
    read nimi
    echo "Sisesta eriala: "
    read eriala
    echo "Sisesta matrikli Nr: "
    read matrikkel
    echo '-------------SISESTATI---------------'
    echo "Nimi: $nimi"
    echo "Eriala: $eriala"
    echo "Matrikkel: $matrikkel"</ul>
### Pilt käsure väljundist
![10 3 1](https://user-images.githubusercontent.com/75208899/202529234-cd365d55-f78a-4d27-9e51-c6ae5ecff7c3.png)

## Neljas harjutus
### Kood
    #!/bin/bash
    echo "sisesta otsitav laiend nt txt: "
    read otsitav
    echo "sisesta asendus laiend nt csv: "
    read asendatav
    echo "muudetud failid: "
    katalog=$(ls)
    for el in $katalog
    do
        if [ ${el##*.} = $otsitav ]
        then
            echo "$el"
            mv $el ${el/$otsitav/$asendatav}
        fi
    done
### Pilt käsure väljundist
![10 4 1](https://user-images.githubusercontent.com/75208899/202539424-f6284eff-fabc-4dea-a0ab-9892520a8ac4.png)

## Viies harjutus
### Kood
    #!/bin/bash
    IFS=$'\n'
    echo "sisesta otsitav protsessi nimi:  "
    read otsitav
    echo ""

    protsessid=$(ps -A | grep "$otsitav")
    for p in $protsessid
    do
        echo " "$p | tr -s ' ' | cut -d ' ' -f2,5
    done
### Pilt käsure väljundist
![10 5 1](https://user-images.githubusercontent.com/75208899/202543103-947a1b0b-a02f-4fe1-a247-990ec3c924ec.png)

## Kuues harjutus
### Kood
    #!/bin/bash
    korrutamine () {
        if [ $2 -eq 1 ]
        then
        a=$(($1))
        else
        a=$(($1 * $(korrutamine $1 $(($2-1)))))
        fi
        echo $a
    }

    k=$(korrutamine 9 5)
    echo $k
### Pilt käsure väljundist
![10 6 1](https://user-images.githubusercontent.com/75208899/202549422-9bf94c29-35c1-48ea-87b9-d358f914a49a.png)


Täiendatud: 17/11/2022
