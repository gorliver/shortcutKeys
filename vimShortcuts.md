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
H             move to first line on current page
M             move to middle of current page
L             move to last line on current page
zz            center current line
gg            move to the head of the file
#G,#gg        goto # line
G             move to the tail of the file
%             jump between {},()... 
```

```
$             move cursor to end of the line
^             move cursor to first non-blank character the line
0             move cursor to start of the line
w, 5w         move cursor to right(5) word(s)
b, 5b         move cursor to left(5) word(s)
e, 5e         move cursor to the end of right(5) word(s)
{,}           jump backward/forward one paragraph
[{, ]}        jump to { or } when cursor in a code block (defined by {}) 
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
di(           delete the context within the block (defined by (),{}, [],"" ...)
ci(           delete the context within the block (defined by (),{}, [],"" ...) and then enter insert mode
db,d5b        delete backward to the head of the (5) word(s)
d$            delete to the end of the line
d^            delete to the head of the line
```
### yank and paste
```
v             start visual mode
V             start visual mode line-wise
ctrl-v        start visual mode block-wise
yy            yank current line
va}y          select current block(defined by {}) and yank
y$            yank to the end of the line
yw            yank to the end of the word
p             paste
P             paste above current line
```
### Edit
```
a             insert after (append)
i             insert
c             change (delete then enter edit mode)
ciw           change current words
r             replace
u             undo
ctrl-r        redo
J             merge next line to current line
o             insert new line
O             insert new line before current line
.             repeat last operation
```

### search and replace
```
:/            search forward
:?            search backward
:%s/p1/p2/g   replace p1 by p2
cgn           search next match and change it. This works nicely with `.`
```

### recording for repeat operation
Hit `q` and `a-z` to start recording.

Hit `q` again to stop recording.

Hit `@` + `a-z` or `@@` to apply the recorded operation on current line.

When recording, avoid use `hjkl` because each line is in different length. Using `w`,`e`,`b`,`$` and `^` instead.

Use `:+10` or `:-10` to jump down/up 10 lines. Then hit `@:` to repeat previous operation. This works great with `@a`

## file operation
```
:e f.txt      open and edit f.txt
:r f.txt      append f.txt to current file
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
