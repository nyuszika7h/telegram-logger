# telegram-logger

A simple Python script using Telethon to log all (or some) messages a user or bot account can see on Telegram.

# Requirements
* Python 3.6 or newer
* Python package dependencies: `poetry install` or `pip install -r requirements.txt`
* A Telegram user or bot account

# Usage
Set your `api_id` and `api_hash` in `config.toml`. You can get this from "API development tools" on <https://my.telegram.org/>. Note that this authenticates an app, not a user.

When you start the script for the first time, you will be prompted for credentials. Upon successful authentication, it will start logging all messages it can see to stdout.

You can set `enabled_chats` and `disabled_chats` in the config to a list of chat IDs to control which chats should be logged (the default is all).

You can set `log_seperate_files` to `false` if you want the all logging to be saved to one file, the default is one file per chatId.

When logging to files, you may want to turn logging to stdout off, by setting `log_stdout` to false.
