# Twitch-and-toot

Twitch-and-toot is an open source project that allows you to post to Mastodon when a streamer is live on Twitch. It is built on NodeJS and can run on a RaspberryPi, Single Board Computer, Linux VPS, or a private server.
Requirements and Prerequisites

    NodeJS installed on the device that you plan to run the script on.
    A Twitch API key (client ID and secret) which can be obtained from the Twitch Developer Dashboard.
    A Mastodon API key (access token) which can be obtained from your Mastodon instance.

## Installation

    Clone the Github repository to your device: git clone https://github.com/ChiefGyk3D/twitch-and-toot.git
    Install the required packages: npm install
    Create a config.json file based on the config_template.json file in the repository. Fill in the required information such as Twitch API key, Mastodon API key, and the channel name you want to track.
    Run the script: node twitch-and-toot.js

## Configuration

The configuration file config.json is used to store the required information such as Twitch API key, Mastodon API key, and the channel name you want to track. 

You can also customize the messages that will be posted to Mastodon when the streamer is live, but you currently must keep a total of five (5) messages for the array to work properly. And they are customized directly in the script. I hope in the future to move it to config.json

## Modules

The auth.js, channelData.js, and getStreams.js modules are borrowed from Twitch-Discord-Bot. They are used to obtain the required information from the Twitch API and post to Mastodon.

## Future plans
    
    Move Mastodon message choices to config.json and unhinge it from the five message option requirement
    Consolidate the last post time information into the config.json file.
    Add messaging for when the stream ends to post to Mastodon and thank followers.
    Create a SystemD service to keep the script running and boot with the device hosting it.

## Donations and Tips

If you would like to support the development of Twitch-and-toot, you can donate through the following links: https://links.chiefgyk3d.com

You can also tip the author with the following cryptocurrency addresses:

    Bitcoin: bc1q5grpa7ramcct4kjmwexfrh74dvjuw9wczn4w2f
    Monero: 85YxVz8Xd7sW1xSiyzUC5PNqSjYLYk4W8FMERVkvznR38jGTBEViWQSLCnzRYZjmxgUkUKGhxTt2JSFNpJuAqghQLhHgPS5
    PIVX: DS1CuBQkiidwwPhkfVfQAGUw4RTWPnBXVM
    Ethereum: 0x2a460d48ab404f191b14e9e0df05ee829cbf3733

Author

ChiefGyk3D is the author of Twitch-and-toot, with assistance from Y-Love to educate on NodeJS. ChatGPT helped build about 80% of the template
