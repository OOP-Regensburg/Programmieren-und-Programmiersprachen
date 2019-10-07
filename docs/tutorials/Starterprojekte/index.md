# Importieren und Exportieren von Starterprojekten  

Nachdem Sie IntelliJ installiert haben, und bevor Sie mit Bouncer und Java starten können, müssen Sie Starterprojekte in IntelliJ importieren. Diese enthalten alle notwendigen Dateien und Sie können sofort mit der Arbeit an den Übungsaufgaben und Studienleistungen beginnen. Die Starterprojekte finden Sie alle auf GRIPS. Auch die dort bereitgestellten Beispiele können Sie auf die gleiche Art und Weise importieren. Fertiggestelle Projekte können als ZIP-Archiv gepackt und weitergegeben werden. Studienleistungen müssen auf diese Weise in GRIPS hochgeladen werden.

## Herunterladen und Entpacken der Projekte

Laden Sie sich das entsprechende Starterprojekt aus GRIPS und speichern Sie es auf Ihrer Festplatte. Die Projekte werden in der Regel als ZIP-Archiv bereitgestellt. In dem Archiv finden Sie einen Ordner mit den Projektdateien. Entpacken Sie das Archiv und merken Sie sich den Dateipfad.

## Öffnen der Projekte in IntelliJ

Das entpackte Projekt können Sie in IntelliJ öffnen. Wählen Sie dazu auf dem Startbildschirm oder über das *File*-Menü den Punkt *Open* aus. Im nächsten Fenster navigieren Sie zu dem Ordner, in den Sie das Projekt-Archiv entpackt haben. Wählen Sie den Ordner[^1]. Bestätigen Sie die Auswahl mit OK und folgen Sie den Anweisungen des folgenden Dialogs: 

![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Farben-Testbild.svg/1024px-Farben-Testbild.svg.png?uselang=de)

## Einrichten des SDKs

Nach dem Öffnen der Projekte müssen Sie unter Umständen das zu verwendende Java SDK in den Projekteinstellungen auswählen; Sie erkennen das Fehlen dieser Einstellung an der Einblendung *Project SDK is not defined* über dem Editor-Fenster. Öffnen Sie dazu die Projekteinstellungen in dem Sie im Kontextmenü (Rechtsklick auf den Projektnamen) den Punkt *Open Module Settings* auswählen. Im nächsten Fenster wählen Sie den Reiter Project aus und fügen über New ein neues SDK ein (Abbildung 4). Wählen Sie anschließend den Ordner auf Ihrer Fest- platte aus, in dem das JDK (Siehe auch [Installation der IDE IntelliJ IDEA Community Edition](../Entwicklungsumgebung)) installiert ist. Bestätigen Sie die Auswahl und schließen Sie die Projekteinstellungen.

## Exportieren von Projekten

Wenn Sie ein Projekt exportieren möchten, müssen Sie dazu den gesamten Projektordner speichern und weitergeben. Der Ordner enthält alle Dateien und Informationen, die es Ihnen erlauben, das gespeicherte Projekt auch auf anderen Rechnern zu öffnen und zu bearbeiten. Am einfachsten speichern Sie den Ordner, indem Sie ein ZIP-Archiv erstellen. Unter Windows können Sie dazu im Explorer zum Projektordner navigieren und im Kontextmenü unter Senden an den Punkt ZIP-komprimierter Ordner auswählen. Die so erstellte ZIP-Datei können Sie unter anderem im GRIPS-Kurs hochladen, um die Studienleistungen einzureichen.

[^1]: Falls das Archiv aus mehreren Ebenen besteht, erkennen Sie den tatsächlichen Projektordner an der darin liegenden `*.iml`-Datei.