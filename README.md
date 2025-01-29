# pcl README

This is the README for a VSCode extension that adds syntax highlighting to the PPCL language.

## Features
Adds syntax highlighting to VS Code for PPCL

## Extension Settings
Syntax highlighting relies on your settings already having some colors defined for the scopes [keyword.operator, keyword.control, constant.numeric, string.quoted.double, comment.block]. If you do not have these scopes defined then you will have to add them to your settings manually. Do this by

1. Open User Settings:
Press Ctrl+, to open the settings.
Click on the {} icon in the top right corner to open the settings JSON file.

2. Add Custom Color:
Add the following JSON to customize the color for the keyword.operator scope:
```json
"editor.tokenColorCustomizations": {
    "textMateRules": [
        {
            "scope": "keyword.operator",
            "settings": {
                "foreground": "#FF0000"  // Replace with your desired color
            }
        }
    ]
}
```

## Known Issues
Numeric constant highlighting does not work. I think the textmate software uses a slightly different regex syntax than the tester I was using. It seems like textmate doesn't recognize word boundaries \b the same way as the tester I was using.
