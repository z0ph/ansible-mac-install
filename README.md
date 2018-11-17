# Ansible Playbook for Mac install

[![Build Status](https://travis-ci.org/z0ph/ansible-mac-install.svg?branch=master)](https://travis-ci.org/z0ph/ansible-mac-install) 

## Disclaimer

This installation is setup for my own usage, and to my needs. Please adapt the configuration.
This playbook comes from [flemzord](https://github.com/flemzord/ansible-mac-install), and [geerlingguy](https://github.com/geerlingguy/mac-dev-playbook)

## Installation

  1. Run `xcode-select --install` to install minimal tools (git, ...)
  2. Clone this repository to your local drive.
  3. Change and adapt to your needs the configuration in ```config.yml```.
  4. Run ```sh run.sh``` from your brand new macOS installation

## Upgrade

To upgrade your installation:

    $ sh files/upgrade.sh