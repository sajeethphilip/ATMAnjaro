# ATMAnjaro

## Additions
1. The sos command has been replaced by the command "atma" and sos now will start a cron job that allows you to specify where to backup your data. You can specify the machine IP, the folder in the backup machine, your folder name and it will set up a cronjob to backup your files to the remote machine every 15 mins. You can check with crontab-l command to make sure that the job runs.
2. atma command will ask for a new root user password. This password will be used only for the session and will not affect the root password on the host system. So you can use any random password for this. You will need it to return to the host system after finishing your atma avathar. Here is some more detail on how to enter and exit an atma avathar:
    (a) On the host system, be it be a laptop with installed version of ATMAnjaro or a live session, nsert the USB drive with a folder atma/home/<your avathar user name> in it. Now, login as root with your root password for the host system and call atma. It will detect the USB drive that you inserted last and look for he folder atma in it. Because you already created it, it will copy the important information for the session in this folder. 
    (b) The system will now ask you for a root password. THis will be the root password for the session. If you are doing it for someone else, keep this password private. Otherwise, the avathar can have access to the entire system through this root password.
    (c) That's it. Now you have to logout from the host system. You can use switch user also, in which case, on return you will be taken back to the workspace you have been with all your files in place, as soon as the atma avathar leaves the machine!
    (d) Before loging out,create a user <your avathar user name> with a password for yourself. This is needed only for the first time you run atma on the USB.
    (e) log out from the machine or switch user to the login screen where you find that your name is now in the list. login and lo, you are on the system.
    (f) After finishing, take a terminal and become root with the password for root that you created for the session. Call atma again. It will now do the house cleaning and will tell you that you are safe to leave. Logout and unplug your USB.
    (g) You will notice that the login screen do not have your name anymore! When the host machine user login, he will be taken back to his switched environment as if nothing had happened! No memory of the atma avaar is left in the system!
    (h) It is also possible for having another atma session with a new USB in an avathar session. At this time, the previous atma avatar will be pushed out and the new will take its place. On return, the machine will switch back to the host system and not to the previous avatar.

------------------OLD doc continues-----------------
  
ATMA on Manjaro Linux XFCE - best option for laptops running on battery. 

One great consideration everyone have is good backup time and availability of all necessary software on their laptops. Manjaro linux on XFCE is best in this. So, what I have here is a custom made Manjaro Linux with the ATMA software on top of it.

What is the advantage?

You create a Ventoy disk (https://www.ventoy.net/) using their GUI version to reserve a reasonable work space. For ATMANJARO, you may need something like 6BG and the remaining can be your work space in linux ext4 format. Create a folder named atma in the workdrive. Give it only root permission so that only root can view the files in that folder.

Download ATMANjaro_science.iso image (https://drive.google.com/file/d/15Ak7UAeTI1Td4q9rsg3obm55TH9MYo9p/view?usp=sharing) to the Ventoy folder. 

Thats all.

Boot you computer from the USB drive that has the Ventoy partition. It will take you to the Manjaro installation with a custom screen of two kids walking to a forest holding their hands. Yes, that is the moto - a helping hand to everyone to computing!

Open a teminal from Manjaro menu and type su (super user). It will take you to the root prompt. Now, type sos. You may see a set of messages flagging up. Ignore them and just add a user - yourself (useradd -m \<user name\>) with a password (passwd \<user name\>)

Go to the logout menu and select switch user. You can find your name in the list that shows up. Login and lo, your account will be created under the atma folder in work area. That mean, though you are working on a live CD, all that you do will be saved here!. After setting up your favourite screen, (I recommend trying verity from the Accessories menu to get on the fly images and an onscreen  clock as well. But that is up to you.) log out and login to manjaro with the password same as manjaro. In the previous terminal, type sos again. That is when all your work will get saved to the atma folder. So if you did not want anything that you did to be retained, just skip this step and reboot! A good option to just demo your system. But if you run sos, from next time onwards, your browser and other online cache will get written to this new folder and will be presistent across reboots.

I find this convenient because (1) you can work on the same set of programs and in your folder by just booting with the pendrive from your friends or a public computer without risking any of your data or getting a visrus into your system. (2) It consumes very less power that you will find that your backup time has more than doubled! (3) you need not have to carry your laptop anymore. Just find a public machine and the permission to boot into it. Cool. Enjoy! What is life if you can't enjoy! 

# Installing to a PC

You can install ATMAnjaro to a PC from the install menu just like you do a manjaro installation. sos will still be there in the installed version but use it with care!You can insert a USB with folder atma and your saved working environment and call sos to switch over to the USB. Now the installed system will be locked. Logout and log in to the USB environment. Once finished, login as root with your root password (default is manjaro) and run sos again. This should display that you are safe to remove the USB. Logout and unplug the USB. The system should now be ready to run the installed ATMANJARO in the system. If you accidently switch off or reboot the system without running sos for the second time, the files in the computer will be safe but will be inassessable. This is because the sos has replaced the system passwd file and group file with the USB version. You will have to either reinstall or manually edit the password and group files to get access to the system folders! So beware of it!!
