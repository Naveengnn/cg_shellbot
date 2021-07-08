# fclone shell bot V2.0

[Tutorial FAQ](https://git.io/JJZ3E) [Original Tutorial](https://git.io/JJZ30) [Script 1.0 Manual Tutorial](https://git.io/JJZ34)

`shellbot` can mobilize and run VPS commands on TG. This script is only a google drive dump application of shellbot!

Of course, the transfer tool is very important, `fclone`, 400 fils/s, yes, speed is about files, although there are other advantages, but a speed can already be worthy of its name fxxk clone, world martial arts, in order not to break, If you use fclone, other clones can only see your back.

<img src="https://github.com/cgkings/gclone_shell_bot/blob/master/images/bot.gif" height="420px" width="270"/> <img src="https://github. com/cgkings/fclone_shell_bot/raw/master/images/main.jpg" height="420px" width="270"/> <img src="https://github.com/cgkings/fclone_shell_bot/raw/master/images /chat2.jpg" height="420px" width="270"/>

**Note:** One-click installation and configuration scripts only support (Ubuntu/Debian) temporarily, centos can be installed manually, and windows cannot be installed! ! !

## Installation steps: <hr />

<details>

<summary>Step 1: Clone the library/grant script permissions/run one-click installation script</summary>

 

```

cd /root && git clone https://github.com/cgkings/fclone_shell_bot.git && chmod -R 777 /root/fclone_shell_bot && mv /root/fclone_shell_bot/fcshell.sh /root && /root/fcshell.sh

```

</details>

<details>

<summary>Step 2: Use one-click installation script</summary>

<details>

  <summary>Use scenario I: Complete installation</summary>

  If you are using the fclone shell bot for the first time, please follow the steps below **0 Complete installation**:

  1. Click **0 Complete installation**

  2. Click **10 Modify bot configuration** (optional)

     Fill in the bot’s token and your TG ID, don’t know what this is? Ask the customer service staff at the end of this article

     

     According to the test, the bot configuration is changed, and when you start the bot, you will also be asked for bot token and TG id.

              

  3. Click **15 Modify script dump parameter ini**

   

     3.1 Fill in your clone account name

         

         ** is the name in [] displayed by rclone config show**

         

         ** Of course, in the one-click script, click 11 to view the rclone configuration, and you can also see it **

         

     3.2 Fill in the transfer ID

         

         **gd_id\jav_id\mdv_id\book_id, if these names are changed, you need to modify the script accordingly. It is recommended to modify only = back, ID in ""**

     

     3.3 Modify the dump parameters (optional)

         

         Go to [this tutorial FAQ](https://github.com/cgkings/fclone_shell_bot/blob/master/help/MY_FAQ.md)

  4. Click **5 to start bot**

     The default is to start the bot in the background. I can’t see any running ones at the moment. Would you like to see it? `tmux a -t shellbot` to see it in the background

     

     Because of the original problem, the first time you click to start, please `tmux a -t shellbot` to the background to complete the following operations:

     

     4.1 Fill in the BOT token

     

     4.2 Send messages randomly in the bot on TG

     

     4.3 When you return to vps, your TG ID should be recognized, and you can just reply with y

     

     4.4 After running the configuration successfully for the first time, run `node server` again to start it, or use the configuration script 5 to start it from that dialog.

     

     In the future, you don’t need to go to the background. Unless the bot has an exception, you don’t need to go to it if there is an exception. Just click the script to restart the bot

  5. Click **13 to view script shortcut commands**

   

     5.1 Copy shortcut commands

     5.2 TG find [bot big father](https://t.me/BotFather), select your bot, enter `/setcommands`, paste the shortcut commands

     5.3 On your bot, in the chat bar, click [/] and select the function you want to use!

  </details>

  <details>

  <summary>Use scenario Ⅱ: Partial installation</summary>

  If you have already installed the environment or shellbot, you can click to install it according to your needs

  **Note: No matter how you choose, `4 install update dump script` is indispensable, that is for permissions, aliases for scripts, if you don't install it, you won't be able to use scripts if you enter bot!

  **Note: If `fclone version` does not display the version number, it means that your fclone has not been successfully installed and the dump script cannot be successfully transferred. Please enter the following command to install fclone manually:

```

wget -N https://github.com/cgkings/fclone_shell_bot/raw/master/fclone/fclone.zip && unzip fclone.zip && mv fclone /usr/bin && chmod +x /usr/bin/fclone

```

  

  </details>

  </details>

  

**Above, the installation is basically explained. If you still don’t understand, I suggest you go to [original author’s tutorial](https://github.com/botgram/shell-bot) or [the previous version of this script’s tutorial ](https://github.com/cgkings/fclone_shell_bot/blob/master/help/Manual_README.md)

## Instructions for use: <hr />

<details>

<summary>/fq speed dump</summary>

 

Support task queue

</details>

<details>

<summary>/fsort automatic sorting</summary>

1. Generate the jason file:

For the folders you want to organize, for example, by number, you go to the existing number folder (the reason is the same, the actress name is the same), run the following command: <br>

  

`fclone lsjson your username: {folder ID} --fast-list --dirs-only --no-mimetype --no-modtime --max-depth number of folder levels` <br>

  

Get information similar to the following:<br>

  

`{"Path":"S/SSNI","Name":"SSNI","Size":-1,"ModTime":"","IsDir":true,"ID":"10n2Vz5vdzwg_mgJSWAiT190xMkztnvRx"},` <br>

`{"Path":"S/SSPD","Name":"SSPD","Size":-1,"ModTime":"","IsDir":true,"ID":"1mqNfuJUiTmwqaY9aC90YQFVFDJWji9WE"},` <br>

`{"Path":"S/STAR","Name":"STAR","Size":-1,"ModTime":"","IsDir":true,"ID":"1nxBRq5Jg8gzR71wrAaI2up0IP-ucFh4z"} ,` <br>

  

Because I am not good at learning skills, I need to process this jason information. Copy it to excel and display it in columns. Delete redundant columns and merge them into this format:

  

`SSNI:10n2Vz5vdzwg_mgJSWAiT190xMkztnvRx`

`SSPD:1mqNfuJUiTmwqaY9aC90YQFVFDJWji9WE`

`STAR:1nxBRq5Jg8gzR71wrAaI2up0IP-ucFh4z`

  

Overwrite and paste this information into \root\fclone_shell_bot\av_num.txt (the original file is my category name and folder ID)<br>

  

2. Run the fsort script

  

The most critical step is step 1. As long as your first step is correct, the script will ask you to enter the ID of the folder that needs to be organized, and then the script will do the following: <br>

⑴ Traverse the file name in the folder to be sorted;<br>

⑵ Compare with keywords in av_num.txt, if the file name contains keywords, this file will be **moved** to the keyword folder;<br>

⑶ Delete the empty folders in the organized folder; <br>

⑷ ⑴——(3) Steps loop until the file name of the file in the folder does not contain the keywords in av_num.txt. <br>

</details>

## Authorization Letter<hr />

When launched for the first time, the bot will only accept messages from your users. For security reasons: you don't want anyone to issue commands to your computer! <br>

If you want to allow other users to use the bot, please use /token and provide a link to the result. If you want to use this bot on the online forum, /token will send you a message to be forwarded to the online forum<br>

## Final words<hr />

Sending you a thousand words, there will always be a difference. As a little white, I can publish shamelessly on github because of the open development atmosphere of github, and also because of the selfless help of open and enthusiastic Chinese technology bigwigs on TG. I would like to thank you all TG gods, in no particular order:<br>

* fxxkrlab (professional adventurer) I hope that we can learn more languages, and we have compiled [转存bot textbook](https://github.com/fxxkrlab/iCopy) according to our needs. Unfortunately, we haven't studied it yet. <br>

* aevlp (steve x), the originator of the dumping script, selflessly provided the dumping bot that uses mysql to realize the dumping task sequence. Unfortunately, it has not been researched for the time being.<br>

* Ip2N5M (Kali Aska) Little white gospel, no textbooks, no cases, answers and tools directly, thanks to the core code of the script and [魔改版gclone](https://github.com/mawaya/rclone) , The magic changed the gclone of rclone, experience it<br>

* shine_y (shine) The original author of the one-click dump script I modified, thank you very much, [Address](https://github.com/vcfe/gd) <br>

* Onekingen (oneking) is a small partner on the road to the magic change of scripts. I have done a lot of custom scripts, [Address](https://github.com/vitaminx/gclone-assistant) <br>

* GreatPanoan (Panoan) took me to the guide who bought the chicken and did not return. Without him, I would not start this tossing journey. Anyway, I wish the college entrance examination a success, kid! <br>

In addition, [hrvstr](https://github.com/) on github, he provided a template of custom commands on shellbot, thank him very much<br>

Of course, the original author of shellbot [Botgram](https://botgram.js.org) is indispensable <br>

Finally, if you are a foreign friend, it is an honor, Sun Thief, use Google Translate!

## Customer Service List<hr />

#### [Tutorial FAQ](https://github.com/cgkings/fclone_shell_bot/blob/master/help/MY_FAQ.md)

#### 1#Customer Service: [@谷哥](https://www.google.com);

#### 2#Customer Service: [@度娘](https://www.baidu.com);

#### 3#Customer Service[@TG Group Robot](https://t.me/sharegdrive)
