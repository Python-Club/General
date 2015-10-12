##Accessing the HPCC at Michigan State

###Windows users
Open Mobaxterm.
On the top left, click the "Session" tab, and on the popup menu right under it, click "new session". 
Again on the very top left on this new window, click "SSH". 
Under "basic SSH settings", enter into the "remote host" window:

```
hpcc.msu.edu
```

Check the box for "specity username", and input your netID. Now click "ok" at the bottom of the screen. 
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
to show your current file path. 

