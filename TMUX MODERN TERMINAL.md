```
tmux attach                -> go direct tmux intreface 

tmux ls                    -> check how paration avilable

tmux new -s (name)         -> add new paration

tmux -V                    -> check the install version

which tmux                 -> check the tmux version

Detach TMUX ( come to normal terminal with running tmux )  -> Ctrl + B  and some time press D

echo $TMUX     -> show empty then you will be worked on normal terminal

tmux switch-client -t airflow        |
                                      ->   both command used for session changed 
Ctrl + B press after some time s     |

Session window :

         Session: kubeflow
            ├── Window 0 : coding
            ├── Window 1 : logs
            └── Window 2 : testing

Ctrl+B C   -> used for new windlow

Ctrl+B N   -> next window

Ctrl+B P   -> previous window

Ctrl+B ,

Ctrl + b & press s ( check the running session window

tmux lsw   -> check avilable window 

tmux list-windows    -> check how many window in specifc session

```
