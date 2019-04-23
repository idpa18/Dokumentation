# Dokumentation

Bitte die Extension james-yu.latex-workshop für VSCode installieren.

Im VSCode unter settings.json ```json
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
    ],``` hinzufügen (evtl. nach die Commands installieren).

