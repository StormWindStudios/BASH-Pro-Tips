# BASH Pro-Tips
Tips for efficiently navigating the BASH commandline interface

## Re-run the Last Command as Sudo
People commonly forget to use sudo when running commands that require elevated privileges. To rerun the command as the sudo user, you can use **sudo !!**

```console
user@company:~$ apt-get install -y cowsay
E: Could not open lock file /var/lib/dpkg/lock-frontend - open (13: Permission denied)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), are you root?
user@company:~$ sudo !!
sudo apt-get install cowsay
[sudo] password for user: 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
cowsay is already the newest version (3.03+dfsg2-4).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded. #test
```
## Re-use the Last Argument 
Sometimes we need to use arguments from previous commands. We can avoid typing them out manually by using the **alt+.** shortcut, which will cycle through the arguments you've recently used. 

## Move Around Long Commands Quickly
Modifications can be a pain to make in a long command if you're using just the left and right arrow keys. The following shortcuts are helpful.

* **ctrl+a:** move to the beginning of the line
* **ctrl+e:** move to the end of the line
* **alt+b:** go backward one word
* **alt+f:** go forward one word
