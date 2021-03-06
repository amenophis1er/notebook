# Sublime Text 3: favorite config and plugins

### Config
+ Highlight current line: add to User settings: `"highlight_line": true`
+ Auto-pair backtits: Add to User Key Bindings (Parameters > Key Bindings)
```JS
    {
        "keys":
        [
            "`"
        ],
        "command": "insert_snippet",
        "args":
        {
            "contents": "`$0`"
        },
        "context":
        [
            {
                "key": "setting.auto_match_enabled",
                "operator": "equal",
                "operand": true
            },
            {
                "key": "selection_empty",
                "operator": "equal",
                "operand": true,
                "match_all": true
            },
            {
                "key": "following_text",
                "operator": "regex_contains",
                "operand": "^(?:\t| |\\)|]|\\}|>|$)",
                "match_all": true
            },
            {
                "key": "preceding_text",
                "operator": "not_regex_contains",
                "operand": "[`a-zA-Z0-9_]$",
                "match_all": true
            },
            {
                "key": "eol_selector",
                "operator": "not_equal",
                "operand": "string.quoted.single",
                "match_all": true
            }
        ]
    },
    {
        "keys":
        [
            "`"
        ],
        "command": "insert_snippet",
        "args":
        {
            "contents": "`${0:$SELECTION}`"
        },
        "context":
        [
            {
                "key": "setting.auto_match_enabled",
                "operator": "equal",
                "operand": true
            },
            {
                "key": "selection_empty",
                "operator": "equal",
                "operand": false,
                "match_all": true
            }
        ]
    },
    {
        "keys":
        [
            "`"
        ],
        "command": "move",
        "args":
        {
            "by": "characters",
            "forward": true
        },
        "context":
        [
            {
                "key": "setting.auto_match_enabled",
                "operator": "equal",
                "operand": true
            },
            {
                "key": "selection_empty",
                "operator": "equal",
                "operand": true,
                "match_all": true
            },
            {
                "key": "following_text",
                "operator": "regex_contains",
                "operand": "^`",
                "match_all": true
            }
        ]
    },
    {
        "keys":
        [
            "backspace"
        ],
        "command": "run_macro_file",
        "args":
        {
            "file": "res://Packages/Default/Delete Left Right.sublime-macro"
        },
        "context":
        [
            {
                "key": "setting.auto_match_enabled",
                "operator": "equal",
                "operand": true
            },
            {
                "key": "selection_empty",
                "operator": "equal",
                "operand": true,
                "match_all": true
            },
            {
                "key": "preceding_text",
                "operator": "regex_contains",
                "operand": "`$",
                "match_all": true
            },
            {
                "key": "following_text",
                "operator": "regex_contains",
                "operand": "^`",
                "match_all": true
            }
        ]
    },
```

### Plugins


### Themes

