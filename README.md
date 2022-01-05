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

* `ESC` reset prompt
* `ctrl/cmd+ENTER` transmit selection
* `ctrl/cmd+I` prompt focus and copy selection
* `ctrl/cmd+S` save buffer
* `ctrl/cmd+P` polish output
* `ctrl/cmd+L` switch layout
* `ctrl/cmd+B` print bookmarks
* `ctrl/cmd+U` print units
* `ctrl/cmd+T` print threads

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
@var <replace with an alias> {
  <replace with path>
}
```

**execute command**
```
@cmd <replace with os-command>
```

**cache a command**
```
@cmd <replace with an alias> {
  <replace with os-command>
}
```

**execute command without terminal**
```
@run <replace with os-command>
```

**cache a command without terminal**
```
@run  <replace with an alias> {
  <replace with os-command>
}
```

> * select and press ctrl/cmd+ENTER to transmite
> * use alias to cache units
> * use upper case Alias to store permanently
