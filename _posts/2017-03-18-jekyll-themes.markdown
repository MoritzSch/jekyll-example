---
layout: post
title:  "Jekyll Themes"
date:   2017-03-18 20:00:00 +0100
categories: jekyll update
---

Jekyll Themes:

Ein Theme kann in zwei unterschiedliche Arten installiert werden. 


Gem-basiertes Themes:

Eine Art ist das Theme als Gem zu installieren, dadurch kann man leichter die verschiedenen Themes austauschen. **[Hier](https://github.com/planetjekyll/awesome-jekyll-themes#official-themes)** befindet sich eine Liste von Themes die man per Ruby installieren kann.

Im Folgenden wird das Standart-Theme **Minima** durch das **Swiss** Theme ausgetauscht. 
1. Installation vom Theme `Jekyll-Swiss`: Um dieses Theme zu installieren muss der Befehl `gem install jekyll-swiss` in die Konsole eingegeben werden.
2. Bearbeiten der **Gemfile**: In der Gemfile muss die Zeile `gem "minima", "~> 2.0"` durch `gem "jekyll-swiss", "0.4.0"` ersetzt werden. Die Version dahinter kann jedoch weggelassen werden `gem "jekyll-swiss"`. 
3. Bearbeiten der **_config.yml**: In der _config.yml muss das Theme geändert werden. Die Zeile `theme: minima` muss durch `theme: jekyll-swiss` ersetzt werden.
4. Neustarten des Webservers. 

Der große Vorteil dieser Themes ist, dass man so leicht ohne größeren Aufwand verschiedene Themes austauschen und ausprobieren kann ohne größeren Aufwand.


Classic Themes:

Die andere Möglichkeit ist, das Theme herunterzuladen z.B. als .zip-Datei. Auf der Website **[Jekyll-Themes](http://jekyllthemes.org/)** befindet sich eine Liste sehr vieler Themes zum Herunterladen. 

Um das Theme zu benutzen muss die .zip-Datei extrahiert werden. Der erstellte Ordner ist nun eine leere Jekyll-Website mit dem heruntergeladenen Theme. 
Nun kann man in den meisten Fällen wie gewohnt in `_post` seine Einträge erstellen und den Webserver starten. 
