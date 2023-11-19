# Lab 4
## Step 4: Log into ieng6
![Image](lab42.png)

Keys pressed: I already had the command `ssh cs15lfa23oh@ieng6.ucsd.edu` in my clipboard, so I copy pasted it by right clicking on the terminal and then used `<enter>` to run the command.

## Step 5: Clone your fork of the repository from your Github account (using the SSH URL)

![Image](lab41.png)

Keys pressed: `<up><up><up><enter>`. The command was 3 up in the history, so I used the up arrow to access it.

## Step 6: Run the tests, demonstrating that they fail

![Image](lab43.png)

Keys pressed: `cd lab7`, then `bash test.sh`. First I switched into the lab7 folder, then used the provided `test.sh` file to compile and run the JUnit tests. 

## Step 7: Edit the code file ListExamples.java to fix the failing test (as a reminder, the error in the code is just that index1 is used instead of index2 in the final loop in merge)

![Image](lab44.png)

Keys pressed: `<4><3><enter><e><x><i><2>`. Since I now know which line the error in the code is, I type '43' and then press `<enter>` to jump to that line. If I didn't know where it was, I would use `/index1` to search for the error. I then used `<e>` to move the cursor onto the 2, `<x>` to delete the 2, `<i>` to enter insert mode, and `<2>` to alter the code.

## Step 8: Run the tests, demonstrating that they now succeed

![Image](lab45.png)

Keys pressed: `<esc><:wq><up><enter>`. I exited insert mode use `<esc>`, then saved and exited the file with `<:wq>`. Since `bash test.sh` was the previous command, I used the up arrow to access and run the tests again.

## Step 9: Commit and push the resulting change to your Github account

![Image](lab46.png)

Keys pressed: `git add ListExamples.java`, `git commit -m "Changes to ListExamples.java"`, `git push`. Updated the repository with above commands.
