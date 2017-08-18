# Visual Studio Code (xkas) 65816 assembly syntax highlighting extension

This is an extension for Visual Studio Code to add syntax highlighting support for xkas style 65816 assembly. Original tmLanguage file was lifted from [https://github.com/DanielOaks/65816-Assembly-TMlanguage](https://github.com/DanielOaks/65816-Assembly-TMlanguage). I have fixed some bugs in it and added xkas syntax specific highlighting.

Since this is just a .tmLanguage file it should work fine in textmate and other editors that support textmate markup files.

## Installation

### Visual Studio Code Extension Marketplace
You can find this extension on the marketplace by searching for ```65816 Assembly```

### Manual Installation

Copy the files to a new folder in your vscode extensions directory (I recommend ```65816-assembly```). See Microsoft's documentation [https://code.visualstudio.com/docs/extensions/yocode#_your-extensions-folder](https://code.visualstudio.com/docs/extensions/yocode#_your-extensions-folder) for platform specific locations.

## Extension Settings

The following scopes are defined and can have custom coloring and styling applied (see suggestion below). You can set these in your User Configuation using the ```editor.tokenColorCustomization``` setting added in vscode 1.15.0:
```
keyword.xkas.command.concatenate
keyword.xkas.snes
keyword.xkas.define
label.xkas.label.reference
label.xkas.sublabel.reference
keyword.xkas.asm
variable.xkas.storage.register
constant.xkas.numeric.hexvalue
constant.xkas.numeric.decvalue
constant.xkas.numeric.binvalue
constant.xkas.numeric.address
label.xkas.label
label.xkas.sublabel
```

The following are also used, but changing them will impact other languages:
```
comment.line
keyword.mnemonic
string.quoted.double
string.quoted.single
```

Note that some of the names are default names used for syntax highlighting all languages, if this is a problem please open an issue and I will change them.

I suggest you add the following to your User Settings file for some initial sane highlighting:

```
    "editor.tokenColorCustomizations":{
        "textMateRules": [
            {
                "scope": "keyword.xkas.command.concatenate",
                "settings": {
                    "foreground": "#848484"
                }
            },
            {
                "scope": "keyword.xkas.snes",
                "settings": {
                    "foreground": "#0000FF"
                }
            },
            {
                "scope": "keyword.xkas.asm",
                "settings": {
                    "foreground": "#0000FF"
                }
            },
            {
                "scope": "keyword.xkas.define",
                "settings": {
                    "foreground": "#0000FF"
                }
            },
            {
                "scope": "constant.xkas.numeric.hexvalue",
                "settings": {
                    "foreground": "#0000B6"
                }
            },
            {
                "scope": "constant.xkas.numeric.decvalue",
                "settings": {
                    "foreground": "#000000"
                }
            },
            {
                "scope": "constant.xkas.numeric.binvalue",
                "settings": {
                    "foreground": "#8C0909"
                }
            },
            {
                "scope": "constant.xkas.numeric.address",
                "settings": {
                    "foreground": "#9811DD"
                }
            },
            {
                "scope": "label.xkas.sublabel.reference",
                "settings": {
                    "foreground": "#FFAC3D",
                    "fontStyle": "italic"
                }
            },
            {
                "scope": "label.xkas.sublabel",
                "settings": {
                    "foreground": "#FFAC3D",
                    "fontStyle": "bold"
                }
            },
            {
                "scope": "label.xkas.label.reference",
                "settings": {
                    "foreground": "#A40000",
                    "fontStyle": "italic"
                }
            },
            {
                "scope": "label.xkas.label",
                "settings": {
                    "foreground": "#A40000",
                    "fontStyle": "bold"
                }
            },
            {
                "scope": "variable.xkas.storage.register",
                "settings": {
                    "foreground": "#3CB3FD"
                }
            }
        ]
    }
```


## Known Issues

None at the moment.