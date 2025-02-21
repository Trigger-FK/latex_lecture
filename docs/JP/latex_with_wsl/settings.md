```json
{
    "[latex]": {
        "editor.tabSize": 2,
        "editor.wordWrap": "on",
        "editor.suggest.snippetsPreventQuickSuggestions": false,
        "editor.bracketPairColorization.enabled": true,
        "editor.unicodeHighlight.invisibleCharacters": true,
        "editor.wordSeparators": "./\\()\"'-:,.;<>~!@#$%^&*|+=[]{}`~?。．、，（）「」『』［］｛｝《》てにをはがのともへでや ",
        "editor.unicodeHighlight.allowedCharacters": {
            "，": true,
            "．": true,
        },
    },
    "[bibtex]": {
        "editor.tabSize": 2,
        "editor.wordWrap": "on"
    },
    "files.exclude": {
        // "out/*.bbl": true,
        "**/*.log": true,
        "**/*.dvi": true,
        "**/*.fls": true,
        "**/*.aux": true,
        "**/*.blg": true,
        "**/*.out": true,
        "**/*.fdb_latexmk": true,
        "**/*.synctex.gz": true,
        "**/*.nav": true,
        "**/*.snm": true,
        "**/*.toc": true,
        "*Zone.Identifier": true,
        "*/*Zone.Identifier": true
    },
    "latex-workshop.latex.outDir": "out",
    "latex-workshop.latex.tools": [
        {
            "name": "lualatex",
            "command": "lualatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-output-directory=%OUTDIR%",
                "%DOCFILE%.tex"
            ]
        },
        {
            "name": "pbibtex",
            "command": "pbibtex",
            "args": [
                "-kanji=utf8",
                "%OUTDIR%/%DOCFILE%"
            ]
        },
        {
            "name": "platex",
            "command": "wsl.exe",
            "args": [
                "platex",
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-kanji=utf8",
                "-guess-input-enc",
                "%DOCFILE%.tex"
            ]
        },
        {
            "name": "dvipdfmx",
            "command": "wsl.exe",
            "args": [
                "dvipdfmx",
                "-f",
                "yu-win10.map",
                "%DOCFILE%"
            ]
        }
    ],
    "latex-workshop.latex.recipes": [
        {
            "name": "lualatex",
            "tools": [
                "lualatex",
                "pbibtex",
                "lualatex",
                "lualatex",
            ]
        },
        {
            "name": "platex",
            "tools": [
                "platex",
                "platex",
                "dvipdfmx"
            ]
        }
    ],
}
```

## How to use?