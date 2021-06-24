# Creating an Image Server (ShareX)

## Step 1 - Downloading ShareX


Head over to the [ShareX website](https://getsharex.com/) and click Download. The .exe file will automatically be downloaded to your PC.

## Step 2 - Creating a server
Now, we need to create our ShareX server. We have to go to the commands channel of the DBH discord and type the following command `DBH!server create sharex <name>`. 

![Create a server](https://media.discordapp.net/attachments/754441222424363088/857707564771180554/Screenshot_2021-06-24_at_20.43.33.png?width=1153&height=587)

## Step 3 - Configuring our server

Now we need to visit the [panel](https://panel.danbot.host). After getting there, select your server and go to the file manager. Go to the `src `folder and open `config.json`. You should now see this:
![image](https://tolis.is-a.fail/LV61Gv.png)

> Psst, don't worry. Its too easy to figure out what to do here; just follow my instructions

So, let's configure the server:
```json
{
  "key": [""],
  "domain": "example.com",
  "puploadKeyGenLength": 64,
  "public": false,
  "maxUploadSize": 50,
  "markdown": true,
  "port": 80,
  "secure": true,
  "fileNameLength": 4,
  "shortUrlLength": 3,
  "securePort": 443,
  "ratelimit": 1000,
  "dateURLPath": false,
  "allowed":[
    "png", "jpg", "gif", "mp4", "mp3", "jpeg", "tiff", "bmp", "ico", "psd", "eps", "raw", "cr2", "nef", "sr2", "orf", "svg", "wav", "webm", "aac", "flac", "ogg", "wma", "m4a", "gifv"
  ],
  "admin":{
    "key": ["admin pass key goes here"],
    "maxUploadSize": 1024,
    "allowed": [
    "png", "jpg", "gif", "mp4", "mp3","jpeg", "tiff", "bmp", "ico", "psd", "eps", "raw", "cr2", "nef", "sr2", "orf", "svg", "wav", "webm", "aac", "flac", "ogg", "wma", "m4a", "gifv", "html"
     ]
  },
  "paste": {
    "maxUploadSize": 20
  },
  "discordToken": "Discord Token Here (required if you want API monitoring through Discord)",
  "discordAdminIDs": ["discord IDs of people who can run commands go here", "Like this"],
  "discordChannelID": "the channel you're trying to send api monitor updates to",
  "prefix": "enter prefix for bot commands here"
}
```
On the `key` field, enter a password if you wish the server to be private. On the `domain` field, enter the domain you want to use for the server.

> Psst, if you are a donator, you can get a free only-fans.club subdomain.

If you wish to create a **public** image server, set `public` option to true. Now, set the `port` and the `securePort` to the port that your server has. Finally, on the `key` field inside the `admin` category should be the same as the key you set on the 1st line.

## Step 4 - Proxy the server
Go to the DNS management of your domain, and create an A type record that points to `164.132.74.251`. Then, head over to the commands channel - for the last time - and use the `DBH!server proxy <your_domain> <server_id>` command.

## Step 5 - Starting the server
Now, press the start button to start your server. It should report no errors, and you shall be able to access your server at the domain you used.

## Any issues? Don't worry!
If you have any issues you may ask for help in our discord server. Thanks for reading this guide.