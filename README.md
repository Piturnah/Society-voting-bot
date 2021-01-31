# CSS voting-bot
A Discord bot for doing basic CSS's elections at the University of Birmingham. The voting system used is Instant Runoff Voting.

## Dependencies
    pip install -U Discord.py python-dotenv pyrankvote

## Setup

You'll need to create a discord bot of your own in the [Discord Developer Portal](https://discord.com/developers/applications) with View Channels and Read Messages permissions. It's also handy if you have an empty server (or "guild") for you to test in. This section of [this guide](https://realpython.com/how-to-make-a-discord-bot-python/#how-to-make-a-discord-bot-in-the-developer-portal) may be helpful to set that up.

You'll need to set three environment variables:
* DISCORD TOKEN -> The Discord token for the bot you created (available on your bot page in the developer portal).
* GUILD_URL -> The URL of the UoB Guild of Students members page (make sure it's listed by group).
* GUILD_COOKIE -> Your Guild of Students session cookie so the bot has permission to view your members list (You can extract this from your web browser after signing in to the Guild of Students website. You must be a committee member).
* COMMITTEE_CHANNEL_ID -> The Discord channel ID for the committee channel, this is where you setup new posts, get the members list and see results. This should be a channel only available to committee members.
* VOTING_CHANNEL_ID -> The Discord channel ID for the voting channel, this is where elections are started by committee members. This should be a channel only available to members.
* VOTERS_FILE -> The file that the registered voter list is backed up to.
* STANDING_FILE -> The file that the standing candidates list is backed up to.

You can put these in a .env file in the repo directory as it uses dotenv (See [here](https://pypi.org/project/python-dotenv/) for usage) so you don't have to keep them in your environment.

## Contributions

In short, patches welcome. If you raise a PR, I'll review it, test it, and (probably) merge it.