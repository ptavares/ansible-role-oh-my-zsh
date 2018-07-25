[![Build Status](https://img.shields.io/travis/ptavares/ansible-role-oh-my-zsh/master.svg?style=flat-square)](https://travis-ci.org/ptavares/ansible-role-oh-my-zsh)
[![Ansible Role](https://img.shields.io/ansible/role/27782.svg)](https://galaxy.ansible.com/ptavares/ansible-role-oh-my-zsh)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.txt)

ansible-role-oh-my-zsh
=========

Ansible role for installating and configuring zsh and oh-my-zsh

Requirements
------------

Only test with ansible 2.5 min version

Role Variables
--------------
- Copy content of [main.yml](https://github.com/ptavares/ansible-role-oh-my-zsh/blob/master/defaults/main.yml) in your playbook's vars file.
- Customize it as you like, following as below : 
```yaml
---
#####################
# Section for theme
#####################

# Default theme to load (included with oh-my-zsh)
# All included theme here : https://github.com/robbyrussell/oh-my-zsh/tree/master/themes
oh_my_zsh_default_theme: robbyrussell

# For a custom theme not present in $HOME/.oh-my-zsh/themes or in $HOME/.oh-my-zsh/custom/themes/ :
# 1. Fill oh_my_zsh_custom_theme_info
#    - This theme will be checkout into directory $HOME/.oh-my-zsh/custom/custom-themes/
# oh_my_zsh_custom_theme_info: { url: "oh_my_zsh_custom_theme_git_url", dir_dest_name: "oh_my_zsh_custom_git_dir_name" }
# example :
# oh_my_zsh_custom_theme_info: { url: "https://github.com/ptavares/zsh-themes.git", dir_dest_name: zsh-themes }

# 2. Choose the custom zsh theme name to load
#    - A symlink will be created from $HOME/.oh-my-zsh/custom/custom-themes/oh_my_zsh_custom_theme_git_dir_name/oh_my_zsh_custom_theme_name to $HOME/.oh-my-zsh/custom/themes/
# oh_my_zsh_custom_theme: oh_my_zsh_custom_theme_name
# example :
# oh_my_zsh_custom_theme: ptavares


#####################
# Section for plugins
#####################

# Default plugins to load (included with oh-my-zsh installation)
# All included plugins here : https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins
oh_my_zsh_default_plugins:
  - git

# For custom plugins not present in $HOME/.oh-my-zsh/plugins or in $HOME/.oh-my-zsh/custom/plugins/ :
# 1. Fill oh_my_zsh_custom_plugins_info
#    - Plugins will be checkout into directory $HOME/.oh-my-zsh/custom/custom-plugins/
#    - A symlink will be created from $HOME/.oh-my-zsh/custom/custom-plugins/oh_my_zsh_custom_plugin_dir_name to $HOME/.oh-my-zsh/custom/plugins/
# oh_my_zsh_custom_plugins_info: { url: "oh_my_zsh_custom_plugin_git_url", dir_dest_name: "oh_my_zsh_custom_plugin_git_dir_name" }
# example :
# oh_my_zsh_custom_plugins_info:
#  - { url: "https://github.com/junegunn/fzf.git", dir_dest_name : fzf }
#  - { url: "https://github.com/Treri/fzf-zsh.git", dir_dest_name: fzf-zsh }
#  - { url: "https://github.com/zsh-users/zsh-autosuggestions.git", dir_dest_name: zsh-autosuggestions }
#  - { url: "https://github.com/zdharma/fast-syntax-highlighting.git", dir_dest_name: fast-syntax-highlighting }
#  - { url: "https://github.com/chrissicool/zsh-bash.git", dir_dest_name: zsh-bash }

# 2. List all your custom plugins to load on startup zsh
# oh_my_zsh_custom_plugins:
#	 - oh_my_zsh_custom_plugin_1
#  - oh_my_zsh_custom_plugin_2
# example :
# oh_my_zsh_custom_plugins:
#  - fzf-zsh
#  - zsh-autosuggestions
#  - fast-syntax-highlighting
#  - zsh-bash

# 3. Extra plugin command
# Some plugins need extra command to run successfully
# oh_my_zsh_custom_plugins_command :
#	 - "oh_my_zsh_custom_plugins_command_1"
#  - "oh_my_zsh_custom_plugins_command_2"
# exemple :
# oh_my_zsh_custom_plugins_command :
#	 - "$HOME/.oh-my-zsh/custom/plugins/fzf/install --all"
#  - "fast-theme safari"


######################################
# Section for custom entries in .zshrc
######################################
# Add here all entries you need to put in zhrc file, like alias for example
# oh_my_zsh_custom_zsh_entries:
#	 - "oh_my_zsh_custom_zsh_entries_1"
#	 - "oh_my_zsh_custom_zsh_entries_2"
# example:
# oh_my_zsh_custom_zsh_entries:
#  - "# List only directories alias"
#  - "alias lsd='ls -l | grep \"^d\"'"
```

Dependencies
------------

No dependencie

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
         - { role: ptavares.ansible_role_oh_my_zsh }

License
-------

MIT
