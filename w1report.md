# Logging Into a Coruse Specific Account in ieng6
---
## Step 1 - Preparing VScode
**Download VScode [here](https://code.visualstudio.com/) and run the application**
>You should see a screen that looks something like this:

![image](https://user-images.githubusercontent.com/122496316/211947322-6b4d52b0-59ba-45f0-ab53-8bae70b75190.png)

**For Windows users**
1. Download git [here](https://gitforwindows.org/)
2. In VScode press `Ctrl` + `~` to open a terminal
3. Press `Ctrl` + `Shift` + `P` to open the command palette
4. Type `Select Default Profile`
5. Select Git Bash
6. Click on the + in the terminal
>Your terminal should look something like this: 

![image](https://user-images.githubusercontent.com/122496316/211946116-17c4d8ea-7a3b-4e20-9dcd-50c1d9d03237.png)

**Once you are in the bash terminal go onto the next step**

## Step 2 - Connecting Remotely
**Before completing this step make sure you know your CSE15L account and password**

**If you don't know you can look it up and set your password [here](https://sdacs.ucsd.edu/~icc/index.php)**

* In the bash terminal insert in this command: `ssh cs15lwi23XXX@ieng6.ucsd.edu` (replace *XXX* with your unique 3 character code)
* Type `yes` if prompted
* Enter your password
> Note that as a security feature the terminal will **not** display your password as you are typing it in

> If your login was successful yo should see a message like this:

![image](https://user-images.githubusercontent.com/122496316/212457355-df49f232-fa66-4844-b417-c5bc3bee06ed.png)

**You're now connected to a computer in the CSE basement**

## Step 3 - Testing Commands

**Now that you're in test out some commands and look at the results**

As of now you should know 
* `cd` Which changes the current directory (Won't give an output if it doesn't have an error)
* `ls` Which lists the current files and subdirectories of the current directory (It should output the files in your directory)
* `pwd` Which prints out any applicable text within your directory (It should output out any text files in your directory)
* `mkdir` Which makes a new directory with the given name (Will give an error if you don't specify the directory)
* `cp` Which copies the files in the directory to another location (Will give an error if you don't specify both directories)

Try using these in various ways on to try to figure out how they work on the remote computer.

Now try these same commands on your own computer, do you see any differences?

> For some fun try `ls ..` then you can see all the other student accounts for CSE15L!

![image](https://user-images.githubusercontent.com/122496316/212457777-a786dc60-dafa-4774-8471-f701a590b75f.png)

Once you are done you can run `exit` to log out of the remote computer

**And that's how to remotely connect to a computer in the CSE basement!**
