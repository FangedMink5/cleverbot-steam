# Cleverbot - Steam chat bot

Simple Steam chat bot for people who are bored and don't have anyone to talk with. <3 [Cleverbot](http://www.cleverbot.com/).

[Try it now, talk with my bot!](http://steamcommunity.com/id/YouAreABot/)

## Run your own bot

* Install [node.js](http://nodejs.org/).
* In the directory with cleverbot-steam:
  * `npm install` to install dependencies
  * `sudo npm install -g forever`
  * Copy [config.json.example](config.json.example) to `config.json` and set values:
      * `steamUsername` - Bot's Steam username.
      * `steamPassword` - Bot's Steam password.
      * `botName` - This will change the profile name of your bot.
      * `botState` - Profile state of your bot. Options: _online_, _offline_, _busy_, _away_, _snooze_
      * `botAdmins` - Array of SteamIDs of people who can send commands (example `/send <roomID> <message>`) to your bot. `/help` command lists all commands.
      * `listenToCalls` - Bot replies in the group chat only to messages starting with the specified strings (case insensitive).
      * `defaultJoinMessage` - Default message the bot will send when joining a chat unless a message is specified (or the message is `false`).
      * `autoJoin` - List of chatrooms (group and friend chats) to automatically join with an optional message (say hello).
  * Start the bot with [start_bot_production.sh](start_bot_production.sh) or [start_bot_staging.sh](start_bot_staging.sh).