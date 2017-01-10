# tssh
Tmux cluster ssh same as many many others. This time with autocomplete from `~/.ssh/config`.

## Usage
```shell
tssh host1 host2 host3
```

Where hostnames are from ~/.ssh/config.

You can actually add hosts in `user@IP` and disable pane synchronization with `C+b :setw synchronize-panes off`.

### Autocomplete example
```shell
[jkvita@galahad tssh] $ tssh
bastion-production  flynn-dev1          flynn-dev3          flynn-prod-backup2  flynn-prod-backup4  nginx-prod-east2    nginx-prod-west2    nginx-staging2      
bastion-staging     flynn-dev2          flynn-prod-backup1  flynn-prod-backup3  nginx-prod-east1    nginx-prod-wes1     nginx-staging1      
[jkvita@galahad tssh] $ tssh
```

## Installation
Copy executable to `/usr/local/bin` and autocomplete script to `/usr/share/bash-completion/completions`
```bash
sudo wget -O /usr/local/bin/tssh  https://raw.githubusercontent.com/kvitajakub/tssh/master/tssh
sudo chmod 755 /usr/local/bin/tssh
sudo wget -O /usr/share/bash-completion/completions/tssh  https://raw.githubusercontent.com/kvitajakub/tssh/master/tssh-autocomplete
```
