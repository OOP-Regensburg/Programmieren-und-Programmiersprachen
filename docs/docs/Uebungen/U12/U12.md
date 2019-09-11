---
author:	Alexander Bazo
date: 11. September 2019
---


## Übung zur Einführung in die objektorientierte Programmierung mit Java

# Übungsblatt 12

### **Flight Planner [gemeinsam bearbeiten]**

Ihre Aufgabe ist es, ein Programm zu schreiben, welches aus einer Datei Flugziele von verschiedenen Städten aus ausliest und dem Nutzer erlaubt, einen Round-Trip mit dem Flugzeug zu planen.

Das Ergebnis sollte wie folgt aussehen:

![image](_img/11_flights.png)

**Hinweis:** Eine besondere Schwierigkeit in dieser Aufgabe ist,
angemessene Datenstrukturen zu modellieren, um sich die Informationen,
die für den weiteren Ablauf benötigt werden, abzuspeichern. Man muss
sich sowohl die möglichen Flüge aus der Datei `flights.txt` merken, als auch die Route, die der Nutzer schon zurückgelegt hat. Überlegen Sie hier, wann eine `ArrayList` und wann eine `HashMap` sinnvoll zu benutzen sind. Die Flugdaten stehen in einer Datei `data/assets/flights.txt` im Starterpaket zur Verfügung. Diese Datei ist wie folgt formatiert:

-   Jede Zeile besteht aus einem Städtepaar, unterteilt durch einen
    Pfeil, z.B.:\
    **New York -\> Anchorage**

-   Die Datei soll der Übersicht halber Leerzeilen enthalten können (die
    beim Auslesen zu ignorieren sind)

Die vorgegebene Datei enthält folgenden Inhalt. Ihr Programm sollte aber auch mit anderen Städte-Kombinationen funktionieren, die in der selben Weise formatiert sind.

    San Jose->San Francisco
    San Jose->Anchorage

    New York->Anchorage
    New York->San Jose
    New York->San Francisco
    New York->Honolulu

    Anchorage->New York
    Anchorage->San Jose

    Honolulu->New York
    Honolulu->San Francisco

    Denver->San Jose

    San Francisco->New York
    San Francisco->Honolulu
    San Francisco->Denver

Ihr Programm soll folgende Anforderungen erfüllen:

-   Die Informationen aus der Datei `flights.txt` einlesen und in einer
    geeigneten Datenstruktur abspeichern.

-   Die komplette Städteliste anzeigen.

-   Den Benutzer eine Stadt auswählen lassen, von der aus die Rundreise
    beginnt.

-   In einer Schleife alle Städte anzeigen, die von der aktuellen Stadt
    aus direkt erreicht werden können und den Nutzer nach der nächsten
    Stadt fragen.

-   Sobald der Nutzer wieder zur Anfangsstadt kommt, bricht die Schleife
    ab und das Ergebnis der Flugroute wird ausgegeben.

----

**Hinweis:** Übungsaufgaben und Konzept basieren zum Teil auf dem Kurs
*CS106A: Programming Methodology* der Universität Stanford von Eric
Roberts und Mehran Sahami
