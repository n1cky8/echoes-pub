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
* `ctrl/cmd+i` prompt focus and copy selection
* `ctrl/cmd+s` save buffer
* `ctrl/cmd+p` polish output
* `ctrl/cmd+l` switch layout
* `ctrl/cmd+b` print bookmarks
* `ctrl/cmd+u` print units
* `ctrl/cmd+t` print threads

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
