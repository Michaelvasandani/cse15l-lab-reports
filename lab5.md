# Lab Report 5
---
## Part 1
**Student**: Hi I'm having a problem with my `ListExamples.java` file, I ran the `bash test.sh` command, but I keep on failing tests. I think I might have some problems inside one of my while loops, but I'm not really sure. I attached an image of the terminal output when I ran the tests and the test I think I'm failing.
![Image](actualactualerror.png)
![Image](test.png)

**TA**: From looking at your terminal output, it looks like your test is timing out; this is usually the case when a loop is run an infinite amount of times. From the terminal output, it also looks like there's a problem in line 39 of your `ListExamples.java` file. A question you could ask yourself is, what's in line 39 of `ListExamples.java` and does this line potentially cause an infinite loop?

**Student**: When looking at line 39, I realized I was incrementing `index2` instead of `index1`, causing my while loop to run an infinite number of times. I fixed this by incrementing index1 instead, and now the problem seems to be fixed. I attached the terminal output when I ran the `test.sh` bash script as well as my fixed code.

![Image](actualFixederror.png)
![Image](fixedTest.png)

* **File and Director Structure**:
```
- lab7
    - lib
      - hamcrest-core-1.3.jar
      - junit-4.13.2.jar
    - .gitignore
    - ListExamples.java
    - ListExamplesTests.java
    - test.sh
```

* **Contents of file before fixing problem**:
![Image](contentsBefore.png)
![Image](testScreenshot.png)
![Image](bashscreen.png)
* **The full command line (or lines) you ran to trigger the bug**
bash test.sh 


* **A description of what to edit to fix the bug**
Changed line 39 of ListExamples.java from index2+= 1; to index1+= 1; fixing the infinite loop.

## part 2
I learned a lot of things from the second half of this class, but some things I think will be most useful would probably be debugging especially using the java debugger (jdb). When doing my work in java, like the PA's in CSE 12, sometimes I would get really confused when I'm debugging, I would go through all lengths, adding print statements to my code just to try to figure out where the mistake was happening. But when I learned about using jdb in class it sped up the debugging process for me by alot. I no longer needed to add print statements in my code just to figure out what was happening. Now, I can do it by just using the jdb command.

