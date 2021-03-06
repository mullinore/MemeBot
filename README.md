# Memebot

Memebot lets you add, play, and share your favorite memes on your discord server.

* Add memes from youtube
* Play memes with commands
* Moderate memes
* Keep track of meme stats

## Usage
Once installed, memebot can be controlled completely from your text channel with the following commands:

`!help` - list of commands  
`!add` - add memes from youtube link  
`!list` - list of your memes  
`!delete` - remove unwanted memes  
`!random` - plays a random memes  
`!info` - stats about your memes  
`![meme]` - plays the meme on your currently connected voice channel

**PSA: You must be connected to a voice channel to play memes**

## Registering a bot with Discord

Before you install the Memebot server, you must register a bot with Discord. Follow Discord's  [guide](https://discordapp.com/developers/docs/intro "discordapp.com") to make a new bot.

## Installation

These installation is for unix-like environments (i.e. Linux and OSX). You may have to do more work to install on Windows.

#### Installing node.js
Install node.js version 6.0.0 or later. I recommend using [nvm](https://github.com/creationix/nvm) to install and manage versions of node.

#### Download repository
```
git clone --bare https://github.com/arjunchib/memebot
```

#### Install dependicies
```
cd memebot
npm install
```

## Setting up environment

#### Create environment file
```
nano .env
```

#### Declare environement variables
In your newly created `.env` file, enter the lines below. Only the `DISCORD_TOKEN` variable is required. The `ADMIN_USER_ID` variable is optional and gives one user admin privaleges (i.e. removing memes).
```
DISCORD_TOKEN=<YOUR DISCORD TOKEN>
ADMIN_USER_ID=<YOUR DISCORD USER ID>
```

Your Discord app token is found in the [Discord Dev Portal](https://discordapp.com/developers/applications/me) in the app page you created earlier. Copy the token under `APP BOT USER` and use that string for `<YOUR DISCORD TOKEN>`.

Follow this [support guide](https://support.discordapp.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-) to find your `ADMIN_USER_ID`.

## Running Memebot

To start the server, in the memebot directory run
```
node index.js
```

To stop the server enter `Ctrl-C`


Optionally, I recommend using [screen](https://www.linode.com/docs/networking/ssh/using-gnu-screen-to-manage-persistent-terminal-sessions) to manage server sessions.

## Adding bot to your Discord server

Go back to the [Discord Dev Portal](https://discordapp.com/developers/applications/me) and find the `Client ID` string in the app you created earlier. Replace `<CLIENT_ID>` in the link below with your app's Client ID.

```
https://discordapp.com/oauth2/authorize?&client_id=<CLIENT_ID>&scope=bot&permissions=0
```

Visit the link in your web browser and follow the instructions to add the bot to your Discord server.
