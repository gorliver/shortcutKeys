# frequently used shortcuts in vim

## Cursor movement

```
h             move cursor to left
l             move cursor to right
k             move cursor to up
j             move cursor to down      
```

```
ctrl-u        half-page up
ctrl-d        half-page down
H             move to first line
M             move to middle of current page
L             move to last line
zz            center current line
```

```
$             move cursor to end of the line
^             move cursor to head of the line
w, 5w         move cursor to right(5) word(s)
b, 5b         move cursor to left(5) word(s)
e, 5e         move cursor to the end of right(5) word(s)
{,}           jump backward/forward one paragraph
f,F+char      jump forward/backward to next char, cursor will be on the char
t,T+char      jump forward/backward to next char, cursor will be before the char
''            return to the line where the cursor was before the latest jump
```

## Text operation

### Deletion
```
x             delete one character
dw, d5w       delete forward to the end of the (5) word(s)
diw           delete current word
db,d5b        delete backward to the head of the (5) word(s)
d$            delete to the end of the line
d^            delete to the head of the line
```
### yank and paste
```
yy            yank current line
va}+y         select current block and yank
y$            yank to the end of the line
yw            yank to the end of the word
p             paste
P             paste above current line
```
### Edit
```
a             insert after
i             insert
r             replace
u             undo
J             merge next line to current line
o             insert new line
O             insert new line before current line
.             repeat last operation
```

## file operation
```
:e f.txt      open and edit f.txt
:r f.txt      append f.txt to current file
```
## search and replace
```
:/            search forward
:?            search backward
:%s/p1/p2/g   replace p1 by p2
```
## Folding
Fold by indent:
In vim, set foldmethod to indent:
```
:setlocal foldmethod=indent
```
```
zi            switch folding on or off
za            toggle current fold open/closed
zc            close current fold
zR            open all folds
zM            close all folds
zv            expand folds to reveal cursor
```
Manual fold:
Set foldmethod to manual:
```
:setlocal foldmethod=manual
```
```
zf10j        fold next 10 lines
zfa}         fold to next }
v+zf         use v to select lines and then zf
```
