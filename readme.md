--- compose for tmux

I need a compose key in tmux.

Thank you that is all.

  run with:

```
tmux bind C-y command-prompt -p compose "if '[pathto]python [pathto]compose.py \\%% | tmux load-buffer -' 'pasteb -d' 'display digraph not found'" 
```
(where python is a path to python, and the pathto the script is ... specified properly.)

Can obviously be stuck in your tmux.conf
python 3.