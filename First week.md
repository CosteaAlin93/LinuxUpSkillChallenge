<details><summary> Day 1 - Get to know your server </summary>
 <br>

    1) Connect and login remotely to your server
- Log into the AWS account you created in the Day0 of the challenge and launch your EC2 instance.

![image](https://user-images.githubusercontent.com/86648102/139727838-26378eac-0cc3-46fa-a65b-9ec8e86536ae.png)

- Open your virtual machine. Make sure to have the key copied into the **.ssh** folder and have it's permissions set to 440.

![image](https://user-images.githubusercontent.com/86648102/139728310-7317283d-77f6-45c9-a6d1-2bf0014912d8.png)

- Connect to the instance using the provided IP from AWS console.

![image](https://user-images.githubusercontent.com/86648102/139728494-e64ccdf7-c9d3-4092-942f-ef562712a252.png)

---
    2) Run a few simple simple commands to check the status of your server
Try these simple commands:
`ls`
`uptime`
`free`
`df -h`
`uname -a`

![image](https://user-images.githubusercontent.com/86648102/139728753-038bc87a-7824-49d6-b59b-a41ee2ac0ff9.png)

 ---
    3) Change your password
    
Use `sudo passwd ubuntu` command, then type the password you would like. Please make it strong!!!

---

That's all for today. Easy but fundamental.

---

<br>
</details>

    
<details><summary> Day 2 - Basic navigation </summary>
 <br>
 
    1) Login to your server using ssh
 
 ![image](https://user-images.githubusercontent.com/86648102/139802849-392214b2-c63c-476d-b66a-3e3adaf88aed.png)

    Use `pwd` and `cd` commands. Get familiar with them. Learn to use both, absolute and relative paths to change directories.
 
![image](https://user-images.githubusercontent.com/86648102/139803730-a9f6239e-18a2-4d1f-b178-ce8e24532203.png)

 ---
     2) Use the `printenv` command to show info about the current environment. Those can also be shown separately, by using `echo $HOME` , `echo $PWD` , `echo $OLDPWD` , `echo $USER` , or just `echo $ <any variable you see in the printenv output>` 
 
 ![image](https://user-images.githubusercontent.com/86648102/139804269-ac30f832-a525-4be6-892e-98b69920e866.png)

 ---
     3) Get used with `ls` command. `ls -l ; ls -lh ; ls -ltr ; ls -altr` . You'll use this command and switches daily.
 
 ![image](https://user-images.githubusercontent.com/86648102/139922296-b519c19e-c4f9-48c3-8c46-ad430cfbe8c8.png)

 ---
    4) Prompt customization
 `echo $PS1` will display current prompt.
 
 ![image](https://user-images.githubusercontent.com/86648102/139924383-e851d51b-10be-4f37-a66d-18a426722a87.png)

 
 This article here, will help you customize your prompt in more detail : 
 
 https://phoenixnap.com/kb/change-bash-prompt-linux
 
 For instance, let's change the prompt to give a bit more detail.
 
 `export PS1="\u\@\h \w \s \d \W \t"`
 
To exit that prompt, the command `bash` will open a new shell with your default environment.
 
 ![image](https://user-images.githubusercontent.com/86648102/139925150-15cc8142-5d31-415d-9a4e-38791447547f.png)

 ---
     5) Create files and directories.
 
 `mkdir` - will make a new directory in your current folder by default.
 
 `touch a` - will create a blank file named 'a' in your current folder. 
 
 ![image](https://user-images.githubusercontent.com/86648102/139925551-5ccbd957-a009-406b-b065-35a2b727d362.png)

 `mv` to move a file to another directory or rename a file

 ![image](https://user-images.githubusercontent.com/86648102/139925919-73b54b4d-23f5-4b87-8d6d-593982b3715c.png)

 `cp` will copy a file.
 
 ![image](https://user-images.githubusercontent.com/86648102/139926682-1fbaef20-73b5-4eef-98ba-4fd429fb3c62.png)

 `rm` will remove a file or multiple files
 
 ![image](https://user-images.githubusercontent.com/86648102/139926810-a2dc4bb5-992b-4eb5-be35-94aadd480028.png)

 `rmdir` will delete an empty directory
 
 ![image](https://user-images.githubusercontent.com/86648102/139926979-4be607af-fa91-435a-b979-b21fd65ab6ba.png)

 ---
     6) RTFM. I'll let you guess what this means.
 
 `man` is a command that displays the manual of the command given as argument.
 `man ls` will display everthing there is to know about `ls` command.
 
 ![image](https://user-images.githubusercontent.com/86648102/139927460-60069b1b-89cf-4d55-be09-9f720d0af49b.png)

 `apropos` is kind of the same, except that is shows every command or command explanations containing what we give as argument.
 
 ![image](https://user-images.githubusercontent.com/86648102/139927910-8f18f93e-d9a4-494d-bc12-3330bc0a03a6.png)

 `tldr` is a shorter version of man, containing a simplified version
 
 ![image](https://user-images.githubusercontent.com/86648102/139928305-b25ea31c-9d9f-4957-9faa-9a85b607e92f.png)

 
 ---
 
 
 
<br>
</details>
 
 
<details><summary> Day 3 - Power trip! </summary>
<br>
 
    1) The `root` user is the boss of your system.Period. 
 
     All the other users should have the minimum ammount of permission; just the necessary stuff for their actions to be possible. However, if your user is properly configured/allowed, you can run commands as the `root` user from your current one. For that, you need to use the `sudo` command.
 
 ![image](https://user-images.githubusercontent.com/86648102/140276137-d8c21f0a-780b-4159-ad7e-981bbe8f92fb.png)

 
 ![image](https://user-images.githubusercontent.com/86648102/140275620-c51b4f8c-171a-4a21-9bb0-199319de366d.png)

    2) `uptime` command can be used to check for how long is the system running and how many users are connected.
 
 ![image](https://user-images.githubusercontent.com/86648102/140275929-3f8cb4fa-6871-4b8f-9cbe-3c2fd9e286f7.png)

    3) Log checking. For instance, check authentication logs. Many other usefull files are in the `/var/log/` directory.
 
 ![image](https://user-images.githubusercontent.com/86648102/140277142-1b1f180c-1784-4341-a596-2a6114445712.png)

You can also, filter the results using `grep` to show only sudo entries.
 
 ![image](https://user-images.githubusercontent.com/86648102/140277587-745a1be9-91e6-4874-a207-0258f981e990.png)

    4) Hostname changing. 
     `hostnamectl`
 
![image](https://user-images.githubusercontent.com/86648102/140808987-99f8af28-3f16-413f-946f-12f2dd9d6b4e.png)

    `sudo hostnamectl set-hostname upskillchallenge`
 
 ![image](https://user-images.githubusercontent.com/86648102/140809319-48975163-c331-413a-9e22-7e89f86a98a7.png)

     5) Change the system time and date
 
     `timedatectl`
 
 ![image](https://user-images.githubusercontent.com/86648102/140809505-5256830b-6f0a-443f-8b01-0e72a62776ff.png)

 ![image](https://user-images.githubusercontent.com/86648102/140809561-7f305d17-ca90-4b4c-915f-720cbabff9f8.png)

    `sudo timedatectl set-timezone Europe/Bucharest`
 > Used this to set the time to my current timezone.
 
 ![image](https://user-images.githubusercontent.com/86648102/140809869-2818f971-08b1-4f66-a64a-025bbb5bf007.png)
  
<br>  
</details> 
 
 
<details><summary> Day 4 - Installing software, exploring the file structure </summary>
<br>
 
    1) Install new applications.
 
> For Debian: apt, dpkg, aptitude, synaptic  (.deb)
> For Redhat: yum, dnf, (.rpm)
 
    Example: we want to install midnight commander, but don't know the exact name of the package.
 
    `apt search midnight`
 
 ![image](https://user-images.githubusercontent.com/86648102/140811849-28a2c2ec-dd90-4723-a604-d46455b42b14.png)

    `sudo apt install mc`
 
 ![image](https://user-images.githubusercontent.com/86648102/140811943-24665b1c-83e7-4bff-8c32-07e3c820cbca.png)

 
 
 
 <br>  
</details> 
 
 
 
