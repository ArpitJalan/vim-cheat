# Vim cheatsheet

### Contents
1. [Text Manipulation](#text-manipulation)
2. [Moving around](#moving-around)
3. [Indentation](#text-indentation)

----

## Text manipulation
```de``` - Delete everything till the end of the word by pressing . at your heart's desire.

```ci(xyz[Esc]``` - This is a weird one. Here, the 'i' does not mean insert mode. Instead it means inside the parenthesis. So this sequence cuts the text inside parenthesis you're standing in and replaces it with "xyz". It also works inside square and figure brackets -- just do ci[ or ci{ correspondingly. Naturally, you can do di (if you just want to delete all text without typing anything. You can also do a instead of i if you want to delete the parentheses as well and not just text inside them.

```ci"``` - cuts the text in current quotes

```ciw``` - cuts the current word. This works just like the previous one except that ( is replaced with w.

```C``` - cut the rest of the line and switch to insert mode.

```ZZ``` - save and close current file (WAY faster than Ctrl-F4 to close the current tab!)

```U``` - uppercase, so viwU upercases the word

```~``` - switches case, so viw~ will reverse casing of entire word

```de``` - delete from cursor to the end of the word (you can also do dE to delete until the next space)

```bde``` - delete the current word, from left to right delimiter

```df[space]``` - delete up until and including the next space

```dt.``` - delete until next dot

```dd``` - delete this entire line

```capital D``` - (take a deep breath) Deletes the rest of the line to the right of the cursor, same as Shift+End/Del in normal editors (notice 2 keypresses - Shift+D -- instead of 3)

```:! [command]``` - executes an external command while you're in vim.

But add a dot after the colon - :.! [command] -- and it'll dump the output of the command into your current window. That's : . ! 

```diw``` - to delete the current word

```di(``` - to delete within the current parens

```di"``` - to delete the text between the quotes

```dab``` - "delete arounb brackets"

```daB``` for around curly brackets, t for xml type tags, combinations with normal commands are as expected cib/yaB/dit/vat etc

## Moving around

```ddp``` - move current line one row down

```xp``` - move current character one position to the right

```zz``` - it scrolls the screen to make this line appear in the middle. This is excellent for putting the piece of code you're working on in the center of your attention. Sibling commands -- zt and zb -- make this line the top or the bottom one on the sreen which is not quite as useful.

```%``` finds and jumps to the matching parenthesis.

```ye (or yE)``` - yanks text from here to the end of the word

```ce``` - cuts through the end of the word

```bye``` - copies current word (makes me wonder what "hi" does!)

```yy``` - copies the current line

```cc``` - cuts the current line, you can also do S instead. There's also lower cap s which cuts current character and switches to insert mode.

```viwy or viwc.``` Yank or change current word. Hit w multiple times to keep selecting each subsequent word, use b to move backwards

```vi{``` - select all text in figure brackets. va{ - select all text including {}s

```vi(p``` - highlight everything inside the ()s and replace with the pasted text

```b and e``` move the cursor word-by-word, similarly to how Ctrl+Arrows normally do. The definition of word is a little different though, as several consecutive delmiters are treated as one word. If you start at the middle of a word, pressing b will always get you to the beginning of the current word, and each consecutive b will jump to the beginning of the next word. Similarly, and easy to remember, e gets the cursor to the end of the current, and each subsequent, word.

similar to b/e, capital B and E move the cursor word-by-word using only whitespaces as delimiters.

## Indentation

```=i{``` - automatically indents inside the block of code your curson currently is.

```=%``` - automatically indents when over a curly brackets { or }

```>> or <<``` - moves the text one tab right or left respectively, then repeat using ```.``` as many times as you want
