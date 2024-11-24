https://github.com/orgs/FonamentsEnginyeria/sso?authorization_request=BMGAIGREX4EOOLERFKQCUWLHHR2RZA5PN5ZGOYLONF5GC5DJN5XF62LEZYBWSSE6VVRXEZLEMVXHI2LBNRPWSZGOO2Z65Y5PMNZGKZDFNZ2GSYLML52HS4DFVNHWC5LUNBAWGY3FONZQ


Hi ha un "esquema" he canviat el com es veu:
Veuràs que es comença per Mermaid. Tot el que hi ha dins d'aquest bloc col·loca això:

graph TD
    A[Script Principal] --> B{Menú}
    B --> OP1
    B --> OP2
    B --> OP3
    B --> OP4
    B --> OP5

    OP1[OP1] --> SubOpcions1
    OP2[OP2] --> SubOpcions2
    OP3[OP3]
    OP4[OP4]
    OP5[Sortir]

    %% Estilo de los nodos
    style A fill:#f9f,stroke:#333,stroke-width:4px,color:#000
    style B fill:#bbf,stroke:#333,stroke-width:2px,color:#000
    style OP1 fill:#bbf,stroke:#333,stroke-width:2px,color:#000
    style OP2 fill:#bbf,stroke:#333,stroke-width:2px,color:#000
    style OP3 fill:#bbf,stroke:#333,stroke-width:2px,color:#000
    style OP4 fill:#bbf,stroke:#333,stroke-width:2px,color:#000
    style OP5 fill:#f99,stroke:#333,stroke-width:2px,color:#000

    %% Estilo de las flechas
    linkStyle 0 stroke:#f66,stroke-width:2px
    linkStyle 1 stroke:#f66,stroke-width:2px
    linkStyle 2 stroke:#f66,stroke-width:2px
    linkStyle 3 stroke:#f66,stroke-width:2px
    linkStyle 4 stroke:#f66,stroke-width:2px
    linkStyle 5 stroke:#f66,stroke-width:2px

Més coses.

- A l'apartat de Detalls Tècnics:
On posa Opció 2: Cera al catàleg. S'ha de posar el següent text:
Permet visualitzar la informació dels arxius `.csv` de manera filtrada per mitjà de diferents tipus de filtres (any, títol de la pel·lícula i actor/actriu). Aquesta opció disposa d'un submenú que crida als següents scripts:
	- **tasca2-1.sh **: Mostra la informació filtrada per una franja d'anys introduits manualment.
	- **tasca2-2.sh **: Mostra la informació filtrada pel títol de les pel·lícules, que s'introdueix manualment.
	- **tasca2-3.sh **: Mostra la informació filtrada pel nom de l'autor o actriu, que s'introdueix manualment.
>Es mostra una pestanya per poder introduir les dades requerides per cada script. Aquesta pestanya disposa de verificació en cas que les dades introduides no siguin les correctes.

(Has de treure els espais després dels noms dels arxius, entre ".sh" i "**")

i, per últim:

On hi ha els Scripts Secundaris:

A continuació del que ja hi ha has de posar això:

#### tasca2-1.sh
- **Funció**: Mostra la informació dels dos arxius `.csv` entre una franja d'anys. Aquesta franja ha de venir introduida per paràmetre, cal que s'introdueixi de la següent forma:
bash
bash tasca2.1.sh csv1 csv2 anyInici anyFinal

- **Input **: Requereix dos arxius `.csv` i de dos anys com a paràmetres.
#### tasca2-2.sh
- **Funció **: Mostra la informació dels dos arxius `.csv` filtrada pel títol. El titol de la pelicula, parcial o total, cal que s'introdueixi per paràmetre, cal que s'introdueixi de la següent forma:
bash
bash tasca2.1.sh csv1 csv2 "Títol pel·lícula"

- **Input **: Requereix dos arxius `.csv` i el títol a cercar com a paràmetres.
> **Nota **
> És preferible que el títol de la pel·lícula estigui entre cometes, per tal que funcioni de manera correcta
#### tasca2-3.sh
- **Funció **: Mostra la informació dels dos arxius `.csv` filtrada pel nom de l'actor o actriu. El nom, parcial o total, cal que s'introdueixi per paràmetre, cal que s'introdueixi de la següent forma:
bash
bash tasca2.1.sh csv1 csv2 "Nom actor/actriu"
```
- *Input *: Requereix dos arxius .csv i el nom a cercar com a paràmetres.
> *Nota *
> És preferible que el nom de l'actor o actriu estigui entre cometes, per tal que funcioni de manera correcta
