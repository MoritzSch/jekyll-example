---
layout: post
title:  "Grundlegende Einstellungen"
date:   2017-03-18 21:00:00 +0100
categories: jekyll update
---
Konfiguration der _config.yml:

Um die Startseite des Blogs anzupassen öffnet man die **_config.yml**. Dort kann der Titel bei dem Unterpunkt ``title:`` beliebig angepasst werden. Außerdem ist es möglich der Seite eine Beschreibung hinzuzufügen. 
Dies ist durch den Unterpunkt ``description:`` möglich. Weiterhin kann der Konverter bei dem Gliederungspunkt ``markdown:`` angepasst werden. Standardmäßig steht dieser auf **kranmdown** was die besten Möglichkeiten bietet.
Bei ``exclude:`` werden die Dateien eingetragen, die von dieser Konfiguration ausgeschlossen sind und somit auch nicht auf der Seite angezeigt werden.

Erstellung eines Posts:

Um einen neuen Post zu erstellen müssen erst einige Konfigurationen getroffen werden. Die Datei, die den Post enthalten soll, muss im Namen immer ein Datum im folgenden Format enthalten ``2017-03-14-examplename``,
des Weiteren sollte immer mit der Dateiendung **.markdown** verwendet werden. Außerdem ist es nötig die Datei mit einem ``---`` zu starten. Unter diesen drei Bindestrichen werden die Grundlegenden YAML Anweisungen des Dokuments festgelegt. 
Grundlegende Parameter sind: ``layout:`` welcher bei einem Post auf ``layout: post`` gesetzt ist, einem Titel: ``title: "exampleTitle"`` und dem Datum: ``date:2017-03-19 14:07:30 +0100``. Diese YAML Anweisungen werden auch wieder durch ``---`` beendet.


Erstellung eines Menüpunktes:

Um einen neuen Menüpunkt zu erstellen muss eine **".md"** Datei erstellt werden. Diese muss in den ersten Zeilen folgendes beinhalten (wie bei **about.md**):

```
---
layout: "Layout-Name"
title: "Titel"
permalink: "Link"
---

```

Es könnte zum Beispiel wie folgt aussehen:

```
---
layout: page
title: Jekyll-Doku
permalink: /Jekyll-Doku/
---

```

Danach kann der Inhalt eingefügt werden.


Bild in einem Post hinzufügen:

Um ein Bild in einen Post hinzuzufügen muss zuerst ein neuer Ordner erstellt werden. Der Ordner kann einen beliebigen Namen besitzen, jedoch darf er nicht mit einen "_" anfangen. 
Das Bild in den neu angelegten Ordner kopieren. Nun muss man im Post an der gewünschten Stelle folgendes eingeben: 

`![Name-des-Bildes-in-HTML]({{ site.baseurl }}/angelegter_Ordner/Name_des_Bildes.DateiFormat)`

Ein Beispiel:

`![Jekyll-Minima]({{ site.baseurl }}/img/neue_jekyll_seite.JPG)`

Nun sollte das Bild im Post erscheinen.