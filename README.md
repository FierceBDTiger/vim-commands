# VIM Editor Commands
[![N|Solid](https://vim.sourceforge.io/images/vim_header.gif)](https://vim.sourceforge.io/)
Vim is an editor to create or edit a text file.
There are two modes in vim. One is the command mode and another is the insert mode.
In the command mode, user can move around the file, delete text, etc.
In the insert mode, user can insert text.
## Changing mode from one to another
> From command mode to insert mode	type `a/A/i/I/o/O` ( see details below)
> From insert mode to command mode	type `Esc` (escape key)
#### Text Entry Commands (Used to start text entry)
```sh
a Append text following current cursor position
```
```sh
A Append text to the end of current line
```
```sh
i Insert text before the current cursor position
```
```sh
I Insert text at the beginning of the cursor line
```
```sh
o Open up a new line following the current line and add text there
```
```sh
O Open up a new line in front of the current line and add text there
```
*The following commands are used only in the commands mode.*
### Cursor Movement Commands
```sh
h Moves the cursor one character to the left
```
```sh
l Moves the cursor one character to the right
```
```sh
k Moves the cursor up one line
```
```sh
j Moves the cursor down one line
```
```sh
nG or :n Cursor goes to the specified (n) line
(ex. 10G goes to line 10)
```
```sh
^F (CTRl F) Forward screenful
```
```sh
^B Backward screenful
```
```sh
^f One page forward
```
```sh
^b One page backward
```
```sh
^U Up half screenful
```
```sh
^D Down half screenful
```
```sh
$ Move cursor to the end of current line
```
```sh
0 (zero) Move cursor to the beginning of current line
```
```sh
w Forward one word
```
```sh
b Backward one word
```
### Exit Commands
```sh
:wq Write file to disk and quit the editor
```
```sh
:q! Quit (no warning)
```
```sh
:q Quit (a warning is printed if a modified file has not been saved)
```
```sh
ZZ Save workspace and quit the editor (same as :wq)
```
```sh
: 10,25 w temp
write lines 10 through 25 into file named temp. Of course, other line numbers can be used. (Use :f to find out the line numbers you want.
```
### Text Deletion Commands
```sh
x Delete character
```
```sh
dw Delete word from cursor on
```
```sh
db Delete word backward
```
```sh
dd Delete line
```
```sh
d$ Delete to end of line
```
```sh
d^ (d caret, not CTRL d) Delete to beginning of line
```
##### Yank (has most of the options of delete)-- VI's copy commmand
```sh
yy yank current line
```
```sh
y$ yank to end of current line from cursor
```
```sh
yw yank from cursor to end of current word
```
```sh
5yy yank, for example, 5 lines
```
##### Paste (used after delete or yank to recover lines.)
```sh
p paste below cursor
```
```sh
P paste above cursor
```
```sh
"2p paste from buffer 2 (there are 9)
```
```sh
u Undo last change
```
```sh
U Restore line
```
```sh
J Join next line down to the end of the current line
```
### File Manipulation Commands
```sh
:w Write workspace to original file
```
```sh
:w file Write workspace to named file
```
```sh
:e file Start editing a new file
```
```sh
:r file Read contents of a file to the workspace
```
```sh
To create a page break, while in the insert mode, press the CTRL key
And l. ^L will appear in your text and will cause the printer to start
A new page.
```
### Other Useful Commands
Most commands can be repeated n times by typing a number, n, before the command. For example `10dd` means delete 10 lines.
```sh
. Repeat last command
```
```sh
cw Change current word to a new word
```
```sh
r Replace one character at the cursor position
```
```sh
R Begin overstrike or replace mode use ESC key to exit
```
```sh
:/ pattern Search forward for the pattern
```
```sh
:? pattern Search backward for the pattern
```
```sh
n (used after either of the 2 search commands above to
continue to find next occurrence of the pattern.
```
```sh
:g/pat1/s//pat2/g replace every occurrence of pattern1 (pat1) with pat2
```
###### Example
```sh
:g/tIO/s//Ada.Text_IO/g
This will find and replace tIO by Ada.text_IO everywhere in the file.
:g/a/s// /g replace the letter a, by blank
:g/a/s///g replace a by nothing
note: Even this command be undone by u
```
## Examples
#### Opening a New File
`Step 1` type	vim filename	(create a file named filename)

`Step 2` type	i	( switch to insert mode)

`Step 3` enter text	(enter your Ada program)

`Step 4` hit	Esc key	(switch back to command mode)

`Step 5` type	:wq	(write file and exit vim)

#### Editing the Existing File
`Step 1` type	vim filename	(edit the existing file named filename)

`Step 2` move around the file using `h/j/k/l` key or any appropriate command

```sh
h Moves the cursor one character to the left
l Moves the cursor one character to the right
k Moves the cursor up one line
j Moves the cursor down one line
nG or :n Cursor goes to the specified (n) line
(ex. 10G goes to line 10)
```

`Step 3` edit required text (replace or delete or insert)

`Step 4` hit Esc key (exit from insert mode if you insert or replace text)

`Step 5` type	:wq
