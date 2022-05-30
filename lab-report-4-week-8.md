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
  
Yes, I think there is an easy fix for this issue. I can use to variables to track the opening and closing index of backticks and if the link indexes lie between the opening and closing indexes of the backticks, then we know to ignore that link.
  



