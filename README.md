# tssh
Tmux cluster ssh same as many many others. This time with autocomplete from `~/.ssh/config`.

## Usage
```shell
tssh host1 host2 host3
```

Where hostnames are from ~/.ssh/config.

You can actually add hosts in `user@IP` and disable pane synchronization with `C+b :setw synchronize-panes off`.

## Installation
Copy executable to `/usr/local/bin` and autocomplete script to `/usr/share/bash-completion/completions`
```bash
sudo wget -O /usr/local/bin/tssh  https://raw.githubusercontent.com/kvitajakub/tssh/master/tssh
sudo chmod 755 /usr/local/bin/tssh
sudo wget -O /usr/share/bash-completion/completions/tssh  https://raw.githubusercontent.com/kvitajakub/tssh/master/tssh-autocomplete
```
