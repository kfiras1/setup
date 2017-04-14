setup.git
=========
Download and run this on a new Digital Ocean droplet running Ubuntu 14.04 LTS to
configure both the machine and your individual development environment as
follows:

```sh
# to start, please ssh login as root with your key
wget -qO- github.com/kfiras1/setup/raw/master/update_locales.sh | sh
exit
# please ssh login as root again
wget -qO- github.com/kfiras1/setup/raw/master/create_user.sh | sh -s <your_username>
su <your_username>
cd
wget -qO- github.com/kfiras1/setup/raw/master/setup.sh | sh -s <your_username>
#After this last command, dotfiles folder have to be created. Otherwise, zsh will not be configured correctly
#After executing next command, try option 0 in zsh wizard
zsh
wget -qO- github.com/kfiras1/setup/raw/master/configure_zsh.sh | zsh
# you can now exit and reconnect as <your_username> with the same key

```
Install Menlo-Powerline on your local machine: https://github.com/thlorenz/dotfiles/commit/d7de2f6ed73136fc9cedfd89ae5577253286dd2d

Run the following for ubismart only
```sh
wget -qO- github.com/kfiras1/setup/raw/master/ubi_setup.sh | sh
```

###Notes: 
* You will probably need to exit and reconnect to apply the new shell profile.
* It may also be necessary to install flycheck from emacs package manager.

See also http://github.com/kfiras1/dotfiles and
[Startup Engineering Video Lectures 4a/4b](https://class.coursera.org/startup-001/lecture/index)
for more details.





