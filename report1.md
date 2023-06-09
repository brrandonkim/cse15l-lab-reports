# Hello Incoming CSE 15L Students!

This post will teach you how to log into a course-specific account on `ieng6`. 

---
**Step 1: Logging into your CSE 15L Account**

1. Click this link: [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php)
  * Then proceed to log in using the asked information
  * Your page should look like this: <img width="1494" alt="Screen Shot 2023-04-08 at 7 48 04 PM" src="https://user-images.githubusercontent.com/110199983/230751497-d18b09a8-06df-4c18-baa7-c1e3580a2bd9.png">
2. Then please click on your course-specific account name which starts with the 8 letter characters "*cs15sp23*" (The first 8 characters vary depending on the course and quarter taken.)
  * After doing so it should look like this: <img width="1491" alt="Screen Shot 2023-04-08 at 7 50 36 PM" src="https://user-images.githubusercontent.com/110199983/230751571-541bc19f-4314-468b-b483-04b98f90f6af.png">
3. Please click on the **Global Password Change Tool** and proceed to change/add your password to this course-specific account.
4. You should be set! Make sure to try logging in with your new username and password.
> The purpose of this is to connect to your account to the **remote** server.

---
**Step 2: Downloading and Setting Up Visual Studio Code**

1. Click this link to download *VSCode*: [VSCode](https://code.visualstudio.com/)
  * Please download the version based on your operating system.
  * Depending on what operating system and settings, open *VSCode* and it should look similar to this: <img width="1284" alt="Screen Shot 2023-04-09 at 2 49 37 AM" src="https://user-images.githubusercontent.com/110199983/230766072-189623b9-ee71-4d80-9611-2974669f1818.png">
  * Keep in mind, whenever you see a chunk of code in light gray, it is specifying that the code block is running on the remote server. And remember that the $ is not for you to type in! It’s just a convention for how we write commands. For example:
    `$ this is a command to the remote server`
2. **(Windows only)** You must install `git` if you are a Windows user. If you are using Mac you may skip to the next step. Click this link to download git: [Git for Windows](https://gitforwindows.org/)
3. Once installed, follow these upcoming steps to set your default terminal to use the newly-installed `git bash` in Visual Studio Code: 
  * Click this link to use git bash: [Git Bash Tutorial](https://stackoverflow.com/a/50527994)
  * Then, to use `ssh`, open a terminal in VScode. (Mac Users: Look at the top of the screen and click View → Terminal. Windows Users: Terminal → New Terminal menu option). It should look like this, but with the `xx` replaced by the letters in your course-specific account.
  `$ ssh cs15lsp23xx@ieng6.ucsd.edu`
  * Since this is the first time you’ve connected to this server, you will get a message like this: 
```
⤇ ssh cs15lsp23zz@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```
  * Type **yes** and press enter, then give your password (it will look like nothing is typing into terminal, but it still is typing the keys you enter)
  <img width="538" alt="Screen Shot 2023-04-09 at 9 53 17 PM" src="https://user-images.githubusercontent.com/110199983/230828651-d5bbaebd-a2b8-4215-9503-dc5d01aace1c.png">
  * The whole interaction should look something like this once you have successfully given your password and are logged in: <img width="613" alt="Screen Shot 2023-04-09 at 9 50 34 PM" src="https://user-images.githubusercontent.com/110199983/230828302-bbafe709-918a-4e68-b5dc-24ce7b2a1c46.png">

  * Now your terminal is connected to a computer in the CSE basement, and any commands you run will run on that computer! We call your computer the client and the computer in the basement the server based on how you are connected.

---
**Step 3: Let's Try to Run Some Commands**
1. Try running the commands `cd`, `ls`, `pwd`, `mkdir`, and `cp` a few times on your computer after ssh-ing (use the terminal in VScode) 
2. Here are some specific useful commands to try:

  * `cd ~` 
  * `cd`
<img width="494" alt="Screen Shot 2023-04-09 at 9 57 20 PM" src="https://user-images.githubusercontent.com/110199983/230829040-6c506b40-2b24-4c27-b2aa-d79579a4388d.png">
These two should allow you to move between desired directories.

---
  * `ls -lat`
<img width="461" alt="Screen Shot 2023-04-09 at 9 58 12 PM" src="https://user-images.githubusercontent.com/110199983/230829121-170e9fa8-6bc3-4091-971f-5438cf86ad99.png">
This command writes the standard output of the contents of each specified Directory or the name of each specified File, along with any other information you ask for with the flags.

---
  * `ls -a`
<img width="1151" alt="Screen Shot 2023-04-09 at 9 58 45 PM" src="https://user-images.githubusercontent.com/110199983/230829184-92bbf9d3-2f58-4097-a91a-afa2966ce4e0.png">
This shows the list contents of present working directory.

---
These next ones need specific files or names:

  * `ls <directory> where <directory> is /home/linux/ieng6/cs15lsp23/cs15lsp23abc`, where the abc is one of the other group members’ username
  * `cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/`
  * `cat /home/linux/ieng6/cs15lsp23/public/hello.txt`
  * Both cat and cp write the output file. With cat , the output file is opened by the shell, whereas with cp , the output file is opened by cp.
3. To log out of the remote server in your terminal (if needed), you can use:

  * Ctrl+D
  * Run the command `exit`
> You can also open more terminals in VSCode (there is a little + button at the top of the terminal window where you can create another).

---

## That's all! Congrats on your initiation to CSE 15L!
