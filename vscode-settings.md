# My vscode settings


### Extensions

`ESLint` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

`Laravel 5 Snippets` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=onecentlin.laravel5-snippets)

`Laravel Blade Snippets` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=onecentlin.laravel-blade)

`Laravel goto view` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=codingyu.laravel-goto-view)

`PHP Intelephense` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=bmewburn.vscode-intelephense-client)

`phpfmt - PHP formatter` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=kokororin.vscode-phpfmt)

`Project Manager` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)

`Vetur` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=octref.vetur)

### Settings

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
        "editor.formatOnSave": true,
    },
    "[python]": {
        "editor.tabSize": 4
    },
    "[vue]": {
        "editor.tabSize": 2
    },
    "editor.formatOnSave": false,
    "editor.fontSize": 16,
    "editor.renderWhitespace": "boundary",
    "editor.tabSize": 2,
    "editor.wordWrap": "on",
    "files.eol": "\n",
    "search.exclude": {
        "**/bower_components": true,
        "**/dist": true,
        "**/frontend/public": true,
        "**/node_modules": true,
        "**/public": true,
        "**/vendor": true
    },
    "telemetry.enableTelemetry": false,
    "css.validate": false,
    "scss.validate": false,
    "less.validate": false,
    "eslint.validate": [
        {
            "language": "vue",
            "autoFix": true
        },
        {
            "language": "javascript",
            "autoFix": true
        }
    ],
    "window.zoomLevel": -1,
    "terminal.integrated.shell.windows": "D:\\Program Files\\Git\\bin\\bash.exe",
    "workbench.enableExperiments": false,
    "update.showReleaseNotes": false,
    "telemetry.enableCrashReporter": false,
    "editor.codeLens": false
}
```
