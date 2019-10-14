---
author:	Alexander Bazo
date: 11. September 2019
---


## Übung zur Einführung in die objektorientierte Programmierung mit Java

# Übungsblatt 3


### **Große und kleine Zahlen finden**

In diesem Programm kann der Nutzer eine Reihe von Ganzzahlen eingeben.
Das Programm bestimmt die größte und kleinste Zahl und gibt diese am
Bildschirm aus, nachdem der Nutzer die Zahl 0 eingegeben hat:

![image](img/03_findrange)

Ihr Programm muss für die folgenden Sonderfälle funktionieren:

-   Wenn der Nutzer nur **eine** Zahl vor der 0 eingibt, soll das
    Programm diese Zahl als größte und kleinste Zahl ausgeben.

-   Wenn der Nutzer **als erste** Zahl eine 0 eintippt, erhält das
    Programm keine Werte und muss den Nutzer mit einer entsprechenden
    Meldung darauf hinweisen.

**Zielscheibe**

In dieser Aufgabe sollen Sie eine Zielscheibe auf dem Bildschirm
zeichnen:

![image](img/03_target)

Die Zielscheibe muss aus 15 Ellipse-Objekten bestehen und im Zentrum des
Bildschirms gezeichnet werden. Der mittlere Ring ist rot und hat einen
Durchmesser von 10, die Farben wechseln sich dann nach außen hin ab. Der
Durchmesser jedes weiteren Rings entspricht dem seines Vorgängers,
erhöht um den Durchmesser des ersten Rings.

Legen Sie für die Anzahl der Ringe und den Durchmesser des innersten
Rings geeignete Konstanten an, und testen Sie, ob Ihr Programm auch mit
anderen Werten einwandfrei funktioniert. Legen Sie weitere Konstanten
an, um Ihren Code robuster gegen Veränderungen zu machen.

**Tipp:** Die Ringe werden übereinander gezeichnet, d.h. Sie müssen mit
dem äußersten Ring anfangen, um zu vermeiden, dass die kleineren Ringe
verdeckt werden.

### **Pythagoras**

Der Satz des Pythagoras besagt, dass sich die Seitenlängen eines
rechtwinkligen Dreiecks wie folgt verhalten: `a^2 + b^2 = c^2`

Diese Gleichung lässt sich wie folgt umschreiben: `c = sqrt(a^2+b^2)`

Sie haben die meisten Operatoren in dieser Gleichung bereits in der
Vorlesung kennengelernt. Es fehlt lediglich die Berechung der Wurzel,
die Sie durch Aufruf der Methode `Math.sqrt()` berechnen können.
Beispielsweise setzt der folgende Aufruf den Wert der Variablen `y` auf
den Wert der Wurzel aus `x`.

`double y = Math.sqrt(x);`

Schreiben Sie ein Programm, bei dem der Nutzer die Werte für `a` und `b`
als Ganzzahlen eingeben kann. Anschließend wird daraus `c` als `double`
berechnet und das Ergebnis wieder an den Nutzer ausgegeben:

![image](img/03_pythagoras)

### **Hailstone Puzzle**

Douglas Hofstadters mit dem Pulitzer-Preis prämiertes Buch *Gödel,
Escher, Bach* beinhaltet viele interessante mathematische Rätsel, von
denen viele durch Computer-Programme gelöst werden können. In Kapitel 12
beschreibt Hofstadter ein Problem, welches gut zum aktuellen Stoff
passt. Das Problem kann folgendermaßen beschrieben werden:

- Man nehme eine positive Ganzzahl und nenne sie *n*.
- Falls *n* gerade ist, halbiere man sie.
- Ist *n* ungerade, multipliziere man sie mit drei und zähle eins dazu.
- Dann setze man diesen Prozess solange fort, bis *n* den Wert
eins angenommen hat.

Auf Seite 401 veranschaulicht Hofstadter diesen Prozess mit folgendem
Beispiel, beginnend mit der Nummer 15:

zahl ist (un)gerade, also nehme man xxxx: Ergebnis

15 ist ungerade, also nehme man 3n+1: 46.\
46 ist gerade, also halbiere man: 23.\
23 ist ungerade, also nehme man 3n+1: 70.\
70 ist gerade, also halbiere man: 35.\
35 ist ungerade, also nehme man 3n+1: 106.\
106 ist gerade, also halbiere man: 53.\
53 ist ungerade, also nehme man 3n+1: 160.\
160 ist gerade, also halbiere man: 80.\
80 ist gerade, also halbiere man: 40.\
40 ist gerade, also halbiere man: 20.\
20 ist gerade, also halbiere man: 10.\
10 ist gerade, also halbiere man: 5.\
5 ist ungerade, also nehme man 3n+1: 16.\
16 ist gerade, also halbiere man: 8.\
8 ist gerade, also halbiere man: 4.\
4 ist gerade, also halbiere man: 2.\
2 ist gerade, also halbiere man: 1.

Aus dem Beispiel wird ersichtlich, dass die Zahl zwar steigt und sinkt, aber irgendwann - zumindest für alle Zahlen, die jemals probiert wurden - wird die Zahl 1 erreicht. In gewisser Hinsicht ist dieser Prozess
ähnlich dem Entstehen eines Hagelkorns (engl. *hailstone*) oder einer
Schneeflocke, die im Wind immer wieder nach oben und unten fliegen,
bevor sie zu Boden fallen. Aufgrund dieser Analogie wird diese Sequenz
normalerweise *hailstone sequence* genannt, obwohl es dafür auch viele
andere Namen gibt. Schreiben Sie ein Programm, welches eine Nummer von
der Konsole einließt und die dazugehörige *hailstone sequence* ausgibt,
wie in Hofstadters Buch beschrieben. Anschließend wird ausgegeben, wie
viele Schritte benötigt wurden, um die Zahl 1 zu erreichen. Ihr Programm
sollte eine Ausgabe wie im folgenden Beispiel erzeugen können:

![image](img/03_hailstone)

### **Fibonacci**

Im dreizehnten Jahrhundert formulierte der italienische Mathematiker
Leonardo Fibonacci eine Zahlensequenz, um die Ausbreitung einer
Hasenpopulation zu beschreiben. Die ersten beiden Zahlen dieser
Fibonacci-Folge (`Fib(0)` und `Fib(1)`) sind 0 und 1, jede darauf
folgende Zahl ist die Summe Ihrer beiden Vorgänger. Die ersten Zahlen
der Fibonacci-Folge sehen wie folgt aus:

`Fib(0)` = 0\
`Fib(1)` = 1\
`Fib(2)` = 1 (0+1)\
`Fib(3)` = 2 (1+1)\
`Fib(4)` = 3 (1+2)\
`Fib(5)` = 5 (2+3)\

Erstellen Sie ein Programm, das die Fibonacci-Folge ab `Fib(0)` ausgibt,
solange der Wert für die aktuelle Fibonacci-Zahl unter 500 liegt.

Ihr Programm berechnet solange neue Zahlen, solange diese unter dem
Maximalwert (z.B. 500 liegen). Ihr Programm benötigt daher eine Zeile
wie z.B.:

`while (nextFib < MAX_VALUE)`\
Legen Sie `MAX_VALUE` als Konstante ab.

![image](img/03_fibonacci)

### **Schachbrett**

Zeichnen Sie ein Schachbrettmuster mit Hilfe der *GraphicsApp*. Nutzen
Sie die bekannten Funktionalitäten der *GraphicsApp* um ein
Schachbrettmuster auf dem Bildschirm zu Zeichnen. Das Muster soll aus
acht Zeilen und Spalten bestehen, die abwechselnd weiße bzw. schwarze
gleichgroße Rechtecke enthalten. Legen Sie die Breite und Höhe der
Anwendung in geeigneten *Konstanten* fest und berechnen Sie Position und
Größe der Rechtecke basierend auf diesen Werten. Nutzen Sie geeignete
Kontrollstrukturen, um das Zeichnen der Felder effektiv zu gestalten.

Teilen Sie das Programm in zwei Methoden auf. In der einen
initialisieren Sie die Anwendung (Größe und Hintergrundfarbe) und in der
anderen zeichnen Sie das Schachbrettmuster.

![image](img/03_chess)

### **Copy & Paste**

Bouncers Aufgabe ist es, die linke Hälfte der Karte spiegelverkehrt auf
der rechten Seite nachzuzeichnen. Um dies zu erreichen, soll er jede
Zeile der Karte vom linken Rand (`x=0`) bis zur Mitte (`x=7`)
durchlaufen. Stößt er auf ein grünes Feld, merkt er sich den Abstand des
Feldes vom linken Rand und zeichnet es auf der gegenüberliegenden,
rechten Seite im gleichen Abstand ein. Anschließend setzt er die
Überprüfung der aktuellen Zeile an der Stelle fort, an der er das zu
spiegelnde Feld gefunden hat. Das erste grüne Feld hat die Koordinaten
(`x=2,y=2`) und würde nach diesen Regeln an die Position (`x=13,y=2`)
gespiegelt. Sie können davon ausgehen, dass die Karte immer die selben
Dimensionen (15x15) hat und das es nur leere oder grüne Felder gibt. Für eine sinnvolle Lösung der Aufgabe werden Sie Variablen einsetzen
müssen.

Bei der Bearbeitung sollten Sie über folgende Teilprobleme nachdenken:

-   Sorgen Sie dafür, dass Bouncer eine beliebige Zeile bis zur Mitte
    durchläuft und von einer Zeile in die nächste darunterliegende Zeile
    wechseln kann. Kombinieren Sie diese Aktionen so, dass Bouncer alle
    15 Zeilen überprüft.

-   Lassen Sie Bouncer die Farbe der Felder überprüfen.

-   Überlegen Sie sich, wie Sie Bouncer in die Lage versetzen, ein Feld
    in einem bestimmten Abstand vom rechten Rand einzufärben.

-   Überlegen Sie sich, wie Bouncer zu einem bestimmten Feld in der
    aktuellen Zeile zurückkehren kann.

![image](img/03_copyAndPaste)
