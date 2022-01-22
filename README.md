# Echoes
```
+---------+
|  e   c  |
+---------+
     h
+---------+
|         |
|    o    |
+---------+
   e   s   
```

Makes Markdown interactive

## KEY BiNDiNG

* `ESC` switch prompt
* `ctrl/cmd+ENTER`   transmit selection
* `ctrl/cmd+n`       new buffer
* `ctrl/cmd+shift+n` new window
* `ctrl/cmd+i`       transfer focus to the prompt
* `ctrl/cmd+shift+i` transfer focus to the prompt and copy selection
* `ctrl/cmd+s`       save buffer
* `ctrl/cmd+p`       polish output
* `ctrl/cmd+l`       switch layout
* `ctrl/cmd+b`       print bookmarks
* `ctrl/cmd+u`       print units
* `ctrl/cmd+t`       print threads
* `ctrl/cmd+f`       find text
* `ctrl/cmd+r`       replace text

## CLI options

* `<path> :nb` new bookmark
* `<path> :nd` create new directory
* `<path> :nf` create new file
* `<path> :d` delete directory or file
* `<path> :w` write buffer to file
* `<echo file> :up` scan and cache units

## Declarative system language

**put in cache**
```
@var <alias> {
  <value>
}
```

**ask for input**
```
@arg <alias> {
	<label>
}
```

**execute command (single line format)**
```
@cmd <os-command>
or
@cmd (<path>) <os-command>
```

**cache a command (multi line format)**
```
@cmd <alias> {
  <os-command>
}
or
@cmd <alias> (<path>) {
  <os-command>
}
```

**execute command without terminal (multi line format)**
```
@run <os-command>
or
@run (<path>) <os-command>
```

**execute command without terminal (multi line format)**
```
@run <alias> {
  <replace with os-command>
}
or
@run <alias> (<path>) {
  <replace with os-command>
}
```

**perform a cached unit (@cmd or @run)**
```
@use $<verb>.<alias>
```

**print cached unit (@arg or @var)**
```
@ink (<#color>) <value>
```

**print text or cached unit (@arg or @var) using default color**
```
@ink <value>
```

**placeholder**
```
$<verb>.<alias> or ${<verb>.<alias>}
```

**special placeholders**
```
$path.user replace with user's home (like ~)
$path.wdir replace with current working directory
```

> * select and press ctrl/cmd+ENTER to transmite
> * use alias to cache units
> * use upper case Alias to store permanently

## CLI

**search text**
```
:f<delimiter><search>

*example*
:f|hello echoes
```

**search text and replace**
```
:f<delimiter><search><delimiter>:r<delimiter><new><delimiter>

*example*
:f|hello echoes|:r|hello nickyb
```

**search text and replace in a range**
```
:f<delimiter><search><delimiter>:r<delimiter><new><delimiter>:l<delimiter><start-line>..<end-line>

*example*
:f|hello echoes|:r|hello nickyb|:l|10..15
or
:f|hello echoes|:r|hello nickyb|:l|10..
or
:f|hello echoes|:r|hello nickyb|:l|..15
```

### Examples
[Git Cheat Sheet](./cheat-sheets/git.echo?ts=2)
