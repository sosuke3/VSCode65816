# Visual Studio Code (xkas) 65816 assembly syntax highlighting extension

This is an extension for Visual Studio Code to add syntax highlighting support for xkas style 65816 assembly. Original tmLanguage file was lifted from [https://github.com/DanielOaks/65816-Assembly-TMlanguage](https://github.com/DanielOaks/65816-Assembly-TMlanguage). I have fixed some bugs in it and added xkas syntax specific highlighting.

Since this is just a .tmLanguage file it should work fine in textmate and other editors that support textmate markup files.

## Installation

### Manual Installation

Copy the files to a new folder in your vscode extensions directory (I recommend ```65816-assembly```). See Microsoft's documentation [https://code.visualstudio.com/docs/extensions/yocode#_your-extensions-folder](https://code.visualstudio.com/docs/extensions/yocode#_your-extensions-folder) for platform specific locations.

## Extension Settings

The following scopes are defined and can have custom coloring and styling applied (see suggestion below). You can set these in your User Configuation using the ```editor.tokenColorCustomization``` setting added in vscode 1.15.0:
```
comment.line
command.concatenate
keyword.snes
keyword.xkas.define
keyword.mnemonic
keyword.asm
storage.register
constant.numeric.asm
constant.numeric.dec
string.label
string.label.reference
string.sublabel
string.sublabel.reference
string.quoted.double
string.quoted.single
```

Note that some of the names are default names used for syntax highlighting all languages, if this is a problem please open an issue and I will change them.

I suggest you add the following to your User Settings file for some initial sane highlighting:

```
    "editor.tokenColorCustomizations":{
        "textMateRules": [
            {
                "scope": "constant.numeric.asm",
                "settings": {
                    "foreground": "#000000"
                }
            },
            {
                "scope": "string.sublabel.reference",
                "settings": {
                    "foreground": "#FFAC3D",
                    "fontStyle": "italic"
                }
            },
            {
                "scope": "string.sublabel",
                "settings": {
                    "foreground": "#FFAC3D",
                    "fontStyle": "bold"
                }
            },
            {
                "scope": "string.label.reference",
                "settings": {
                    "foreground": "#A40000",
                    "fontStyle": "italic"
                }
            },
            {
                "scope": "string.label",
                "settings": {
                    "foreground": "#A40000",
                    "fontStyle": "bold"
                }
            },
            {
                "scope": "keyword.xkas.define",
                "settings": {
                    //"foreground": "#AA5E07",
                    "fontStyle": "bold"
                }
            }
        ]
    }
```


## Known Issues

None at the moment.