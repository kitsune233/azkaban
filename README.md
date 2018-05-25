# azkaban

La presó d'Azkaban necessita una base de dades per portar el control dels reclusos. Aquestes són les necessitats:

>Tenim els delictes codificats, un preś pot estar comdemnat per més d'un delicte. 
Per cada delicte cal apuntar els dies de commdenna, la comdenna total és la suma de tots els dies.
Del pres ens interessa el seu número identificador, el nom i la data d'ingrés.
Els presos estan confinats en cel·les, cada cel·la té un número i un aforament. 
També apuntem a quin número de mòdul es troba la cel·la.
Els presos poden gaudir de permisos ( sempre que hagin complert més d'un 50% de comdenna ). 
Un permís comença en una data i finalitza en una altra data. No es poden sol·lapar permisos.

## MCD

T01 - Fes el MCD de dades.

## SQL

* T02 - Fes el create table. En cas de canviar el nom d'una cel·la, aquest canvi es propagarà.
* T03 - Inserta les següents dades.
  * Carlotta Pinkstone. Des de 1 de gener de 2018
     * Estatuto Internacional del Secreto Mágico: 600 dies
  * Bartemius Crouch Jr. Des de 1 de gener de 2015
     * Torturar con la maldición Cruciatus: 300 dies
     * Assessinar: 900 dies
  * Antonin Dolohov. Des de 1 de maig de 2016
     * Assessinar: 900 dies

## Funcions

Fes les funcions:

* T04 - Calcula data de sortida de la presó. Donat un prés ens diu quin dia surt.
* T05 - Calcula % de comdemna. Donat un pres ens diu el % de comdemna que porta complert.

## Procediments:

* Fes el procediment `otorgar permís` que funciona segons les normes de l'enunciat i rep el següents paràmetres:
  * Número de dies de permís.
  * Pres
  * Dia inici del permís
  

