# Haruki version 2.0 

* This page is meant to document the development of Haruki
* See ABOUT for more info about the bot


----
@ HarukiV2.0 03/01/23
----

### File Changes
* Commands from communicate and help cog has been merged with useful cog
* LaunchHaruki and Haruki have been merged into HarukiMain

### Admin
* List of commands converted to slash commands:
  * `deletesongs` (Owner only)
  * `viewdownloaded` (Owner only)
  * `reboot` (Owner)
  * `shutdown` (Owner)
  * `serverlist`
  * `restart` (owner)

### Fun
* [on_member_join] function has been removed
* `gtn` has been separated into 2 commands:
  * `gtn` for choosing game settings
  * `guess` for guessing the number
* {Haruki.jpg} has been replaced with {Haruki2.jpg} in `about`
* [Link](https://github.com/blizt42/Haruki2.0/wiki) to Git hub page have been updated
* `praise` has been changed to `praise_bot`
* `rp` has been changed to `random_picture`
* `yeetball` output has been modified as an embed
* `action` and `emote` have emote variables unrestricted
* `azur` has been renamed `azurlane`
* List of commands converted to slash commands:
  * `gtn`
  * `about`
  * `hi`
  * `ping`
  * `praise_bot`
  * `reddit`
  * `random_picture`
  * `yeetball`
  * `action`
  * `emote`
  * `azurlane`
  * `cat`

### Music
* module [pytube] have been temporarily disabled
* Updated [MusicPlayer] class to work using interaction
* Updated [get_MusicPlayer] function to work using interaction
* `queue` has been renamed `spotifylist`
  * command modified to only accept spotify playlist
  * YouTube playlist will be updated into a new command next update
  * queuing single mp3 has been removed. use `play` to queue them
* List of commands converted to slash commands:
  * `play`
  * `join`
  * `spotifylist`
  * `playqueue`
#### Known Issues
* Bot does not disconnect after being inactive 
* no response when `view` is used in another server when user and player in another server's channel
* interaction does not work with voice_client, hence some commands have not been converted to slash
  * view
  * skip
  * stop
  * pause
  * resume

### Useful
* `help` have been moved here from Help cog
* `dm` and `dma` have been merged and moved here from Communicate cog
* `search` has been removed
* List of commands converted to slash commands:
  * `help`
  * `clear`
  * `flip`
  * `direct_message` from `dm` to `dma`

>"New year, new gear" ~Haruki

----
