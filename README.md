# for support join here [TorrentLeech-Gdrive](https://telegram.dog/GBotStore)
# working example group [Leech Here](https://t.me/AKLEECHZONE)

A Telegram Torrent (and youtube-dl) Leecher.

# Benefits :-
    ✓ Telegram File mirrorring to cloud along with its unzipping, unrar and untar
    ✓ Drive/Teamdrive support/All other cloud services rclone.org supports
    ✓ Unzip
    ✓ Unrar
    ✓ Untar
    ✓ Custom file name
    ✓ Custom commands
    ✓ Get total size of your working cloud directory
    ✓ You can also upload files downloaded from /ytdl command to gdrive using `/ytdl gdrive` command.
    ✓ You can also deploy this on your VPS
    ✓ Option to select either video will be uploaded as document or streamable
    ✓ Added /renewme command to clear the downloads which are not deleted automatically.
    ✓ Added support for youtube playlist 😐
    ✓
    
# TO-DO
-   [x] Gdrive file clonning using Gclone

### Credit goes to SpEcHiDe for his Publicleech repo.

## installing...

### The Easy Way

#### STEPS (I did this to avoid the use of same button multiple times)

a)You have to fork this repo at first(Don't know how to🤔, Then google it😐)

b)Find `app.jso`. 🧐

c)Tap on that. 😬

d)Tap to edit and just add `n` at last of name (Don't touch code🤦). ✍️

e)It should look like `app.json`. 🎉

f)Then tap 👇👇

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy) #Revived 

<p><a href="https://heroku.com/deploy?template=https://github.com/akprivatebots/VideoLeech"> <img src="https://img.shields.io/badge/Deploy%20To%20Heroku-blueviolet?style=for-the-badge&logo=heroku" width="200""/></a></p>


### an example config.py 👇
```py
from tobrot.sample_config import Config

class Config(Config):
  TG_BOT_TOKEN = ""
  APP_ID = 6
  API_HASH = "eb06d4abfb49dc3eeb1aeb98ae0f581e"
  AUTH_CHANNEL = [-1001234567890]
```

### Variable Explanations

##### Mandatory Variables

* `TG_BOT_TOKEN`: Create a bot using [@BotFather](https://telegram.dog/BotFather), and get the Telegram API token.

* `APP_ID`
* `API_HASH`: Get these two values from [my.telegram.org/apps](https://my.telegram.org/apps).
  * N.B.: if Telegram is blocked by your ISP, try our [Telegram bot](https://telegram.dog/UseTGXBot) to get the IDs.

* `AUTH_CHANNEL`: Create a Super Group in Telegram, add `@GoogleIMGBot` to the group, and send /id in the chat, to get this value.

* `RCLONE_CONFIG`: Create the rclone config using the rclone.org and read the rclone section for the next.

* `DESTINATION_FOLDER`: Name of your folder in ur respective drive where you want to upload the files using the bot.

* `OWNER_ID`: ID of the bot owner, He/she can be abled to access bot in bot only mode too(private mode).

##### Set Rclone

1. Set Rclone locally by following the official repo : https://rclone.org/docs/
2. Get your `rclone.conf` file.
will look like this
```
[NAME]
type = 
scope =
token =
client_id = 
client_secret = 

```
3. Only copy the config of drive u want to upload file.
4. Copy the entries of `rclone.conf` 
5. Your copied config should look like this:
 ```
type = 
scope =
token =
client_id = 
client_secret = 

and everythin except `[NAME]`

```

6. Paste copied config in `RCLONE_CONFIG`

7. Hit deploy button.
8. Examples:-


## FAQ

##### Optional Configuration Variables

* `DOWNLOAD_LOCATION`

* `MAX_FILE_SIZE`

* `TG_MAX_FILE_SIZE`

* `FREE_USER_MAX_FILE_SIZE`

* `MAX_TG_SPLIT_FILE_SIZE`

* `CHUNK_SIZE`

* `MAX_MESSAGE_LENGTH`

* `PROCESS_MAX_TIMEOUT`

* `ARIA_TWO_STARTED_PORT`

* `EDIT_SLEEP_TIME_OUT`

* `MAX_TIME_TO_WAIT_FOR_TORRENTS_TO_START`

* `FINISHED_PROGRESS_STR`

* `UN_FINISHED_PROGRESS_STR`

* `TG_OFFENSIVE_API`

* `CUSTOM_FILE_NAME`

* `LEECH_COMMAND`

* `YTDL_COMMAND`

* `GLEECH_COMMAND`

* `TELEGRAM_LEECH_COMMAND_G`

* `PYTDL_COMMAND_G`

* `UPLOAD_AS_DOC`: Takes two option True or False. If True file will be uploaded as document. This is for people who wants video files as document instead of streamable.

* `INDEX_LINK`: (Without `/` at last of the link, otherwise u will get error) During creating index, plz fill `Default Root ID` with the id of your `DESTINATION_FOLDER` after creating. Otherwise index will not work properly.
## Available Commands

* `/ytdl`: This command should be used as reply to a [supported link](https://ytdl-org.github.io/youtube-dl/supportedsites.html)

* `/pytdl`: This command will download videos from youtube playlist link and will upload to telegram.

* `/ytdl gdrive`: This will download and upload to your cloud.

* `/pytdl gdrive`: This download youtube playlist and upload to your cloud.

* `/leech`: This command should be used as reply to a magnetic link, a torrent link, or a direct link. [this command will SPAM the chat and send the downloads a seperate files, if there is more than one file, in the specified torrent]

* `/leech archive`: This command should be used as reply to a magnetic link, a torrent link, or a direct link. [This command will create a .tar.gz file of the output directory, and send the files in the chat, splited into PARTS of 1024MiB each, due to Telegram limitations]

* `/gleech`: This command should be used as reply to a magnetic link, a torrent link, or a direct link. And this will download the files from the given link or torrent and will upload to the cloud using rclone.

* `/gleech archive` This command will compress the folder/file and will upload to your cloud.

* `/leech unzip`: This will unzip the .zip file and dupload to telegram.

* `/gleech unzip`: This will unzip the .zip file and upload to cloud.

* `/leech unrar`: This will unrar the .rar file and dupload to telegram.

* `/gleech unrar`: This will unrar the .rar file and upload to cloud.

* `/leech untar`: This will untar the .tar file and upload to telegram.

* `/gleech untar`: This will untar the .tar file and upload to cloud..

* `/tleech`: This will mirror the telegram files to ur respective cloud cloud.

* `/tleech unzip`: This will unzip the .zip telegram file and upload to cloud.

* `/tleech unrar`: This will unrar the .rar telegram file and upload to cloud.

* `/tleech untar`: This will untar the .tar telegram file and upload to cloud.

* `/getsize`: This will give you total size of your destination folder in cloud.

* `/renewme`: This will clear the remains of downloads which are not getting deleted after upload of the file or after /cancel command.

* `/uploadasdoc`: all your Telegram uploads will be as document here after until server restarted(its standalone command no need to reply to any media)
 
* `/uploadasvideo`: all your Telegram uploads will be as video here after until server restarted(its standalone command no need to reply to any media)

values in the <> are variables

* `/split <4>`: This will split the given Telegram video file into 4 equal parts and upload to Telegram Ex:/split 6

* `/split <00:10:00-00:15:00>`: This will get sample of given telegram video from 10th min to 15th min and will upload to Telegram(you can change the timestamps) Ex: /split 00:02:00-01:02:00

* `/rename <newfilename>`: This will rename the given telegram file and upload to cloud and telegram Ex:/rename Dark S02 E04

* `/leech rename <newfilename>`: This will rename the file and upload to telegram after leech.

* `/gleech rename <newfilename>`: This will rename the file and upload to your cloud after leech.



* [Only work with direct link for now]It is like u can add custom name as prefix of the original file name.
Like if your file name is `gk.txt` uploaded will be what u add in `CUSTOM_FILE_NAME` + `gk.txt`

## How to Use?

* send any one of the available command, as a reply to a valid link/magnet/torrent. 👊
