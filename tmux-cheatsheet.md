# tmux CLI

- start new session:

    `tmux`

- list sessions:

    `tmux ls`

- attach to last session:

    `tmux a`

- kill session:

    `tmux kill-ses -t name/#`

# Inisde tmux, hit the prefix `ctrl+a` and then:

## Sessions

    :new<CR>  new session
    s  list sessions
    $  rename session
    d  detach session

## Windows (tabs)

    c  new window
    w  list windows    
    ,  rename window
    &  kill window
    
## Panes (splits)

    -  horizontal split
    \  vertical split
    type: exit  kill pane

## Misc

    d  detach
    t  big clock
    ?  list shortcuts
    :  prompt

# Resources

* [cheat sheet](http://cheat.errtheblog.com/s/tmux/)


