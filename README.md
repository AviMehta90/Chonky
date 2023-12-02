# Chonky

This project is a Discord bot implemented in Python using the Discord.py library. The bot is designed to provide user login functionality, manage credentials, and display user-specific activities.

## Project Overview

The main functionalities of the Discord bot include user login, user logout, displaying user credentials, and changing user credentials. The project is structured in the following way:

### Dependencies

The project depends on the following libraries:

- `discord.py`: A library for interacting with the Discord API.
- `json`: Used for reading and writing data in JSON format.

### Bot Commands

1. **Login (`ch login`)**: This command allows a user to log in to the bot. When logged in, the bot sets the user's name as its activity and changes its presence status accordingly.

2. **Logout (`ch logout`)**: This command logs the user out from the bot. Upon logout, the bot's presence status is cleared.

3. **Show Credentials (`ch creds`)**: This command displays the user's credentials, such as their username and password. The credentials are read from a JSON file.

4. **Change Credentials (`ch credchange`)**: This command allows the user to change their credentials. It prompts the user to enter a new username and password, and the updated credentials are stored in a JSON file.

### Bot Initialization

The bot is initialized with a custom command prefix, which is set to 'ch' (short for 'chat').

### Event Handling

The bot includes an event handler that runs when the bot is ready. It prints a message indicating that the bot has logged in and displays its username.

## Usage

To use this Discord bot:

1. Ensure you have the required dependencies (`discord.py` and `json`) installed.

2. Create a `creds.json` file to store user credentials. It should have the structure:
   ```json
   {
       "username": "your_username",
       "password": "your_password"
   }
   ```

3. Create an `auth.json` file to manage the login state. It should have the structure:
   ```json
   {
       "flag": 0,
       "user": null
   }
   ```

4. Replace `'BOT_TOKEN'` with your actual Discord bot token in the `bot.run(os.environ['BOT_TOKEN'])` line.

5. Run the bot script using Python. The bot will log in to Discord and be ready to respond to commands.

6. Users can interact with the bot by sending messages with the specified command prefix ('ch') followed by one of the available commands.

## Notes

- This project is a basic example of a Discord bot with user login and credential management functionality. It can be extended and improved for more complex use cases and security considerations.
- Always keep your bot token and user credentials secure and avoid sharing them with others.


## Disclaimer

This project is for educational purposes and may lack robust security features typically required in production applications. Be cautious when using and sharing sensitive information through Discord bots.
