# introlinux1
Steps to our Linux workshop 1

Thank you to those who made the workshop! If you didn't, here are all the instructions for setting up a vmware ubuntu machine, then installing a simple file web server on it. I include some other things you can do or check out after you've done this.
I really encourage you to try this install on a home machine (look up "how to make ubuntu bootable usb").
The installation steps will be exactly the same once you get a machine to boot to your usb.

Feel free to reach out to me(Dennis) or K on Discord!
Dennis | Menace#0040  and Turb0Yoda#2222



1)**Install the linux virtual machine**

* Click create new virtual machine
* Hit typical install
* Click on I will install the operating system later
* Choose linux, and click on ubuntu from the dropdown box
* Give your machine a name, ubuntu will do
* The default disk size will do

* click customize hardware
  -Click on New CD
  -Use ISO image file: Browse to desktop. Go into the ISO folder.
  -Select ubuntu-16.04.5-desktop-amd64

*Click close and finish
*Start the machine and click install ubuntu
*Check download updates while installing
*Click erase disk and install ubuntu
*Click and drag window to see continue button. Click continue
*Enter your name and choose a password
*Click restart now



2)**Install VMwareTools**

*Login to your ubuntu install!
*Go to the top bar in the VMware app and click on VM.
*Click on install tools
*Click on the ubuntu button in the top left
  -Search for the terminal. Open it
  -ls to see what is in your directory
  -cd into the root directory. (/)
  -cd into media (keep going into the VMware tools)
  -ls -l to show everything in the directory
  -sudo tar -xzvf VMwareTools*.tar.gz -C ~/Desktop
    * The little squiggle is equivalent to the home directory of the current user (/home/currentUser)
    * the x is to untar the file (it is short for extract)
    * z is to unzip the file
    * v stands for verbose, so it will show you more of what it is doing. Don't put this and you get less output
    * f let's you pick the file on which you want to operate
    * C is short for create (I think). Basically creates a file where you specify (if you just enter  	a directory like /home/billy/Desktop/)or it can even specify the filename 			(/home/billy/Desktop/theNameYouChoose)
  -cd ~
  -ls
  -cd vmware-tools-distrib/
  -sudo ./vmware-install.pl -d
  -reboot
