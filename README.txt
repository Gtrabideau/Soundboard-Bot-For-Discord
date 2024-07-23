Discord Soundboard Bot

Description:
This is a completed Discord Bot except for the bot token in the .esv file, where the user can place their own discord bot token.

This project has the functionality of a soundboard which stores audio files locally on your computer, but allows you to play it over a Discord voice channel by way of a bot. For an exhaustive list of commands look at the bottom of this file or use the ?help command in a server where the bot is running.

How To Run Bot:
1. Go to the Applications section of the Discord Developer Portal at: https://discord.com/developers/applications. Make sure your logged into Discord on this page.
2. Create a new application by clicking the "New Application" button. Name yoour bot then select "Create."
3. Select the "Bot" tab on the left side while you have your new application selected. On that page click the "Reset Token" button and follow the instructions in order to get a bot token. Do not share your bot token with anyone, as they will be able to control your your bot if they have it.
4. Copy this token and put it into the .esv file where it tells you to put the token, make sure to have the token surrounded by only single quotes i.e. BOT_TOKEN='5u34n3403h239845n932485hn98'
5. While your still on the Bot tab, scroll down and toggle "PRESENCE INTENT," "SERVER MEMBERS INTENT," and "MESSAGE CONTENT INTENT" so it is on so the bot is able to recieve commands and carry out commmands from your server.
6. Go to the OAuth2 section in your new application. Under "OAuth2 URL Generator" click the "messages.read" and "bot" boxes to enable them, then in the "BOT PERMISSIONS" tab below select "Administrator." This gives the bot the permissions it needs to work and since you are running the bot yourself, it is safe.
7. At the bottom of the OAuth2 tab there should now be a "GENERATED URL." Copy this URL and paste it into your browser, then add it to the server you want it to be on. Once this is done, the bot should be a part of the server and offline.
8. Finally, open the main.py file in your compiler of choice (PyCharm is what I use) and run it. While it is being run the Discord bot should be online and you should be able to use the bot on your server.

Warning: Do not displace any of the files of the bot from their intended location. "main.py," ".env," and the "cogs" folder should all be within the same folder. The "cogs" folder should also contain "audioClips" which holds the "audioData.csv" file and audio files you save to the bot. The "cogs" folder should also contain the .py files "Audio.py" and "Basics.py." Displacing these files could cause the bot to lose some functionality or more likely stop working completely. Besides this, you should be able to place the "Bot Folder" containing all these files anywhere on your computer.



COMMANDS

?help
Gives a list of commands.

?join
This command makes the bot join your current voice channel.

?leave
This command makes the bot leave whatever voice channel it is in.

?ping
This command gives the bots latency.

?save (Audio attachment)
Use this command with an audio attachment to save the audio file to the bots folder on your local system. You can add an attachment to a post by using Discord's built in attachment system or by copy and pasting the file into the message field.

?play (Audio name)
Use this command to play the audio you saved. You can use the name of the sound with or without the extention.
Example: ?play sound.mp3 or ?play sound

?delete (Audio name)
Use this command to delete a previously saved audio file. You can use the name of the sound with or without the extention.
Example: ?delete sound.mp3 or ?delete sound

?list
Use this command to list the saved audio clips and if they are bound to the soundboard.

?set (Audio name) (Board number)
Use this command to set one of your saved audio files to the soundboard. This command requires you to give the name of the audio, similar to play or delete, and then a number (1 to 9) to indicate which button of the soundboard you want the sound to be on.
Example: ?set sound.mp3 1 or ?set sound 7

?board
Use this command to open the soundboard. If you have not used the ?set command to set audio files to the buttons, the buttons will not do anything. After you set a audio file to a button, you can press the buttons on the board to play the bound sound.