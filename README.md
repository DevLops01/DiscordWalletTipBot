




## Requirements

- node > 9.0.0
- npm > 0.12.x
- Pulse (https://github.com/PulseDeveloper)

## Install the prerequisites
```
$ sudo apt-get install nodejs && apt-get update
```

```
$ wget https://github.com/PulseDeveloper/Pulse/releases/download/v1.2.0.1/pulsed.zip
```

## Installation

Install Pulse
```
$ unzip ~/pulse-linux.zip
```
Follow the instructions on the Pulses GitHub Repository to create a pulse.conf and remember the username and password.

Start Pulse 
```
./pulsed -server -daemon
```

Create a bot and get the bot's API Token: https://discordapp.com/developers/applications/me - https://i.imgur.com/gM8EpJe.png

Make sure the bot has "bot" flags in OAuth2

```
$ cd pulse-tipbot/config
```
Then
```
$ vim default.json.example
```
Input your bots token, the channel ID for your bot command channel, and the username & password for Pulse
Rename the configuration file to "config.json" with

```
$ mv default.json.example config.json
```
Then move the config.json into /bot/config

```
$ mkdir ~/pulse-tipbot/bot/config 
$ cp ~/pulse-tipbot/config/config.json ~/pulse-tipbot/bot/config
```
Then run 
```
npm install
node ~/pulse-tipbot/bot/bot.js
```

To add the bot to your own discord, and for your own coin, edit the default.json file in the config folder.

Then recursively change coin name with an emphasis on capitlization match e.g PLSE - BTC, plse - btc, pulse - bitcoin
