# THM-Writeups
This will be a repository featuring notes taken from THM rooms. 

# Symbols and Operators: 
1. & - Runs commands in the background
2. && - Combines multiple commands together in one line of your terminal 
3. > - Redirector which takes output from one command and directs it elsewhere
4. >> - Appends the output rather than replacing (as done with >)

# Permissions: 
View using ls -lh 
Read, Write and Excute 

User V.S Group: 
Let's put this into a real-world context; the system user that runs a web server must have permissions to read and write files for an effective web application. However, companies such as web hosting companies will have to want to allow their customers to upload their own files for their website without being the webserver system user -- compromising the security of every other customer. 


# Use su -l <user> to be taken to that users home dir uppon entering password. 
  
  
# Common Directories: 
  /etc - contains vital system files 
  /var - contains frquently used files accessed or written by services or applications running the system
  /root - home for the root system user but data for the user is stored in /home/root. 
  /tmp - volatile data storage like ram. (Any user can write here, good for penetration testers) 
  
  
#VIM 
  :q<Enter> to exit 
  :help<Enter> or <F1> 
  :w<Enter> to write
  :wq<Enter> to write and exit 
  :q!<Enter> to force quit 

# Utilities 
  wget <link>
  --> wget -m to download recursively 
  SCP (Assuming you have credentials) - Uses SSH 
  --> upload: scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt
  --> download: scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt 
  Python -m http.server 1234 to host file/s.
  -->wget http://<ip>:<port>/<file> to download
 
# Processes:
  ps aux 
  top 
  kill 
  SIGTERM - Kill the process, but allow it to do some cleanup tasks beforehand
  SIGKILL - Kill the process - doesn't do any cleanup after the fact
  SIGSTOP - Stop/suspend a process
  
# Services to start on boot
  systemctl [option] [service]
  systemctl start apache2
  Options: start, stop, enable, disable 
  
# Background 
  Use & or CTRL+Z
  fg to bring back
  
# Automation: 
  Crontabs used: minute hour DOM MON DOW CMD 
  (Day of month, Month, Day of Week.)
  and would look something like this: 0 *12 * * * cp -R /home/cmnatic/Documents /var/backups/
  The aserisk * means to ignore that value. Therefore the above only exectues every 12 hours. 
  
  https://crontab-generator.org/ (Generator)

  crontab -e to edit using an editor such as nano 

# Package Managment 
  add-apt-respository 
  apt: used for package managment 
  dpkg can be used but apt will check for updates upon using apt-get update 
  apt-apt-repository --remove <ppa:PPA_Name/ppa>
  apt remove [software-name-here]
  
  
 
  
