# Lab Report 4
## Vim (Week 7)
---
**STEP 4**
![image](Lab-Report-4-LogIn.png)
*Keys Pressed:* `ssh m1samson@ieng6.ucsd.edu`, `<enter>`
To log in, I just had to enter the `ssh` command, my UCSD log-in and the `ieng6` address. As we've learned previously, the `ssh` command allows for me to access a remote computer and use it to perform the following steps.

**STEP 5**
![image!](Lab-Report-4-GitClone.png)
*Keys Pressed:* `git clone git@github.com:MaritessSamson/lab7.git`, `<enter>`
I cloned the Github repository that I had forked to my personal Github. To do this, I used the `git clone` command and followed that with the password-protected SSH key. The `git clone` command works with HTTPS links and SSH links as we have learned.

**STEP 6**
![image!](Lab-Report-4-BashTest.png)
*Keys Pressed:* `bash test.sh`, `<enter>`
This step was to show that the tests fail, which they do. I used the `bash` command to run the `test.sh` shell file.

**STEP 7**
![image](https://github.com/MaritessSamson/cse15l-lab-reports/assets/165635190/a2458368-f551-4d88-a4c8-aa1b4060b54d)
*Keys Pressed:* `vim ListExamples.java`, `<enter>`,`44G`,`ce`, `insert2`, `<esc>` `:wq`
This allowed me to get into the Vim editor for the `ListExamples` java file. In the Vim editor, I then used the `G` command to skip to line 44. Because I only had to replace the word "insert1", I used the `ce` command and typed "insert2". This effectively fixed the code so I used the `<esc>` button to exit Insert mode and `:wq` to save my edits and exit the Vim editor.

**STEP 8**
![image!](Lab-Report-4-BashTestPass.png)
*Keys Pressed:* `<up> <up>`, `<enter>`
Because I had ran the bash test previously, I went used the `<up>` key to go up past the previous command and land on the `bash test.sh` command. Because of the previous edits I did, the tests passed. 

**STEP 9**
![image!](Lab-Report-4-GitCommit.png)
*Keys Pressed:* `git add .`, `<enter>`, `git commit -m "Changed ListExamplesTests to run properly"`, `<enter>`, `git push`, `<enter>`
I pushed the edits to my Github account by first using the `git add .` command. Putting the period cut down on time because I did not have type out any part of the name of the file, `ListExamples.java`. I took up time by having a long commit message, but it was thorough. Finally, I used the `git push` command.

---
*Fin*
