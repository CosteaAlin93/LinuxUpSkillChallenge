<details><summary> Day 6 - Editing with "vi/vim" </summary>
 <br>

    1) Editing documents with `vi`. 
 
  ![image](https://user-images.githubusercontent.com/86648102/143769852-95d47134-a989-4b26-aa02-7d5348e2ca81.png)
  
  vi fileName : to open a file
  :w fileName : to save it as another file
  
  **Copying (Yanking)**

To copy text, place the cursor in the desired location and press the y key followed by the movement command. Below are some helpful yanking commands:

    yy - Yank (copy) the current line, including the newline character.
    3yy - Yank (copy) three lines, starting from the line where the cursor is positioned.
    y$ - Yank (copy) everything from the cursor to the end of the line.
    y^ - Yank (copy) everything from the cursor to the start of the line.
    yw - Yank (copy) to the start of the next word.
    yiw – Yank (copy) the current word.
    y% - Yank (copy) to the matching character. By default supported pairs are (), {}, and []. Useful to copy text between matching brackets.

  **Cutting (Deleting)**

In normal mode, d is the key for cutting (deleting) text. Move the cursor to the desired position and press the d key, followed by the movement command. Here are some helpful deleting commands:

    dd - Delete (cut) the current line, including the newline character.
    3dd - Delete (cut) three lines, starting from the line where the cursor is positioned,
    d$ - Delete (cut) everything from the cursor to the end of the line.

The movement commands that apply for yanking are also valid for deleting. For example dw, deletes to the start of the next word, and d^ deletes everything from the cursor to the start of the line.
  
  **Pasting (Putting)**

To put the yanked or deleted text, move the cursor to the desired location and press `p` to put (paste) the text after the cursor or `P` to put (paste) before the cursor.

  **Undo changes**
  Use `u` to revert changes.
  
  **Find**
  Use `/` to find items then `n` to go to the next found item.
  
  2) Use `vimtutor` to find more info about vim and it's powers.
  
  ![image](https://user-images.githubusercontent.com/86648102/143771778-3856ca2e-a886-4891-9dda-5c09183d2061.png)

  
</details>





<details><summary> Day 7 - Install Apache (also known as **httpd** </summary>
 <br>

    1) `sudo apt update` and  `sudo apt upgrade` 
    
>>to update the system
 
    2) `sudo apt install apache2`
  
 ![image](https://user-images.githubusercontent.com/86648102/143772031-e91139d5-5467-40e9-a150-cfae05193dee.png)

  Now, by putting out `Public` IPv4 address into a browser, we'll get this message:
 
 ![image](https://user-images.githubusercontent.com/86648102/143772163-a9c49935-ed3a-438e-b830-269666d19bc8.png)

   3) Check the status of the apache service with `systemctl status apache2.service`
 
   ![image](https://user-images.githubusercontent.com/86648102/143772222-7d09a83a-184c-4e41-b735-c112eae563af.png)
 
   Also, `systemctl` has a lot of other usages, including **restart** , **reboot** , **stop** and many others.
 
 ![image](https://user-images.githubusercontent.com/86648102/143772319-99b6ab55-74d8-41e1-bb0c-4ec382a5d078.png)

 
   4) Apache configuration is found in `/etc/apache2/apache2.conf`
 
 ![image](https://user-images.githubusercontent.com/86648102/143772659-0b12bd74-ea35-4843-a2d4-38bb91e5b0a2.png)
 
   Also, the place where the default page files are found is into `/var/www/html/index.html`
 
 ![image](https://user-images.githubusercontent.com/86648102/143772753-c82f9c04-ae5a-4ae9-9bb6-c1540eefc232.png)

   By modifying this file, you change the look of your default page.
 
 ![image](https://user-images.githubusercontent.com/86648102/143774040-e2c46ebd-9795-4383-9ace-f29008d835f7.png)

   5) Apache logs.
     
   You can see who's been accessing your page in the `/var/log/apache2/access.log` file. 
 ![image](https://user-images.githubusercontent.com/86648102/143774117-994864fe-9fd9-4850-8fe1-04f47c9a70eb.png)

 
  <br>
</details>

<details><summary> Day 8 - The infamous "grep" and other text processors </summary>
 <br>

   1) `cat /var/log/apache2/access.log` 
   2) `less /var/log/apache2/access.log`
   3) `sudo less /var/log/auth.log`
    > View recent logins and sudo usage by viewing /var/log/auth.log with less

   4) `head /var/log/apache2/access.log`
   5) `tail /var/log/apache2/access.log`
   6) `sudo cat /var/log/auth.log | grep "authenticating"`

      `grep "authenticating" /var/log/auth.log | grep "root"`
   7) cut : command to select out most interesting portions of each line by specifying "-d" (delimiter) and "-f" (field)
      `grep "authenticating" /var/log/auth.log| grep "root"| cut -f 10- -d" "`

  <br>
</details>

<details><summary> Day 9 - Diving into networking </summary>
 <br>
  
    1) `netstat` : Print network connections, routing tables, interface statis‐tics, masquerade connections, and multicast memberships
`netstat -l`
`netstat -lp`
`netstat -r` 
`netstat -i` 
 
    2) `ss` : Socket Status
 `ss -ltp` 
 ![image](https://user-images.githubusercontent.com/86648102/155973208-6e42d5a9-c4a4-4d94-8dba-f562baacf581.png)

    3) `namp` : Network Mapper
 `nmap localhost`
 ![image](https://user-images.githubusercontent.com/86648102/155973528-915be1cf-f5e1-4ab5-aaae-9e7c57f96a3a.png)

    4) Firewalls : `ufw`
 `sudo ufw status`
 `sudo ufw deny http`
 `sudo ufw enable`
 `sudo ufw status`
 `sudo ufw allow http`
 ![image](https://user-images.githubusercontent.com/86648102/155975053-261ef379-5d6e-4ac1-9d0b-093f90975c38.png)

 
 
 
 
   <br>
</details>


<details><summary> Day 10 - Getting the computer to do your work for you </summary>
 <br>

    1) Crontab : edit it with `sudo vi /etc/crontab` and add your entries at the bottom of the file.
 ![image](https://user-images.githubusercontent.com/86648102/155978881-6df90ffa-1220-4da5-a11f-4837d01a2f14.png)

 
 
 
 
    <br>
</details>
