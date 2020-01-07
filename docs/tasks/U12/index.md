---
author:	Alexander Bazo
date: 11. September 2019
---

# Übungsblatt 12

## Wichtige Informationen zur Bearbeitung der Aufgabe 

 - [Informationen zur Entwicklungsumgebung *IntelliJ IDEA*](https://regensburger-forscher.de/oop/tutorials/Entwicklungsumgebung)
 - [Informationen zum Im- und Export von Projekten](https://regensburger-forscher.de/oop/tutorials/Starterprojekte)

## **Flight Planner**

Ihre Aufgabe ist es, ein Programm zu schreiben, welches aus einer Datei Flugziele von verschiedenen Städten aus ausliest und dem Nutzer erlaubt, einen Round-Trip mit dem Flugzeug zu planen. Die Verbindungen werden zuerst in einer Datei abgelegt.

Das Ergebnis sollte wie folgt aussehen:

![image](img/11_flights.png)

### Das IntelliJ-Projekt

Legen Sie ein neues IntelliJ-Projekt an, und erzeugen Sie eine Klasse `FlightPlanner`, in der Sie die `main`-Methode des Programms implementieren. Die Datenbasis für die Aufgabe besteht aus einem `String`-Array, das wie folgt aussieht:

```
    private String[] flights = new String[]{
            "San Jose->San Francisco",
            "San Jose->Anchorage",
            "New York->Anchorage",
            "New York->San Jose",
            "New York->San Francisco",
            "New York->Honolulu",
            "Anchorage->New York",
            "Anchorage->San Jose",
            "Honolulu->New York",
            "Honolulu->San Francisco",
            "Denver->San Jose",
            "San Francisco->New York",
            "San Francisco->Honolulu",
            "San Francisco->Denver"};
```

Schreiben Sie eine Klasse `FlightDestinationParser`, die dieses Array sinnvoll in eine `HashMap` speichert.

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

