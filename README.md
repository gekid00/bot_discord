# Bot Discord

A multi-purpose Discord bot built with Python and the discord.py library.
The project provides a foundation for custom commands and event handling on Discord servers.

## Technologies

- Python 3
- [discord.py](https://discordpy.readthedocs.io/)

## Prerequisites

- Python 3.8 or higher
- A Discord bot token (create one at the [Discord Developer Portal](https://discord.com/developers/applications))

## Setup

```bash
# Clone the repository
git clone https://github.com/gekid00/bot_discord.git
cd bot_discord

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Configuration

1. Go to the Discord Developer Portal and create a new application.
2. Under the **Bot** tab, copy your bot token.
3. Set the token as an environment variable or store it in a `.env` file:
   ```
   DISCORD_TOKEN=your_token_here
   ```
4. Invite the bot to your server using the OAuth2 URL generator with the `bot` scope.

## Usage

```bash
python main.py
```

Once the bot is online in your server, interact with it using the configured command prefix. Example commands:

| Command | Description          |
|---------|----------------------|
| `ping`  | Check bot latency    |
| `echo`  | Repeat a message     |

## Project Structure

Commands are organized in the `commands/` directory. Each module registers its own commands, keeping the codebase modular and easy to extend.

## Key Concepts

- **Cogs**: discord.py organizes commands into cog classes, allowing logical grouping and lazy loading.
- **Intents**: The bot declares the gateway intents it requires so Discord only sends relevant events.
- **Async / Await**: All command handlers and event listeners run on an asyncio event loop provided by discord.py.
