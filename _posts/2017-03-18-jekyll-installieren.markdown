---
layout: post
title:  "Jekyll installieren"
date:   2017-03-18 22:00:00 +0100
categories: jekyll update
---
Installation Windows:

Um Jekyll auf seinem eigenen Windows-Rechner nutzen zu können sollte man sich den Package-Manager **[Chocolatey](https://chocolatey.org/install)** installieren. 
Nachdem die Installation ausgeführt wurde öffnet man die Konsole als Administrator. Dort muss der Befehl ``choco install ruby –y`` eingegeben werden, welcher die Installation von der aktuellsten Ruby-Version ausführt.  

Nun muss der Befehl ``gem install jekyll`` in die Konsole eingegeben werden um das "gem" jekyll zu installieren, welches benötigt wird um die HTML Seite zu generieren.

Jetzt gibt es die Möglichkeit seine erste Testseite mit dem Befehl ``jekyll new Ordnername`` zu erstellen. Um den Testserver zu starten muss man in den erstellten Ordner navigieren und dort den Befehl ``jekyll serve`` ausführen. 
Die Domain unter der die lokale Seite erreichbar ist wird nach einer kurzen Ladezeit in der Konsole angezeigt.

Auf der entstandenen Website sieht man das Jekyll-Standard-Theme "minima". Die Seite sollte nun wie folgt aussehen:

![Jekyll-Minima]({{ site.baseurl }}/img/neue_jekyll_seite.JPG)