# Lab Report 5
# Putting it All Together
---
**Part 1**
1. Student: "I was trying to finish the autograder from Week 6's lab. I was using the link that intentionally fails on compilation, but it's not failing here! I think something's wrong with my logic probably, I don't remember what I'm supposed to do for not equals"
![image](https://github.com/MaritessSamson/cse15l-lab-reports/assets/165635190/f883b7ce-d75d-4a97-9c7a-6b0f61f37941) 
2. TA mimic: "Hi. Your logic looks good. What is the exit code from? Make sure it is from the program compiling."
3. In the end, the bug was line 41. Because the student had ran an `echo` command prior to the `if` block. The `echo` command had successfully ran which changed the exit code to be 0, instead of the exit code being from the file compilation.
   Fixed code: ![image](https://github.com/MaritessSamson/cse15l-lab-reports/assets/165635190/39c49d60-2704-4baa-abcc-e016d02b6f98)

4. Additional information:

* The `list-examples-grader` file is used. We are editting the bash script, `grade.sh`.
* The `grade.sh` file clones a student-submitted Github repo, checks for a `ListExamples` java file, and compiles the code. After compiling the code, it will run it with the test cases and return feedback based on the test case results. 
* The command line ran to get the bug was `bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-compile-error.git`
* The `echo` command has to be deleted from the `grade.sh` file on line 41. This fixes the bug since the exit code will continue to depend on the file compilation.

**Part 2**
Learning Vim was probably the coolest thing we learned in the second half of the quarter. I just didn't expect to be able to do so much from the terminal, much less edit files. I think it's very convenient, especially the shortcuts like the one to skip lines in files that are longer and more tedious to scroll through.
