---
layout: post
title: "Emacs tutorial(One)"
date: 2020-06-24 22:30:00 +0800
---

 #  Emacs tutorial

[toc]

## The core key

> we will use the following abbreviation.

### The CONTROL key

Sometimes labeled CTRL or CTL.

* **C - \<chr\>**

  means hold the CONTROL key while typing the character \<chr\>Thus, c-f would be: hold the CONTROL key and type f.

### The META key

Sometimes labeled EDIT or ALT.

* **M - \<chr\>**

  means hold the META or EDIT or ALT key down while typing \<chr\>. IF there is no META, EDIT or ALT key, instead press and release the ESC key and then type (chr). We write (ESC) for the ESC key.

## Move viewing screen

The following commands are useful for viewing screenfuls.

* **C - v**

  Move to the forward screen.

* **M - v**   

  Move backwards one screen.

> You can also use the PageUp and PageDn keys to move by screenfuls, if your terminal has them, *but you can more efficiently if you use C-v and M-v.*

* **C - l**

  Clear screen and redisplay all the text, moving the text aroud the cursor to the center of the screen.*( That's CONTROL - L, not CONTROL -1.)*

  > Find the cursor, and note what text is near it. Then type C-l. find the cursor again and notice that the same text is still near the cursor, but now it is in the center of the screen.
  >
  > **if you press C-l again, this piece of text will move to the top of the screen. Press C-l again, and it moves to the bottom.**

##    Cursor control

The location of the cursor in the text is also called "point". To paraphrase, the cursor shows on the screen where point is located in the text.

### Cursor motion  command

* **C - f **	-->>	move cursor to next character.
* **C - b **	-->>	move cursor to previous character.
* **C - n **	-->>	move cursor to next line.
* **C - p **	-->>	move cursor to previous line.
* **M - f **	-->>	move cursor to next word.
* **M - b **	-->>	move cursor to previous word.
* **C - a **	-->>	move cursor to beginning of the line.
* **C - e **	-->>	move cursor to end of the line.
* **M - a **	-->>	move cursor back to beginning of sentence
* **M - e **	-->>	move cursor to end of sentence
* **M -< **	-->>	move cursor to the beginning of the file.
* **M - > **	-->>	move cursor to end of the file.
#### summary

#####  C-f/b/n/p Refer

You can use the arrow keys, but it's more efficient to keep your hands in the standard position and use the command C- p, C- b, C -f, and C - n. These characters are equivalent to the four arrow keys, like this:

|  |    |  previous line, C-p   |||
|:---:|:-------------:|:---:|:---:|:-------------:|
|   |            |**\|** |  ||
|**Backward, C-b**  |      **--**       | **Current cursor position** |**--**|**Forward, C -f**|
|   |             | **\|** |||
|   |             | **Nest line, C-n** |||

> Move the cursor to the line in the middle of that diagram using C-n or C-p. Then type C-l to see the whole diagram centered in the screen.

| p    | -->   |previous|
| :------:|:------:| :------: |
| **N** | **-->** | **next** |
|**B**|**-->**|**backward**|
|**F**|**-->**|**forward**|

> Each line of text ends with a Newline character, which serves to separate it from the following line. (Normally, the last line in a file will have a Newline at the end, but Emacs does not require it. )

When you move past the top or bottom of the screen, the text beyond the edge shifts the screen, then cursor viewing in the middle of screen. This is called "scrolling ", It enables Emacs to move the cursor to the specified place in the text without moving it off the screen.

#####  M-f/b Refer

When you are in the middle of a word, M-f moves to the end of the word when you are in whitespace between words, M-f moves to the end of the following word. M-b works likewise in the opposite direction.

#####  M->/< Refer

On most terminals, the "<" is above the comma key, so you must use the shift key to type it. On these terminals you must use the shift key to type M-< also; without the shift key, you would be typing-comma.

* If you use **M-<** command then use **C-v** repeatedly to move back here and cursor is viewing beginning line and first character of the screen.

* If you use **M->** command then use **M -v** repeatedly to move back here. cursor is viewing of the screen tail line first character.

##  Prefix argument

> If you have a META (or EDIT or ALT) key, alternative way to enter a numeric argument: type the digits while holding down the META key( the META key in keyboard upper left corner).

The numeric argument is also called a "prefix argument", because you type the argument before the command it applies to. Most Emacs commands accept a numeric argument, this serves as a repeat-count. .

### **command: C-u**

Several commands use it as a flag--the presence of a prefix argument, regardless of its value, makes the command do something different.

* C-v and M-v are another kind of exception. When given an argument, they scroll the text up or down that many lines, rather than by a screenful.

##  Stops responding

###  command

*  **C - g**

### refer

* If emacs stops responding to you commands; you can stop it safely. Use it to stop a command which is taking too long to execute.

* Use it to discard a  numeric argument or the beginning of a command that you do not want to finish. 

* If you have typed an \<esc\> by mistake, you can get rid of it with a C-g.

##  Disabled commands

Some emacs commands are "disabled" so that beginning users cannot use them by accident. If type one of the disabled commands, emacs displays a message saying what the command was, and asking you whether you want to go ahead and execute the command,because new_use may be don't need this command.

##  Windows

> Emacs can have several "windows", each displaying its own text.

* C-X 1						--->	 	One window( kill all other windows).
* C-h k "*command*"	--->		display  the "*command* meaning to a new windows." 

There is a whole series of commands that start with CONTROL-x; many of them have to do with windows, files, buffers,and related things.

These commands are two, three or four characters long.

##  Inserting and deleting








​			



