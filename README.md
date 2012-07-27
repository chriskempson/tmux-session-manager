# Tmux Session Manager (TSM)
A simple ruby script to aid working with and creating tmux sessions.

## Using TSM
Tmux Session manager contains the following tasks:

    tsm help [TASK]  # Describe available tasks or one specific task
    tsm list         # Lists all available sessions configs
    tsm open         # Opens a session
    tsm view         # View a session config
  
Each task is aliased by its first character e.g. `tsm o`, `tsm v`.

## Config Example
Before using TMS you'll need to create a config file for your session you wish to setup

The following file is `~/.tsm/example.yml`

    description: Example Session
    session_dir: ~/example
    session_url: example.dev:8080
    windows:
      compass: [ cd public, clear, compass watch ]
      www: none

Every config option in this file is optional.

## Per-session Environment Variables
The environment variables `SESSION_DIR` and `SESSION_URL` are available to you. One possible use is to create aliases that make use of these.

    alias osd="open $SESSION_DIR"
    alias osu="open $SESSION_URL"
    alias ose="mate $SESSION_DIR"

## Install
Installation is currently a manual process.

    mkdir ~/.tsm
    ln -s PATH_TO_TSM/tsm /usr/local/bin/tsm

## Todo
* Add copy feature to clone existing configs
* Add edit feature to launch the default editor for the specified config
* Tidy the code
* Write a better Readme
* Package into a Gem?

## Contributors
* Just me so far!