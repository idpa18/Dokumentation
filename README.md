# Dokumentation
## Konfiguration
Um dieses Projekt richtig zu nutzen, müssen ein paar Sachen installiert werden.

- VSCode als Editor
- VSCode Extension 'james-yu.latex-workshop' installieren
- In der Datei 'settings.json' bei VSCode, folgende Sachen einfügen (zur automatischen Generation des PDFs)
    ```json
    "latex-workshop.latex.tools": [
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-undump=pdflatex",
                "%DOCFILE%"
            ]
        },
        {
            "name": "biber",
            "command": "biber",
            "args": [
                "%DOC%"
            ]
        },
        {
            "name": "makeglossaries",
            "command": "makeglossaries",
            "args": [
                "%DOCFILE%"
            ]
        }
    ]
    ```
    ```json
    "latex-workshop.latex.recipes": [
        {
            "name": "pdflatex, biber, makeglossaries, pdflatex",
            "tools": [
                "pdflatex",
                "biber",
                "makeglossaries",
                "pdflatex"
            ]
        }
    ]
    ```

## Was wo?
Alle wichtigen Teile der Dokumentation sind in einer eigenen Datei.
Soll etwas bibliografiert werden, kann die Quelle in der Datei `opbef.bib` nach diesem [Format](https://www.overleaf.com/learn/latex/Bibliography_management_in_LaTeX#The_bibliography_file) hinzugefügt werden und nach diesem [Format](https://www.overleaf.com/learn/latex/Bibliography_management_in_LaTeX#Introduction) im Text Zitiert werden.
Einträge für den Glossar werden in der Datei `glossar.tex` nach diesem [Format](https://www.overleaf.com/learn/latex/Glossaries#Introduction) hinzugefügt und nach diesem [Format](https://www.overleaf.com/learn/latex/Glossaries#Introduction) im Text referenziert.

Wird das Dokument gespeichert, wird ein PDF daraus generiert (Oben rechts im VSCode PDF einblenden).

Für generelle Informationen zu LaTeX, ist [diese Seite](https://www.overleaf.com/learn/latex/Main_Page) super hilfreich. 
Auch Herr Schneider kann helfen.