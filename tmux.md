# How to use tmux
### basics
```bash
tmux new -s kos_session # starts session with this name

tmux kill-session -t mysession # kills session with that name
tmux kill-session -a # kills all but the current
tmux kill-session -a -t mysession # kill all but mysession
tmux kill-server # kill all sessions

ctrl+b d # detach from session

tmux ls # list all sessions

tmux attach -t
tmux attach -t mysession # attach to a session

ctrl+b w # preview

ctrl+b % # right
ctrl+b "" # below

ctrl+b arr_down/arr_left # switch to pane

ctrl+b [ # scroll mode

: kill-session # kills all windows
```