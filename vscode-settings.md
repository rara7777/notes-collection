# My vscode settings


### Extensions

`ESLint` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

`Laravel 5 Snippets` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=onecentlin.laravel5-snippets)

`Laravel Blade Snippets` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=onecentlin.laravel-blade)

`phpfmt - PHP formatter` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=kokororin.vscode-phpfmt)

`Project Manager` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)

`Vetur` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=octref.vetur)

### Settings

If you want your editor to work and look exactly the same way as mine does in the course videos, you can copy these settings to your own settings file. Just go to settings in VSCode, and on the right side, you can paste this code.

```
{
    "[blade]": {
        "editor.tabSize": 2
    },
    "[javascript]": {
        "editor.tabSize": 2
    },
    "[php]": {
        "editor.tabSize": 4,
        "editor.formatOnSave": true
    },
    "[vue]": {
        "editor.tabSize": 2
    },
    "[python]": {
        "editor.tabSize": 4
    },
    "editor.tabSize": 2,
    "editor.fontSize": 16,
    "window.zoomLevel": -1,
    "workbench.startupEditor": "newUntitledFile",
    "search.exclude": {
        "**/bower_components": true,
        "**/dist": true,
        "**/frontend/public": true,
        "**/node_modules": true,
        "**/public": true,
        "**/vendor": true
    },
    "editor.renderWhitespace": "boundary",
    "editor.codeLens": true,
    "editor.snippetSuggestions": "top",
    "git.ignoreMissingGitWarning": true,
    "explorer.confirmDragAndDrop": false,
    "editor.quickSuggestions": {
        "other": false,
        "comments": false,
        "strings": false
    },
    "emmet.includeLanguages": {
        "blade": "html"
    },
    "emmet.triggerExpansionOnTab": true, // enable tab to expanse emmet tags
    "telemetry.enableTelemetry": false,
    "workbench.colorCustomizations": {
        "statusBar.background": "#333333",
        "statusBar.noFolderBackground": "#333333",
        "statusBar.debuggingBackground": "#263238"
    },
    "css.validate": false,
    "scss.validate": false,
    "less.validate": false,
    "editor.wordWrap": "on",
    "blade.format.enable": true,
    "vetur.validation.template": false,
    "extensions.ignoreRecommendations": true,
    "files.eol": "\n",
    "phpfmt.php_bin": "\"D:\\XAMPP\\php\\php.exe\"",
    "eslint.validate": [
        {
            "language": "vue",
            "autoFix": true
        },
        {
            "language": "javascript",
            "autoFix": true
        }
    ]
}
```
