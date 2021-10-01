# The `clear` command

`clear` command is used to clear the terminal window.

### Example:
```
clear
```

### Syntax
```
clear [OPTION]
```

### Flags and their functionalities:
|**Flag**|**Description**|
|:---|:---|
|`-V`|print curses-version|
|`-x`|do not clear scrollback (can also be done using ctrl+l)|
|`-T`|Indicates the type of terminal, Usually, this option is unnecessary, because the default is taken from the environment variable **TERM**, but if `-T` is specified, then the shell variable **LINES** and **COLUMNS** will also be ignored|

If the `clear` command is used without flags, it also clear scrollback.
