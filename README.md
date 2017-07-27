Please Start Here
====================
http://www.everydaylinuxuser.com/2015/11/how-to-install-ubuntu-linux-alongside.html

If the link is broken here are it's contents
=============================================

How To Install Ubuntu Linux Alongside Windows 10 (UEFI) 
Posted by Gary Newell  |  at  22:12 222 comments 


Introduction
Updated For Ubuntu 16.04

Windows 10 has been out for a while now and as I have a track record for writing dual boot guides I thought it was about time I created a Windows 10 and Ubuntu dual boot guide. 

This guide focuses on computers with a Unified Extensible Firmware Interface (UEFI) over a standard Basic Input Output System (BIOS). Another guide will be coming out shortly to cover the BIOS version.

What this means is that if you were using Windows 8 and 8.1 before upgrading to Windows 10 then this guide will work for you. If you have just bought a brand new Windows 10 machine and it has a standard hard drive (i.e it isn't a Surface Pro) then this guide will also work for you.

If your computer used to run Windows 7 before upgrading to Windows 10 then it is highly probable that this guide isn't suitable in which case you should follow this guide. 

How can you tell if your computer has a UEFI over a standard BIOS? 


In the search box at the bottom of the screen type "System Information" and when the icon appears at the top click on it.


Halfway down the right panel there is an item called BIOS mode. If it says UEFI then this guide will work for you.

Steps For Dual Booting Windows 10 And Ubuntu
The steps required for dual booting Windows 10 and Ubuntu are as follows:

Backup your Windows 10 operating system (optional but highly recommended)
Create a Ubuntu USB drive
Enable booting from a USB drive
Shrink the Windows 10 partition to make space for Ubuntu
Boot into Ubuntu live environment and install Ubuntu
Amend the boot order to make sure Ubuntu can boot
I have written another guide which shows how to dual boot Ubuntu and Windows 10 on a computer with an SSD. This is largely experimental as it is my first time of doing it but it does work for me and it might give you some ideas when partitioning your SSD.
Back Up Windows 10
In the list of steps above I have put this down as an optional requirement but I can't stress highly enough that you should really do it.

Let's imagine for a moment that you have a machine that used to run Windows 8 and you spent the time upgrading to Windows 10.

If you follow this process and for whatever reason it doesn't work and your machine is left in an undesirable state then without a backup the minimum it will cost you is the time it takes to reinstall Windows 8 and then upgrade to Windows 10.

 
Imagine now that you don't have the Windows 8 media and you don't have a viable recovery partition. You now have no way of getting Windows back without buying either the Windows 8 disk which costs around £90 or a Windows 10 disk which costs £199. You would also have to find and download any required graphics, audio and other drivers required for Windows to run properly.

I have written a guide (linked below) which shows you how to backup all of your partitions using a tool called Macrium Reflect. There is a free version of the tool available and the most this tutorial will cost you is time and if you don't have one an external hard drive or a spindle of blank DVDs.

Click here for my guide showing how to backup Windows 10.



Create A Ubuntu USB Drive
There are many tools out there for creating a Ubuntu USB drive including UNetbootin, Universal USB Creator, YUMI, Win32 Disk Imager and Rufus.

Personally the tool that I find most useful for creating Linux USB drives is Win32 Disk Imager. 

I have written a guide showing how to create a Ubuntu USB drive. 



It shows you how to do the following things:
How to get Win32 Disk Imager, 
How to install Win32 Disk Imager.
How to format a USB drive.
How to create a Ubuntu USB drive
How to set the power options in Windows 10 to allow booting from USB
How to boot into a Ubuntu live environment
You will obviously need a USB drive for this purpose.

Click here for a guide showing how to create a Ubuntu USB drive.


If you would prefer to, you can buy a USB drive with Ubuntu already installed on it.

If you want to get the USB drive back to normal after installing Ubuntu follow this guide which shows how to fix a USB drive after Linux has been installed on it.
Shrink Windows To Make Space For Ubuntu
If your computer only has one hard drive you will need to shrink your Windows 10 partition in order to make space for Ubuntu.

Click here for a guide showing how to shrink your Windows 10 partition.

Boot Into Ubuntu Live Environment
Make sure that the Ubuntu USB drive is plugged into the computer.

If you backed up your computer using Macrium and you chose to create the Macrium boot menu option then you can simply reboot your computer. 


When the above screen appears click on the "Change defaults or choose other options" link at the bottom of the screen.

If you chose not to create the Macrium boot menu option boot into Windows, insert the Ubuntu USB drive, hold down the shift key and reboot your computer. (Keep the shift key held down until a screen similar to the one below appears).



Each manufacturer has a different version of UEFI and so the menu options may be different.

The important thing is that a blue screen with white writing appears.

You are basically looking for the option to boot from the USB drive and this may take some finding. From the image above I chose the “Choose other options” menu item which produced the screen below.




I then clicked on the “Use a device” option which as you can see has the subtext “Use a USB drive, network connection or Windows recovery DVD”. 



A list of devices will now appear.

This isn’t the first time I have installed things on this computer and my EFI partition still has links to old Ubuntu versions.

The important link on this screen is the “EFI USB Device” option.

Choose the EFI USB Device option and Ubuntu should now boot from the USB drive. 



A boot menu will appear.

Choose the first menu option to try Ubuntu.

A large dialogue window will appear with options to install Ubuntu or to Try Ubuntu.

Click on the “Try Ubuntu” option. Ubuntu will now be loaded as a live session. You can try out all of the features of Ubuntu but if you reboot all the changes will be lost.

Install Ubuntu
To start the installation click on the “Install Ubuntu” icon on the desktop.

After clicking on the “Install Ubuntu” option the following screen will appear:


This is the beginning of the installation process and you can select the language which is used to help you through the process.

Choose your language and click “Continue”.


The installer has changed a little bit for Ubuntu 16.04. The pre-requisites screen has been removed as has the option to connect to a wireless network prior to installing.

The preparing to install Ubuntu screen now simply lists the option to download updates (which is only available after you have an internet connection) and the option to install third party software for playing MP3 audio and watching Flash.
If you have a decent internet connection then you might wish to install updates during the installation.

To connect to the internet click on the network icon in the top right corner and a list of wireless networks will be listed. Click on the network you wish to connect to and enter the security key when prompted.

You will need to click the back button on the "preparing to install Ubuntu" screen and then click continue again when you are back at the welcome screen.

If you have a poor internet connection then I would choose not to connect to the internet. You can update your system after it has been installed.

You can choose to install the third party tools for playing MP3 audio as part of the installation process now by checking the box or you can do it after the system has been installed.

Click "Continue".









The “Installation Type” screen lets you decide whether you want to install Ubuntu alongside Windows or over the top.

Choose the “Install Ubuntu alongside Windows Boot Manager” option.


Click “Install Now”.



A window will appear showing you what is going to happen to your disk. By default the Ubuntu installer will create an ext4 partition for Ubuntu and all of your personal files and a swap partition used for swapping idle processes when memory gets low.


Click “Continue”.



A map of the world will appear. The purpose of it is to make it possible for Ubuntu to set the time on your clock correctly.


Click where you live on the map or start typing it into the box provided and then click “Continue”.


Almost there. Just two more steps before Ubuntu is installed.

You now need to choose your keyboard layout. Select your keyboard’s language in the left pane and then the actual physical layout in the right pane.

Alternatively click on the detect keyboard layout option and it will more than likely do it for you.

Test out the keyboard layout that you have chosen by typing into the box provided. Specifically try out symbols such as the dollar sign, pound symbol, hash tags, speech marks, slashes and other special characters as these are the keys that tend to move around on a keyboard.


Click “Continue”.


The final step is to create a default user. 

Enter your name and give your computer a name. 

Enter a username into the box provided and choose a password and repeat it.

Click on the “Require my password to log in” option. I don’t really recommend anyone letting their machine log in automatically unless it is a virtual machine used for test purposes.


Finally click “Continue”.



The files will now be copied to your computer.



When the process has finished you will have the options to continue test or to restart now. 

Choose the “Continue Testing” option.

Change The Boot Order So That Ubuntu Can Boot
You will need to be connected to the internet for this to work.

Click on the network icon in the top right corner and choose your wireless network (unless you are connected with an Ethernet cable). Enter the security key.

Open up a terminal window by either pressing CTRL ALT and T at the same time or click the top icon in the bar on the left side and type “term” into the search box.  Click on the terminal icon that appears.



Type sudo apt-get install efibootmgr into the terminal window.

When asked whether you want to continue press “y”.


After the installation has completed type efibootmgr into the terminal window.

A list of boot devices will appear. 


As you can see in my list there are the following boot options:

boot0000 for Ubuntu (this is an old version and can be ignored)
boot0001 which is Windows
boot0002 and boot0003 are two LAN devices
boot0004 which is the new version of Ubuntu that I just installed
boot0005 is my USB device
boot0006 and boot0007 are two other LAN devices
boot0008 is another USB device

At the top of the text you will see that my current boot device is boot0005 which is the USB device. 

More importantly is the boot order which is listed as 0001,0000,0004,2001. 

What this tells me is that the computer will boot Windows first, then the rubbish version of Ubuntu, then the new version of Ubuntu and finally a USB device.

This is clearly incorrect.



To change the bootorder all you have to do is enter the following command:

·         sudo efibootmgr –o 4,1

The –o says that I want to change the order. Then all I have to do is list the order I want things to boot.

So in the command above I have stated I want Ubuntu to boot first and then Windows. 

Type exit into the window and reboot the computer by clicking the icon in the top far right corner of the screen.

Choose to shutdown and reboot your computer.


When given the option and before the computer actually reboots remove the USB drive. 

Now when you restart your computer a menu will appear with options for booting into Ubuntu and Windows 10.


Try them both out and hopefully you will have successfully installed Ubuntu alongside Windows 10.

What Next
Check out my new guide which shows how to show common applications such as Chrome, Dropbox and Steam easily in Ubuntu.
The Antidote
If you have followed this guide and you want Windows back the way it was before you installed Ubuntu follow this guide:
