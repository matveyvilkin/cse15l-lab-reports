# Week 4 Lab Report

## Code Change 1
1. Screenhsot: ![Screenshot 1](bug_fix1.png)
2. You can see the file that was the failure-inducing input here: [test-file2.md](https://github.com/matveyvilkin/markdown-parser/blob/3bf95f8c828f6e0b47d5a126c1ecc32bef576f2d/test-file2.md)
3. Symptom: ![Screenshot Symptom 1](symptom1.png)
4. Explanation: The failure-inducing file contained a line after the last link. This made the while loop never end and links were added to the `toReturn` ArrayList until it run of out heap space, hence the error shown above. To fix this I added the following code block at the start of the while loop:
    ```java
    if (markdown.indexOf("[", currentIndex)==-1){
        break;
    }
    ```
    This ensured that when the last link was found, if there weren't nay more links after that (even if there was still text), the program wouldn't run infinitely.

## Code Change 2
1. Screenhsot: ![Screenshot 2]()
2. You can see the file that was the failure-inducing input here: [file 2]()
3. Symptom: ![Screenshot Symptom 2]()
4. Explanation: 
## Code Change 3
1. Screenhsot: ![Screenshot 3]()
2. You can see the file that was the failure-inducing input here: [file 3]()
3. Symptom: ![Screenshot Symptom 3]()
4. Explanation: 