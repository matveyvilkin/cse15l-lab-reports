# Week 8 Lab Report

[The Common Mark demo site](https://spec.commonmark.org/dingus/) site will be used to determine the outputs of each respective snippet.

You can access my repository [here](https://github.com/matveyvilkin/markdown-parser).

You can access the repository reviewed in week 7 [here](https://github.com/hsflores7/markdown-parser).

## Snippet 1

1. The output of the program when run on this snippet should be: 
    ```
        [`google.com, google.com, ucsd.edu]
    ```
2. Below is the code for the test of snippet 1:
    ![Test 1](test1.png)

3. The output of my implementation produced the following:

    ![My Test 1 Output](my_output1.png)

4. The output of the repo worked on in week 7 produced the follwoing:

    ![Other Test 1 Output](other_output1.png)

## Snippet 2

1. The output of the program when run on this snippet should be: 
    ```
        [a.com, a.com(()), example.com]
    ```
2. Below is the code for the test of snippet 1:
    ![Test 2](test2.png)

3. The output of my implementation produced the following:

    ![My Test 2 Output](my_output2.png)

4. The output of the repo worked on in week 7 produced the follwoing:

    ![Other Test 2 Output](other_output2.png)

## Snippet 3

1. The output of the program when run on this snippet should be: 
    ```
        [https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]
    ```
2. Below is the code for the test of snippet 1:
    ![Test 3](test3.png)

3. The output of my implementation produced the following:

    ![My Test 3 Output](my_output3.png)

4. The output of the repo worked on in week 7 produced the follwoing:

    ![Other Test 3 Output](other_output3.png)

## Questions

1. Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

    Yes. When two "`" are followed by each other the program should not consider the text to be a link. This can be fixed by adding another condition to the original if-statement at the start of the while loop which would check for whether there a 2 backticks.

2. Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

    Yes. If there are `\` within `[]` preceeding the link, they should be ignored. Similarly, `()` between the link `()` should be ignored. This can be done by updating `closeParen` until no more are found.

3. Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.

    There is not a change under 10 lines which would fix the issues in the code producing the incorrect output. There are multiple issues present here, "twitter.com" should not be appearing as a link, as well as the links appearing on multiple lines.