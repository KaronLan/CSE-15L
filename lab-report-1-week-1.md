In this lab. we will learn about  how to log into a course specific account on ieng6.<br/>
There are six steps that we are going to do during the lab:
1. We will install VScode (if not already installed) where we can use the terminal.<br/>
  Here is a screenshot of what the VScode should look like when you open it up.<br/>
  Open a terminal.

2. We will remotely connect to a remote server.<br/>
  In the terminal, use `$ ssh cs15lfa22zz@ieng6.ucsd.edu` to connect to a remote server.<br/>
  (Remember to replace "zz" with the letters in your course-specific account.)<br/>
  A prompt will appear to ask if you want to `continue connecting (yes/no/[fingerpring])`,<br/>
  and be sure to type in yes.<br/>
  Then, put in the password when prompted. Congratulations, you successfully connects<br/>
  to a remote server.

3. We will try some command on the server to get an idea of what we can do with it.
  * `cd~`
  * `cd`
  * `ls -lat`
  * `ls -a`
  * `ls <directory>` where `<directory>` is `/home/linux/ieng6/cs15lfa22/cs15lfa22zz`
                                      (zz is the last two  the letters in your 
                                      groupmate's course-specific account)
  * `cp /home/linux/ieng6/cs15lfa22/public/hello.txt ~/`
  * `cat /home/linux/ieng6/cs15lfa22/public/hello.txt`

4. We will move files to the remote server using scp.
  First, create a file on your local computer.
  `class WhereAmI {  
   public static void main(String[] args) {  
    System.out.println(System.getProperty("os.name"));  
    System.out.println(System.getProperty("user.name"));  
    System.out.println(System.getProperty("user.home"));  
    System.out.println(System.getProperty("user.dir"));  
   }  
  }`<br/>
  Then, use `scp WhereAmI.java cs15lfa22zz@ieng6.ucsd.edu:~/` to move files to the remote server.<br/>
  Run the file in on the remote server. It should be there.<br/>


5. We will set an SSH key to log in without password.<br/>
  on client, use command `$ ssh-keygen` and you will get:<br/>
  `Generating public/private rsa key pair.<br/>
  Enter file in which to save the key (/Users/joe/.ssh/id_rsa): /Users/joe/.ssh/id_rsa<br/>
  Enter passphrase (empty for no passphrase): <br/>
  Enter same passphrase again: `<br/>
  on client, use command `$ ssh cs15lfa22zz@ieng6.ucsd.edu and then <Enter Password>`<br/>
  on server, use command `$ mkdir .ssh and then <logout>`<br/>
  back on client, use command `$ scp /Users/joe/.ssh/id_rsa.pub cs15lfa22@ieng6.ucsd.edu:~/.ssh/authorized_keys`


6. We will optimize remote running to ensure a better experience.<br/>
  Try these two lines of command<br/>
  * `$ ssh cs15lfa22@ieng6.ucsd.edu "ls"`<br/>
  * `$ cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI`<br/>
  * You can also use up-arrow to recall last command, or use !command number to recall previous commands.
