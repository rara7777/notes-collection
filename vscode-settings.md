# My vscode settings


### Extensions

`ESLint` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

`Laravel 5 Snippets` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=onecentlin.laravel5-snippets)

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
    "[python]": {
        "editor.tabSize": 4
    },
    "[vue]": {
        "editor.tabSize": 2
    },
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
    ],
    "window.zoomLevel": -1
}
```
