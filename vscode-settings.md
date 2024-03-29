# My vscode settings


### Extensions

`Bracket Pair Colorizer` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer)

`Code Runner` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)

`Docker` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)

`ESLint` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

`Laravel Blade Snippets` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=onecentlin.laravel-blade)

`Laravel Blade Spacer` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=austenc.laravel-blade-spacer)

`Laravel Snippets` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=onecentlin.laravel5-snippets)

`Material Icon Theme` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)

`Live Server` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)

`PHP Intelephense` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=bmewburn.vscode-intelephense-client)

`Project Manager` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)

`Vetur` [Link &rarr;](https://marketplace.visualstudio.com/items?itemName=octref.vetur)

### Settings

```
{
    "[blade]": {
        "editor.tabSize": 2,
        "editor.autoClosingBrackets": "always"
    },
    "[javascript]": {
        "editor.tabSize": 2,
    },
    "[php]": {
        "editor.tabSize": 4,
        "editor.formatOnSave": true
    },
    "[python]": {
        "editor.tabSize": 4
    },
    "[vue]": {
        "editor.tabSize": 2,
    },
    "editor.fontSize": 16,
    "editor.renderWhitespace": "boundary",
    "editor.tabSize": 2,
    "editor.wordWrap": "on",
    "files.associations": { "*.module": "php" },
    "files.insertFinalNewline": true,
    "files.trimTrailingWhitespace": true,
    "search.exclude": {
        "**/bower_components": true,
        "**/dist": true,
        "**/frontend/public": true,
        "**/.git": true,
        "**/node_modules": true,
        "**/public": true,
        "**/storage": true,
        "**/vendor": true,
        "package-lock.json": true
    },
    "telemetry.enableTelemetry": false,
    "css.validate": false,
    "less.validate": false,
    "scss.validate": false,
    "window.zoomLevel": -1,
    "workbench.enableExperiments": false,
    "telemetry.enableCrashReporter": false,
    "extensions.autoUpdate": false,
    "workbench.startupEditor": "newUntitledFile",
    "emmet.triggerExpansionOnTab": true,
    "blade.format.enable": true,
    "workbench.iconTheme": "material-icon-theme",
    "security.workspace.trust.untrustedFiles": "open",
    "intelephense.environment.phpVersion": "7.4"
}

```
