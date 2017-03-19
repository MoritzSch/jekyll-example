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

Desweiteren ist es für den Benutzer möglich seine eigenen Blogs sehr leicht zu ändern und zu ersetzen. Dazu müssen nur die gespeicherten **Markup-Dateien** in dem **_posts** Ordner verändert, 
Jekyll gestartet und somit eine statische HTML-Seite generiert werden.


# Installation Windows:

Um Jekyll auf seinem eigenen Windows-Rechner nutzen zu können sollte man sich den Package-Manager **[Chocolatey](https://chocolatey.org/install)** installieren. 
Nachdem die Installation ausgeführt wurde öffnet man die Konsole als Administrator. Dort muss der Befehl ``choco install ruby –y`` eingegeben werden, welcher die Installation von der aktuellsten Ruby-Version ausführt.  

Jetzt gibt es die Möglichkeit seine erste Testseite mit dem Befehl ``jekyll new Ordnername`` zu erstellen. Um den Testserver zu starten muss man in den erstellten Ordner navigieren und dort den Befehl ``jekyll serve`` ausführen. 
Die domain unter der die lokale Seite erreichbar ist wird nach einer kurzen Ladezeit in der Konsole angezeigt.


# Jekyll Themes:

Ein Theme kann in zwei unterschiedliche Arten installiert werden. 


## Gem-basiertes Themes:

Eine Art ist das Theme als Gem zu installieren, dadurch kann man leichter die verschiedenen Themes austauschen. **[Hier](https://github.com/planetjekyll/awesome-jekyll-themes#official-themes)** befindet sich eine Liste von Themes die man per Ruby installieren kann.

Im Folgenden wird das Standart-Theme **Minima** durch das **Swiss** Theme ausgetauscht. 
1. Installation vom Theme `Jekyll-Swiss`: Um dieses Theme zu installieren muss der Befehl `gem install jekyll-swiss` in die Konsole eingegeben werden.
2. Bearbeiten der **Gemfile**: In der Gemfile muss die Zeile `gem "minima", "~> 2.0"` durch `gem "jekyll-swiss", "0.4.0"` ersetzt werden. Die Version dahinter kann jedoch weggelassen werden `gem "jekyll-swiss"`. 
3. Bearbeiten der **_config.yml**: In der _config.yml muss das Theme geändert werden. Die Zeile `theme: minima` muss durch `theme: jekyll-swiss` ersetzt werden.
4. Neustarten des Webservers. 

Der große Vorteil dieser Themes ist, dass man so sehr leicht verschiedene Themes austauschen und ausprobieren kann ohne größeren Aufwand.


## Classic Themes:

Die andere Möglichkeit ist, das Theme herunterzuladen z.B. als .zip-Datei. Auf der Website **[Jekyll-Themes](http://jekyllthemes.org/)** befinden sich eine Liste sehr viele Themes zum Herunterladen. 

Um das Theme zu benutzen muss die .zip-Datei extrahiert werden. Der erstellte Ordner ist nun ein leere Jekyll-Website mit dem heruntergeladenen Theme. 
Nun kann man in den meisten Fällen wie gewohnt in `_post` seine Einträge erstellen und den Webserver starten. 


# Wie wird das HTML generiert?

Die vom Benutzer mit einer beliebigen **Markup-Sprache** (Markdown, Textile usw.) erstellten Dateien werden von **Jekyll** durch die Endung der Datei, bei Markdown **(".markdown")** erkannt 
und leitet diese Datei an den passenden Konverter (bei Markdown normalerweise **[KramDown](https://kramdown.gettalong.org/)**) weiter, welcher die Markup-sprache in HTML umwandelt. 
Zusammen mit einem ausgesuchtem oder einem benutzerdefiniertem **[Theme](http://jekyllthemes.org/)** wird der Inhalt der Seite an eine **[Template-Engine](https://jekyllrb.com/docs/templates/)** (in diesem Fall Liquid) weitergegeben, 
welche es dem Nutzer unmöglich macht willkürlichen Code auf der Seite auszuführen.