    Start VM:

1. Clone the repository: https://git.epam.com/Kuzma_Rezchenko/aqa-cdp-lab
2. In CLI execute vagrant up from folder with cloned repository

Jenkins will be available right after VM is created by url: 127.0.0.1:8080
if port 8080 on your host already used, vagrant should choose free port and output it to CLI

VM credentials:
username: vagrant
password: vagrant


    Actions before run Selenoid pipeline:

1. In Jenkins Pipeline configuration specify the repository: https://github.com/serhiyovich/ShramkoSelenoid.git
 - Branch - master
 - Script path - Jenkinsfile

Execute the following commands in shell on VM:
   sudo docker pull selenoid/chrome:65.0
   sudo docker pull selenoid/firefox:58.0
   sudo docker pull aerokube/selenoid

   sudo visudo

sudoers file wii be opened, add to the end of the file:

jenkins ALL = (ALL) NOPASSWD: ALL





