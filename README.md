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

<h1>Server Install</h1>

33. sudo apt-get install apache2

34. press y and enter to confirm

35. cd /etc/apache2/sites-available/ go to the apache configuration directory

36. sudo nano 000-default.conf //open the document with nano text editor

37. change document root to /var/www

38. Ctrl+O to save. save with same filename (just hit enter)

39. Ctrl+X to exit

40. sudo systemctl restart apache2 *(to restart and apply configs)*

41. Place any files you want to share on your network in /var/www/

<h1>Accessing the files</h1>
42. On the ubuntu machine, run ifconfig or "ip addr" to find the ip address

43. On any computer on your network, open a web browser like chrome or firefox

44. Enter the ip address into the url bar and hit enter
   *-You now have access to all those files!*


<h1>More things you can do</h1>
45. Install and try using vim instead of nano
  **If you get permission errors when you are working on things, look up file permissions in linux**
  **Fairly simple commands to modify who can use what on the system. Look up chmod and chown.**
  **We may go over these in a later workshop**

46. Look up how to install a samba server.
  *-Legit file sharing so that you can upload and download files as easily as if you plugged in a usb*
-Use what you learned in overthewire wargames! Google it if this sentence confuses you.
-Look up other servers that might help around the house
-Come to events and talk to SWIFT about how you can get involved/learn with us!


<h1>Instructions on using a different directory than /var/www/</h1>
This step basically permits other directories to be accessed instead of just the /var/www/ directory
47. go to /etc/apache2

48. sudo nano apache2.conf

49. use control w (stands for where is) to find "directory"
  *-edit "Require all denied" to "Require all granted"*

50. Ctrl+O to save. save with same filename (hit enter)

51. Ctrl+X to exit

52. create a directory where you want to store things for the website. (for this example, I will use /home/billy/www)
 *-The command to do this will be "mkdir /home/billy/www"*

53. edit the 'document root' in /etc/apache2/sites-available/000-default.conf like you did before, except type /home/billy/www instead.

54. Restart the server and check it out!


<h1>Instructions on setting up a home server without using any additional hardware</h1>
(For that shared home computer)

55. Install the vm as described above

56. Go to the VM's settings and use a bridged adapter. This basically sets your VM to act as if it is an actual computer on your home network.
**You should now be able to access the files on that VM from any computer on your network.**
