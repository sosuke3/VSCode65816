# Visual Studio Code (xkas) 65816 assembly syntax highlighting extension

This is an extension for Visual Studio Code to add syntax highlighting support for xkas style 65816 assembly.

## Extension Settings

The following scopes are defined and can have custom coloring and styling applied (see suggestion below):
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
string.sublabel
string.sublabel.reference
string.quoted.double
string.quoted.single
```

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
                    "foreground": "#FF9300",
                    "fontStyle": "bold italic"
                }
            },
            {
                "scope": "string.sublabel",
                "settings": {
                    "foreground": "#FF9300",
                    "fontStyle": "bold"
                }
            },
            {
                "scope": "string.label",
                "settings": {
                    "foreground": "#FF9300",
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

Only sublabel highlighting is availble for jump instructions. Normal labels will be highlighted where defined only. This will be resolved shortly.