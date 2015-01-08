--- compose for tmux

I need a compose key in tmux.

Thank you that is all.

  run with:

```
tmux bind C-v command-prompt -p compose "if '[pathto]python [pathto]compose.py \\%% | tmux load-buffer -' 'pasteb -d' 'display digraph not found'" 
```
(where python is a path to python, and the pathto the script is ... specified properly.)

Can obviously be stuck in your tmux.conf
python 3.  - I think I made it work in python2 as well, by doing the 'from future' bit.

- additional notes, now that I put this on github publicly:
 * uses the X11 compose data. This is probably in a different spot on osX, and may not exist. If someone needs it, I suppose I can add it somehow.
 * certain characters are strings: 'cur' for 'currency' key, as I don't have a currency key, and $ is problematic.
 * certain things need a shell escape (as we're passing this through the shell.) ( and ) are two of them.
 * this can be tested from the command line to see wtf is causing the compose to not work. (chances are: it's an escape you're missing.)
 * this works, but it's not fantastic code.  If folks want to see it shaped up, I may work on it more. Patches welcome.

I've used this for nearly 3 weeks now and ... I don't need screen any longer for _anything._
