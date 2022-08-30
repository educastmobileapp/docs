# Technische Dokumentation

In diesem Repository ist das MkDocs-Projekt zur technischen Dokumentation der educast.nrw-App gespeichert. Die Dokumentation kann unter https://educastmobileapp.github.io/docs/ aufgerufen werden.

## Dev Setup
Als Erstes muss MkDocs installiert werden:
`pip install mkdocs`.

### Commands
Einige wichtige Commands sind:

1. `mkdocs serve` 
    - Mit diesem Command wird die Dokumentation lokal gehosted und kann getestet werden.
2. `mkdocs gh-deploy` 
    - Dieser Command kompiliert die Website und veröffentlicht Sie auf der oben genannten Domain.

### Workflow
Die Dokumentation ist im Unterordner "docs" zu erstellen, wobei `index.md` die Home-Seite darstellt.
Alles weitere ist auf der MkDocs-Website zu finden: https://www.mkdocs.org/  
Alle Datein sind ganz normal mit git zu tracken.  
Kurzes Markdown Tutorial: https://www.youtube.com/watch?v=9rKA62-0Gck.  
Markdown Editor für Windows (quasi Markdown IDE): [Markdown Monster](https://markdownmonster.west-wind.com/download)