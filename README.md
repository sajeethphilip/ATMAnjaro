# ATMAnjaro
ATMA on Manjaro Linux XFCE - best option for laptops running on battery. 

One great consideration everyone have is good backup time and availability of all necessary software on their laptops. Manjaro linux on XFCE is best in this. So, what I have here is a custom made Manjaro Linux with the ATMA software on top of it.

What is the advantage?

You create a Ventoy disk (https://www.ventoy.net/) using their GUI version to reserve a reasonable work space. For ATMANJARO, you may need something like 6BG and the remaining can be your work space in linux ext4 format. Create a folder named atma in the workdrive. Give it only root permission so that only root can view the files in that folder.

Download ATMANjaro_science.iso image (https://drive.google.com/file/d/1MHza_dHHmo56409k5OJlaM5e4aOjxyVL/view?usp=sharing) to the Ventoy folder. 

Thats all.

Boot you computer from the USB drive that has the Ventoy partition. It will take you to the Manjaro installation with a custom screen of two kids walking to a forest holding their hands. Yes, that is the moto - a helping hand to everyone to computing!

Open a teminal from Manjaro menu and type su (super user). It will take you to the root prompt. Now, type sos. You may see a set of messages flagging up. Ignore them and just add a user - yourself (useradd -m -p \<user name\>) with a password (passwd \<user name\>)

Go to the logout menu and select switch user. You can find your name in the list that shows up. Login and lo, your account will be created under the atma folder in work area. That mean, though you are working on a live CD, all that you do will be saved here!. After setting up your favourite screen, (I recommend trying verity from the Accessories menu to get on the fly images and an onscreen  clock as well. But that is up to you.) log out and login to manjaro. In the previous terminal, type sos again. That is when all your work will get saved to the atma folder. So if you did not want anything that you did to be retained, just skip this step and reboot! A good option to just demo your system. But if you run sos, from next time onwards, your browser and other online cache will get written to this new folder and will be presistent across reboots.

I find this convenient because (1) you can work on the same set of programs and in your folder by just booting with the pendrive from your friends or a public computer without risking any of your data or getting a visrus into your system. (2) It consumes very less power that you will find that your backup time has more than doubled! (3) you need not have to carry your laptop anymore. Just find a public machine and the permission to boot into it. Cool. Enjoy! What is life if you can't enjoy! 
