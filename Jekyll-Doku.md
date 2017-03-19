---
layout: page
title: Jekyll-Doku
permalink: /Jekyll-Doku/
---

* Inhaltsverzeichnis
{:toc}

# Was ist Jekyll?

Jekyll ist ein statischer Webseitengenerator, welcher normale Markup-Dateien (z. B. erstellt mit Markdown) in **statisches HTML** umwandelt. 
Außerdem basiert GitHub auf Jekyll, somit wird ermöglicht seine eigene Website kostenlos auf einem Github-Server zu hosten.

Des Weiteren ist es für den Benutzer möglich seine eigenen Blogs sehr leicht zu ändern und zu ersetzen. Dazu müssen nur die gespeicherten **Markup-Dateien** in dem **_posts** Ordner verändert, 
Jekyll gestartet und somit eine statische HTML-Seite generiert werden.


# Installation Windows:

Um Jekyll auf seinem eigenen Windows-Rechner nutzen zu können sollte man sich den Package-Manager **[Chocolatey](https://chocolatey.org/install)** installieren. 
Nachdem die Installation ausgeführt wurde öffnet man die Konsole als Administrator. Dort muss der Befehl ``choco install ruby –y`` eingegeben werden, welcher die Installation von der aktuellsten Ruby-Version ausführt.  

Nun muss der Befehl ``gem install jekyll`` in die Konsole eingegeben werden um das "gem" jekyll zu installieren, welches benötigt wird um die HTML Seite zu generieren.

Jetzt gibt es die Möglichkeit seine erste Testseite mit dem Befehl ``jekyll new Ordnername`` zu erstellen. Um den Testserver zu starten muss man in den erstellten Ordner navigieren und dort den Befehl ``jekyll serve`` ausführen. 
Die Domain unter der die lokale Seite erreichbar ist wird nach einer kurzen Ladezeit in der Konsole angezeigt.

Auf der entstandenen Website sieht man das Jekyll-Standard-Theme "minima". Die Seite sollte nun wie folgt aussehen:

![Jekyll-Minima]({{ site.baseurl }}/img/neue_jekyll_seite.JPG)


# Grundlegende Einstellungen:

## Konfiguration der _config.yml:

Um die Startseite des Blogs anzupassen öffnet man die **_config.yml**. Dort kann der Titel bei dem Unterpunkt ``title:`` beliebig angepasst werden. Außerdem ist es möglich der Seite eine Beschreibung hinzuzufügen. 
Dies ist durch den Unterpunkt ``description:`` möglich. Weiterhin kann der Konverter bei dem Gliederungspunkt ``markdown:`` angepasst werden. Standardmäßig steht dieser auf **kranmdown** was die besten Möglichkeiten bietet.
Bei ``exclude:`` werden die Dateien eingetragen, die von dieser Konfiguration ausgeschlossen sind und somit auch nicht auf der Seite angezeigt werden.


## Erstellung eines Posts:

Um einen neuen Post zu erstellen müssen erst einige Konfigurationen getroffen werden. Die Datei, die den Post enthalten soll, muss im Namen immer ein Datum im folgenden Format enthalten ``2017-03-14-examplename``,
des Weiteren sollte immer mit der Dateiendung **.markdown** verwendet werden. Außerdem ist es nötig die Datei mit einem ``---`` zu starten. Unter diesen drei Bindestrichen werden die Grundlegenden YAML Anweisungen des Dokuments festgelegt. 
Grundlegende Parameter sind: ``layout:`` welcher bei einem Post auf ``layout: post`` gesetzt ist, einem Titel: ``title: "exampleTitle"`` und dem Datum: ``date:2017-03-19 14:07:30 +0100``. Diese YAML Anweisungen werden auch wieder durch ``---`` beendet.


## Erstellung eines Menüpunktes:

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


## Bild in einem Post hinzufügen:

Um ein Bild in einen Post hinzuzufügen muss zuerst ein neuer Ordner erstellt werden. Der Ordner kann einen beliebigen Namen besitzen, jedoch darf er nicht mit einen "_" anfangen. 
Das Bild in den neu angelegten Ordner kopieren. Nun muss man im Post an der gewünschten Stelle folgendes eingeben: 

`![Name-des-Bildes-in-HTML]({{ site.baseurl }}/angelegter_Ordner/Name_des_Bildes.DateiFormat)`

Ein Beispiel:

`![Jekyll-Minima]({{ site.baseurl }}/img/neue_jekyll_seite.JPG)`

Nun sollte das Bild im Post erscheinen.


# Jekyll Themes:

Ein Theme kann in zwei unterschiedliche Arten installiert werden. 


## Gem-basiertes Themes:

Eine Art ist das Theme als Gem zu installieren, dadurch kann man leichter die verschiedenen Themes austauschen. **[Hier](https://github.com/planetjekyll/awesome-jekyll-themes#official-themes)** befindet sich eine Liste von Themes die man per Ruby installieren kann.

Im Folgenden wird das Standart-Theme **Minima** durch das **Swiss** Theme ausgetauscht. 
1. Installation vom Theme `Jekyll-Swiss`: Um dieses Theme zu installieren muss der Befehl `gem install jekyll-swiss` in die Konsole eingegeben werden.
2. Bearbeiten der **Gemfile**: In der Gemfile muss die Zeile `gem "minima", "~> 2.0"` durch `gem "jekyll-swiss", "0.4.0"` ersetzt werden. Die Version dahinter kann jedoch weggelassen werden `gem "jekyll-swiss"`. 
3. Bearbeiten der **_config.yml**: In der _config.yml muss das Theme geändert werden. Die Zeile `theme: minima` muss durch `theme: jekyll-swiss` ersetzt werden.
4. Neustarten des Webservers. 

Der große Vorteil dieser Themes ist, dass man so leicht ohne größeren Aufwand verschiedene Themes austauschen und ausprobieren kann.


## Classic Themes:

Die andere Möglichkeit ist, das Theme herunterzuladen z.B. als .zip-Datei. Auf der Website **[Jekyll-Themes](http://jekyllthemes.org/)** befindet sich eine Liste sehr vieler Themes zum Herunterladen. 

Um das Theme zu benutzen muss die .zip-Datei extrahiert werden. Der erstellte Ordner ist nun eine leere Jekyll-Website mit dem heruntergeladenen Theme. 
Nun kann man in den meisten Fällen wie gewohnt in `_post` seine Einträge erstellen und den Webserver starten. 


# Wie wird das HTML generiert?

Die vom Benutzer mit einer beliebigen **Markup-Sprache** (Markdown, Textile usw.) erstellten Dateien werden von **Jekyll** durch die Endung der Datei, bei Markdown **(".markdown")** erkannt 
und leitet diese Datei an den passenden Konverter (bei Markdown normalerweise **[KramDown](https://kramdown.gettalong.org/)**) weiter, welcher die Markup-sprache in HTML umwandelt. 
Zusammen mit einem ausgesuchtem oder einem benutzerdefiniertem **[Theme](http://jekyllthemes.org/)** wird der Inhalt der Seite an eine **[Template-Engine](https://jekyllrb.com/docs/templates/)** (in diesem Fall Liquid) weitergegeben, 
welche es dem Nutzer unmöglich macht willkürlichen Code auf der Seite auszuführen.


# Git-Hub:

Damit ein Jekyll Webserver auf Git-Hub funktioniert muss die Datei **.gitlab-ci.yml** mit dem Folgenden Inhalt eingefügt werden:

```
image: ruby

pages:
  stage: build
  script:
  - gem install jekyll
  - jekyll build -d public
  artifacts:
    paths:
    - public
  only:
  - master
 ```
