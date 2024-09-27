```tmux.conf
# <--------------------------Tmux Configurations-------------------------->

# Tmux display message on start
set-hook -g session-created 'display "Hello Nathan, Welcome to Fortlinx !!"'
set -g display-time 3000

# Reload tmux.conf with source
bind R source-file ~/.tmux.conf \; display "Source Reloaded! Ready to Bang !!" 

# Change the prefix key to Ctrl + Space
unbind C-Space
set -g prefix C-Space
bind C-Space send-prefix

# Set history limit to 97531
set -g history-limit 97531

# Set pane index numbering to start from 1
set-window-option -g pane-base-index 1

# Switch back to previous active window
bind Tab last-window

# Bind Home key to return to marked window
bind Home switch-client -t'{marked}'

# Create new panes with current directory path
bind % split-window -h -c "#{pane_current_path}"
bind '"' split-window -v -c "#{pane_current_path}"

# Join pane from another window
bind V choose-window 'join-pane -h -s "%%"'
bind H choose-window 'join-pane -s "%%"'

# Change default emacs mode to vi mode
set -g mode-keys vi
setw -g mode-keys vi

# Remap navigation keys to Vim keys
bind h select-pane -L
bind j select-pane -D
bind k select-pane -U
bind l select-pane -R

# <--Disabled Features-->

# Activate mouse in Tmux - Disabled
# set -g mouse off

# Create new window with current directory path - Disabled
# bind c new-window -c "#{pane_current_path}"

# List of plugins

set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'tmux-plugins/tmux-logging'











# Initialize TMUX plugin manager (keep at bottom)
# Run mkdir ~/.tmux; mkdir ~/.tmux/plugins; before running this command.
run '~/.tmux/plugins/tpm/tpm'
```