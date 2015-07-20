Brosec
======
Security, for Bros.

Overview
=========

- Brosec is a reference utility to help Security Bros with useful payloads and commands
- Brosec utilizes saved configuration variables (set at any time by you) to create custom payloads on the fly. These variables persist in a local database for your convenience.
- Brosec outputs payloads and copies them to your clipboard in order to make your pentesting even more magical


###### XXE for Bros
![](http://i.imgur.com/hxrqlvk.gif)

<br>
- Configuration variables can be accessed by the `config` command at any time, or by entering the variable name
- Config values can be changed at any time by entering `set <variable> <value>`

![](http://i.imgur.com/FCateZJ.gif)

- You can navigate to frequently used payloads by entering the menu sequence from the command line: `bros <sequence>`
  - Ex: `bros 413` - This would automate entering 4 for the Web Menu, 1 for the XXE sub menu, and 3 for the XXE local file read payload


Installation
============

#### Mac

- `brew install node netcat` - Install Nodejs and netcat
- `git clone https://github.com/gabemarshall/Brosec.git` - Clone Brosec repo
- `cd Brosec && npm install` - cd into the directory and install npm depdendencies

#### Linux

- `<package manager> install node build-essential g++ xclip netcat` Install Nodejs and other dependencies
- `git clone https://github.com/gabemarshall/Brosec.git` - Clone Brosec repo
- `cd Brosec && npm install` - cd into the directory and install npm depdendencies


Configuration
=====================

Brosec stores configuration values in a local json db file. The default storage location is /var/tmp, but can be changed by editing settings.dbPath variable in the settings.js file. Brosec also uses netcat for several payloads. If needed, the path to netcat can be altered via teh settings.netcat variable.

#### Payload Variables

- LHOST : Local IP or name
- LPORT : Local IP or name
- RHOST : Remote IP or name
- RPORT : Remote IP or name
- USER : Username (only used in a few payloads)
- PROMPT : User Prompt (This isn't a stored value. Instead, payloads with this variable will prompt for input.)


Additional Usage Examples
==================

#### Retrieve DNS server(s) of a domain

![](http://i.imgur.com/Rgl8RR6.gif)

[shortcut](http://i.imgur.com/IvOquvj.gif) via command line by running `bros 111`
