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

<br></details>

    
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

 
 
 
 
 
 
 
 
 
 
 
 
 ---
 
 
 <br>
 
 </details>
