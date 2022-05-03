# Lab Report 2

## Code Issue 1: Code assumes user always provides a file

### **Test File**:

As this error occurs without the need for a test file there is no test file for this code issue

### **Commit Changes Screenshot**

![first-commit](/commit-1.png)

### **Symptom and Relationship**:

![first-symptom](/symptom-1.png)

The bug in this case was that the code always assumed the user would provide a file and hence even in the case where no file is provided the code still
tries to read a file. This causes an ArrayIndexOutOfBoundsException as the args array is actually empty and so in order to fix this we first check if there 
is any file provided by the user and only then execute the rest of the code.

## Code Issue 2: Infinite loop caused by code running even when there are no more links left

### **Test File**:

[test-file-1](/test-file.md)

### **Commit Changes Screenshot**

![second-commit](/commit-2.png)

### **Symptom and Relationship**:

![second-symptom](/symptom-2.png)

The issues in this case is that code for finding links continues to run even when there are no more links remaning in the file to find. This results in an
infinite loop causing an OutOfMemory error. In order to fix this we add an if statement that just checks whether there are any more links remaining in the
file, and if not, we exit the loop.

## Code Issue 3: Image links are included in the list of links 

### **Test File**

[test-file-2](/test-file2.md)

### **Commit Changes Screenshot**

![third-commit](/commit-3.png)

### **Symptom and Relationship**:

![third-symptom](/symptom-3.png)

In this case the code also reads image links, which differ from normal links by an ! mark at the beginning of the lin, and adds it to the list of links.
The leads to incorrect links being added to the list. In order to prevent this we check whether the beginning of the link is an ! point, and if so, we
skip that link








