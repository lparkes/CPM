This program patches Infocom iteractive fiction programs (the .COM
files) to output Xterm compatible control sequences for a window that
is 80x24.

This will likely work for any modern terminal program.

This program also patches the .COM to look for a game file that has
the same name as the .COM file, but with a .DAT extension. Not all
Infocom games were shipped this way and you may need to rename your
.DAT file to match the name of your .COM file.

Building xterm.com
------------------

The xterm is distributed as source code that can be assembled with
ZSM4 or the Microsoft Macro-80 assembler. You can create xterm.com
with any of the following three sets of commands.

```
zsm4 xterm
```

or

```
m80 =xterm.z80
l80 xterm,xterm/n/e
```

or

```
m80 =xterm.z80
link xterm
```

Usage
-----

To patch Zork 1 with the control sequences for Xterm you would run the
following. You only need to run it once per .COM file of course.

```
xterm zork1.com
```

To patch The Hitchhiker's Guide to the Galaxy you would need to do one
of the following.

```
xterm hitch.com
ren hitch.dat = hitchhik.dat
```

or

```
ren hitchhik.com = hitch.com
xterm hitchhik.com
```

