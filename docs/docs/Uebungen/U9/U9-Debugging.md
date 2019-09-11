---
author:	Alexander Bazo
date: 11. September 2019
---


## Übung zur Einführung in die objektorientierte Programmierung mit Java

# Übungsblatt 9

### **Debugging der ClickObjects-Aufgabe [gemeinsam bearbeiten]**

In der letzten Woche haben Sie in der Übung eine Anwendung zur
Demonstration von Interfaces programmiert. Im aktuellen Starterpaket
finden Sie eine Lösung zu dieser Aufgabe. Es haben sich allerdings drei Fehler eingeschlichen, die verhindern, dass die Anwendung wie gewünscht funktioniert.

Versuchen Sie die fehlerhaften Stellen im Code zu identifizieren und
auszubessern. Gehen Sie dabei systematisch vor und berücksichtigen Sie
die Hinweise und *Debugging*-Strategien aus der aktuellen Vorlesung.

Nutzen Sie dazu auch den eingebauten *Debugger* Ihrer
Entwicklungsumgebung, um die Vorgänge im Programm schrittweise
nachzuvollziehen. Sie können dazu z.B. *Breakpoints* setzen, die Anwendung über das entsprechende *Debugger*-Icon starten und *Schritt-für-Schritt* durchgehen. 

Achten Sie genau auf die Reihenfolge der Methodenaufrufe,
die logische Anordnung von Kontrollstrukturen und die verwendeten
Parameter. Rufen Sie sich im Vorfeld die Anforderungen der Aufgabe
(siehe letztes Übungsblatt) in Erinnerung und testen Sie regelmäßig und ausführlich, ob alle Funktionen nutzbar sind.

**Achtung:** Auf der folgenden Seite finden Sie eine Liste mit den
Fehlern und einer kurzen Erklärung zu diesen. Versuchen Sie aber bitte
zuerst, das Programm eigenständig zu *debuggen*. Kontrollieren Sie dann anhand der Lösung, ob Sie alle fehlerhaften Stellen gefunden haben.

Lösung
------

1.  **Initialisierung der klickbaren Objekte**
    (`ClickObjects.java, Zeile 63`)\
    In der Methode `createObjects()` der `ClickObjects`-Klasse werden
    Instanzen der klickbaren Objekte erzeugt und zusätzlich in einem
    Array abgespeichert. Dieses Array wird durchlaufen, wenn ein
    Mausklick im Programm registriert wird. Dabei wird überprüft,
    welches der Objekte geklickt wurde und anschließend der
    Klick-Handler der Klasse aufgerufen. Bei der Initialisierung wurde
    vergessen, das letzte Element von `clickables` zu belegen. So wird
    durch den Zugriff in der mouseClicked()-Methode eine
    `NullPointerException` ausgelöst.

2.  **Positionieren der Augen** (`Eye.java, Zeile 26`)\
    Nach dem Starten der Anwendung sind nur 3 der 4 Objekte sichtbar.
    Der Grund dafür findet sich in der `Eye`-Klasse. Im Konstruktor
    werden die entsprechenden Instanzvariablen mit den Initialwerten
    belegt. Dabei wird jedoch der Parameter für die y-Position auch mit
    dem Wert des `xPos`-Parameters belegt. Da der y-Wert so zu groß für
    den Canvas ist, ist das Auge unsichtbar.

3.  **Darstellung der Tiere** (`Animal.java, Zeile 15`)\
    Die Tiere lassen sich nicht zeichnen -- sobald Zeichenaufruf
    stattfindet, produziert das Programm eine `NullPointerException`.
    Verantwortlich ist ein fehlender Initialisierungsaufruf in der
    Klasse `Animal`. Im Konstruktor muss die Methode `createImage()`
    aufgerufen werden. Passiert dies nicht, entsteht bei den
    implementierten Methoden des `Clickable`-Interface und der
    `draw()`-Methode ein Zugriff auf eine nicht initialisierte Variable.
    Dies führt zum Ausnahmefehler.
