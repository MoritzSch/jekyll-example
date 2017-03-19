---
layout: post
title:  "Wie wird das HTML generiert?"
date:   2017-03-18 18:00:00 +0100
categories: jekyll update
---
Die vom Benutzer mit einer beliebigen **Markup-Sprache** (Markdown, Textile usw.) erstellten Dateien werden von **Jekyll** durch die Endung der Datei, bei Markdown **(".markdown")** erkannt 
und leitet diese Datei an den passenden Konverter (bei Markdown normalerweise **[KramDown](https://kramdown.gettalong.org/)**) weiter, welcher die Markup-sprache in HTML umwandelt. 
Zusammen mit einem ausgesuchtem oder einem benutzerdefiniertem **[Theme](http://jekyllthemes.org/)** wird der Inhalt der Seite an eine **[Template-Engine](https://jekyllrb.com/docs/templates/)** (in diesem Fall Liquid) weitergegeben, 
welche es dem Nutzer unmöglich macht willkürlichen Code auf der Seite auszuführen.