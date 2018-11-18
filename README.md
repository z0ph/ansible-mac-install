# Ansible Playbook for Mac install

[![Build Status](https://travis-ci.org/z0ph/ansible-mac-install.svg?branch=master)](https://travis-ci.org/z0ph/ansible-mac-install) 

Tested on macOS: `10.14.1 (18B2107)`

## Disclaimer

This installation is setup for my own usage, and to my needs. Please adapt the configuration.
This playbook comes from [flemzord](https://github.com/flemzord/ansible-mac-install), and [geerlingguy](https://github.com/geerlingguy/mac-dev-playbook)

## Installation

On a fresh macOS installation:

  1. Run `xcode-select --install` to install minimal tools (git, ...)
  2. Fork, then Clone this repository to your local drive.
  3. Change and adapt to your needs the configuration in ```config.yml```.
  4. Run ```sh run.sh``` from your brand new macOS installation.
  5. Don't forget to commit & push your changes for your next installation.

## Upgrade

To upgrade your macOS installation:

    $ sh files/upgrade.sh

## Options

### Configure dotfiles

To enable the configuration of dotfiles, and download from your own repository.

`configure_dotfiles: yes`

configure the following options in `config.yml`

```yml
dotfiles_repo: https://github.com/your/dotfiles_repo.git
dotfiles_repo_accept_hostkey: yes
dotfiles_repo_local_destination: ~/.dotfiles # destination
dotfiles_files: # file to download
  - .gitignore
  - .osx
  - .zshrc
  - .alias.sh
  - .bashrc
```

### Configure sudoers

Register `sed` and copy sudoers template.

`configure_sudoers: yes`

### Configure osx

configure macOS with `.osx` file

`configure_osx: no`

### Configure extra

Configure few personal stuffs:

* Install zsh theme
* Install zsh plugins
* Set zsh as defaut shell
* Install oh-my-zsh
* Install pure-prompt
* Set an `/etc/hosts` entry

`configure_extra: yes`

### Configure dock

Remove and add icons in the dock

`configure_dock: yes`