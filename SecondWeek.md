<details><summary> Day 6️⃣ - Editing with "vi/vim" </summary>
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





<details><summary> Day 7 - Editing with "vim" </summary>
 <br>

    1) Connect and login remotely to your server
  
  
  <br>
</details>
