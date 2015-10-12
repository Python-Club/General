##Accessing the HPCC at Michigan State
Loosely based on [this](https://github.com/edamame-course/2015-tutorials/blob/master/final/2015-06-22-introduction_to_the_shell.md) tutorial from EDAMAME 2015. 

###Windows users
Open Mobaxterm.
On the top left, click the "Session" tab, and on the popup menu right under it, click "new session". 
Again on the very top left on this new window, click "SSH". 
Under "basic SSH settings", enter into the "remote host" window:

```
hpcc.msu.edu
```

Check the box for "specify username", and input your netID. Now click "ok" at the bottom of the screen. 
After a few seconds, it will prompt you for your password. Enter the password and hit the enter key. *NOTE: nothing will show up on the screen as you type. That's ok. Just type your password as normal.


###Mac users
Open a session of Terminal.
Input the command

```
ssh [your netID]@hpcc.msu.edu
```

Enter your password when prompted.

##Congratulations! You've accessed the HPCC!

###What now?
Now that you are on the HPCC, you'll be using command line to navigate folders (called directories) and files.
When you first log onto the HPCC, you are in your "home" directory. 
Let's try making a new directory within our home directory.

```
mkdir HPCC_tutorial
```

Now we have our home directory and a new HPCC_tutorial directory within it. To make sure the command did what we wanted it to, use this command to list the contents of the directory that we're in, which right now is home:
```
ls
```
This should return only "HPCC_tutorial" if this is your first time accessing the HPCC. If you've used the account previously there may be other directories here.
Let's navigate into the new directory.
```
cd HPCC_tutorial
ls
```
We've now navigated into the HPCC_tutorial directory and listed the contents, which right now is nothing. 
To go back up one level of directories, use
```
cd ..
```
Or, since we want to get back to the home directory, we can use
```
cd
```
which will always take you back to your home directory.
If at any time you've gotten lost down a rabbit hole of directories, you can use the "print working directory" command:

```
pwd
```
to show your current file path. As an example, if you do this in your HPCC_tutorial directory, it will show
```
/mnt/home/[your netID]/HPCC_tutorial
```
##Accessing and transferring files with the shared research space 

Now that we can navigate through directories, let's access our shared research space. 
```
cd /mnt/research/Helab
```
If we list the contents of the directory, we will see four other directories: Data_Management_Protocols, MassSpec, Phenometrics, and Sequencing.
Let's navigate into the Data_Management_Protocols directory and see what's there.
```
cd Data_Management_Protocols
ls
```
Let's go to the Sequencing_protocols directory.
```
cd Sequencing_protocols
```
Let's say that we have some sequencing data and want to transfer the sequencing contextual data file to our computer in order to fill it out. 

###For Windows users
Go to the top left corner of Mobaxterm again and click "Sessions->new session".
This time, click "SFTP" which stands for "secure file transfer protocol".
Enter 
```
hpcc@msu.edu
```
for "remote host" and your netID for the username. Click "ok".
You may or may not be prompted to enter your password. This will take you to your home directory. The file path, in this case "/mnt/home/[your netID]" will be displayed in a bar on the right side of the screen. In order to navigate to the directory we want to be in, we can either enter the file path or click on the folders. 
Once you find the correct file, you can simply drag and drop from the HPCC screen (on the right) to your computer (on the left). 
You're done!

###Mac users
John will help you with FileZilla. Instructions will be updated at a later time. 

