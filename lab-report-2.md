# Lab Report 2

## Code Issue 1: Assuming User Always Provides A File

### **Test File**:
As this error occurs without the need for a test file there is no test file for this code issue

### **Commit Changes Screenshot**
![first-commit](/commit-1.png)

### **Symptom and Relationship**:

![first-symptom](/symptom-1.png)

The bug in this case was that the code always assumed the user would provide a file and hence even in the case where no file is provided the code still
tries to read a file. This causes an ArrayOutOfBounds Exception as the args array is actually empty and so in order to fix this we first check if there 
is any file provided by the user and only then execute the rest of the code.




