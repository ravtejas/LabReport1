## Lab Report 5 Week 10

# How I found tests with different result

I did a a manual check by comparing the output of the test with the implementation provided along with my implemtation of markdown parse. In hindsight, this
was a rahter tedious process and I would have perhaps tried to use a loop to compare each test files output to my output and then gotten the file number
of the test cases that differed.

# Link to Test files used

I used test files 580 and 22. The links are below.

[File 580](/580.md)

[File 22](/22.md)

# Test 1

This test uses test file 580.

- Output for both implementations of Markdown Parse (MarkdownParse2 is my implementation)

![file580](/file580.png)

- Expected Output of file using markdown preview on VsCode

![file580run](/file580run.png)

In this My implemntation of markdown parse was correct and the provided one was incorrect. File 580 contains a single image link and the provided
implementation still considers image links and links and hence adds it to the list of links where as mine does not.

- How to fix the issue

The change would. be a simple check to see if the there is a ! immeadiately behind the '[' index. The code could be added to  part of the program shown below after the index of the [ has been found.

![change1](/change1.png)




