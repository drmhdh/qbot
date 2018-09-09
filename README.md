# qbot

A plugin based, (user)bot for Telegram, somewhat inspired by [otouto], and [uniborg].

[otouto]: https://github.com/topkecleon/otouto/
[uniborg]: https://github.com/uniborg/uniborg

## Requirements
- [Telethon] 1.2
- \>= Python 3.5 (Tested on 3.6.6 and 3.7.0)
- A brain probably

[Telethon]: https://github.com/LonamiWebs/Telethon

---

## Built-In Functions

#### In Private
-  `/ping`
-  `/start`


## Installation and Setup

1.  `cp example_config.ini config.ini`
1.  Follow this [link][my telegram] and login with your phone number
1.  A Create new application window will appear.  Fill in your application details.  There is no need to enter any URL, and only the first two fields (App title and Short name) can currently be changed later.
1.  Click on Create application at the end.  
1.  Add your api id, api hash, and other information to `config.ini`
    -  Create a bot with botfather if you need/want to
    -  If you want a userbot; add your phone number to `PHONE`, if you want an api bot; add your bot token to `TOKEN`
1.  Start bot  

#### Remember that your API hash is secret and Telegram won’t let you revoke it.  Don’t post it anywhere!

[my telegram]: https://my.telegram.org/

`start.sh` creates a `screen` session called `qbot`.  Check the logs by doing `screen -r qbot`.  Detach from the session with `ctrl a`, `d`.  Stop the bot with `ctrl c`.


## Adding Custom Plugins

Create a new plugin file using the template `{name}plugin.py`.  For example `my_plugin.py`.  
`from telethon import events, sync` and `from global_functions import probability` should be at the top.  Then just add whatever you want.
