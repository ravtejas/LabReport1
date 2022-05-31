# Lab Report 4 (Week 8)

## 1. Links to Repositories

[Link to my repository](https://github.com/ravtejas/markdown-parser)

[Link to the Repository I reviewed](https://github.com/mikayladalton2/markdown-parser)

## Expected Outputs for Snippets

- Snippet 1:

[“`google.com”, “google.com”, “ucsd.edu”]

- Snippet 2

[“a.com”, “a.com(())”, “example.com”]

- Snippet 3

[“https://www.twitter.com”, “https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule”, “https://cse.ucsd.edu/”]

## Code for Markdown Parse Tests

- Test for Snippet 1

![Snippet-1-Test](/Snippet1Test.png)

- Test for Snippet 2

![Snippet-2-Test](/Snippet2Test.png)


- Test for Snippet 3

![Snippet-3-Test](/Snippet3Test.png)

## Results of Test run on both repositories

- Tests Run on my Repository Results

![myTests](/Mytests.png)

Result: All tests failed.

- Tests Run on the Repository I Reviewed

![myTests](/otherTests.png)

Result: All tests failed.

## Answering Questions Regarding the Code

- Question 1: Do you think there is a small (<10 lines) code change that will make
  your program work for snippet 1 and all related cases that use inline
  code with backticks? If yes, describe the code change. If not, describe
  why it would be a more involved change.
  
Yes, I think there is an easy fix for this issue. I can use to variables to track the opening and closing index of backticks and if the opening '[' or closing ']' index lies between those values, we can know to ignore that link and move to the next one.

- Question 2: Do you think there is a small (<10 lines) code change that will make
your program work for snippet 2 and all related cases that nest
parentheses, brackets, and escaped brackets? If yes, describe the
code change. If not, describe why it would be a more involved change.

Yes, I think there is an easy fix to this issue. After finding the index of the opening '(' or '[' we can keep a counter of all the open brackets and all the closed brackets of the same type and run a while loop finding all instances of the bracket until the number of closed brackets is equal to the number of open brackets. In this way we can ensure we get the correct closing bracket for the corresponding open bracket and do not prematurely get an incorrect version of the link by taking the wrong closing bracket index.

- Question 3: Do you think there is a small (<10 lines) code change that will make
your program work for snippet 3 and all related cases that have
newlines in brackets and parentheses? If yes, describe the code
change. If not, describe why it would be a more involved change.

In this case, I do not think there is an easy way to solve this issue. It would require me to track new lines within the parantheses which is somthing im not too sure how to tackle. I would perpahs have to check if the closing bracket is on a new line and if so the link should be ignored, but that doesnt account for the edge case where the link might span over 2 lines. As a result, this issue becomes lsightly more complicated to solve.

  
  



