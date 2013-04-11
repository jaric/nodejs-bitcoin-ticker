
## What does it do?

This is a script you could use to display realtime bitcoin exchange rate in your tmux status line

## How to use it?

add following to your tmux confi (assuming ~/.tmux.conf)

```
set -g status-fg green
set -g status-bg black
set -g status-attr bright
set-window-option -g window-status-current-bg green
set-window-option -g window-status-current-fg black
set-window-option -g window-status-current-attr dim
set -g status-right '#[fg=cyan,bright]#(node ~/ticker.js)'
set -g status-right-length 75
set status-interval 60
```

then run 

```
tmux source-file ~/.tmux.conf
```
