# Joke of the Week Discord Bot

Vote for the Joke of the Week.

## Invite the bot

https://discord.com/api/oauth2/authorize?client_id=933319312402436206&permissions=68672&scope=bot%20applications.commands

## Usage

- `/channel`: Set the channel for polls
- `/submit`: Submit a joke

## For Developers

### Create a Discord Application

If you want to run the bot yourself, [create a new Discord Bot](https://discordapp.com/developers/docs/intro#bots-and-apps).
Then make a copy of `template.env` and call it `.env` and copy your token into this file. In most cases using the same
token as `DISCORD_DEV_TOKEN` and `DISCORD_PROD_TOKEN` should be sufficient. However, if you want to work on the bot
while an instance is running, you should create a second bot and use it's token as `DISCORD_ENV_TOKEN`.

### Get your invite link

To create an invite link for your bot, replace `933319312402436206` in the link above with the Client ID of your Discord
Application and `68672` with the generated integer.

### Start the Bot

#### Development

```shell
npm install
npm run start:dev
```

#### Production

```shell
docker-compose up -d
```

### CI/CD

You can set up a GitHub Actions Workflow by copying the [deploy.yml](https://github.com/schollsebastian/CI-Example-Bot/blob/main/.github/workflows/deploy.yml)
file into the `.github/workflows` directory of your repository.
