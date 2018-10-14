# introlinux1
Steps to our Linux workshop 1

Thank you to those who made the workshop! If you didn't, here are all the instructions for setting up a vmware ubuntu machine, then installing a simple file web server on it. I include some other things you can do or check out after you've done this.
I really encourage you to try this install on a home machine (look up "how to make ubuntu bootable usb").
The installation steps will be exactly the same once you get a machine to boot to your usb.

Feel free to reach out to me(Dennis) or K on Discord!
Dennis | Menace#0040  and Turb0Yoda#2222


<h1>Install the linux virtual machine</h1>

1. Click create new virtual machine

2. Hit typical install

3. Click on I will install the operating system later

4. Choose linux, and click on ubuntu from the dropdown box

5. Give your machine a name, ubuntu will do

 - The default disk size will do
 
7. click customize hardware

8. Click on New CD

9. Use ISO image file: Browse to desktop. Go into the ISO folder.

10. Select ubuntu-16.04.5-desktop-amd64

11. Click close and finish

12. Start the machine and click install ubuntu

13. Check download updates while installing

14. Click erase disk and install ubuntu

15. Click and drag window to see continue button. Click continue

16. Enter your name and choose a password

17. Click restart now



<h1>Install VMwareTool</h1>
18. Login to your ubuntu install!

19. Go to the top bar in the VMware app and click on VM.

20. Click on install tools

21. Click on the ubuntu button in the top left

22. Search for the terminal. Open it

 - ls to see what is in your directory-
 
24. cd into the root directory. (/)

25. cd into media (keep going into the VMware tools)

26. ls -l to show everything in the directory

27. sudo tar -xzvf VMwareTools*.tar.gz -C ~/Desktop

 *- The little squiggle is equivalent to the home directory of the current user (/home/currentUser)*
 
 *- the x is to untar the file (it is short for extract)*
 
 *- z is to unzip the file*
 
 *- v stands for verbose, so it will show you more of what it is doing. Don't put this and you get less output*
 
 *- f let's you pick the file on which you want to operate*
 
 *- C is short for create (I think). Basically creates a file where you specify (if you just enter  	a directory like /home/billy/Desktop/)or it can even specify the filename 			(/home/billy/Desktop/theNameYouChoose)*
 
28. cd ~

29. ls

30. cd vmware-tools-distrib/

31. sudo ./vmware-install.pl -d

32. reboot

