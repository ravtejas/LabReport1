# Lab Report 3 (Week 6)

## 1. Streamlining ssh Configuration

- Editing the .ssh/config file

![ssh-config](/ssh-config.png)

This file shows the ssh-config file being edited to allow for easier ssh-ing int the ieng6 server. The alias chosen to replace the previous long command is
**ieng6**. It is now possible to ssh into the server by simply writing ssh ieng6 as shown below.

- Logging in with ssh using new alias

![ssh-alias](/ssh-with-alias.png)

Hence it is now possible to ssh into the server without having to type the long command previously required. This makes the process far less tedious.

- scp command using the new Alias

![scp-alias](/copyingfile-alias.png)

We can also scp files to the serveer by using the alias, as shown above. This also makes the process far easier and less tedious.

## 2. Setting up Github Access with ieng6



## 3. Copying Whole Directories

- Copying the whole markdown-parser directory using scp -r

![scp-r](/scp-r.png)

Entire directories can be copied using the scp -r command as shown above. The entire markdown-parser directory was copied to the remote ieng6 server using
a single command and it took about 3 seconds to complete.

- Running tests on the server 

![runningTests](/runningtest.png)

Now that the whole directory has been copied to the remote server, we can run test files on the remote server using the files in the directory. The above
image shows tests written in the MarkdownParseTest.java file being run on the remote server.

- Combining scp -r and ssh

![scp-r+ssh](/scp+ssh.png)

We can also combine the scp -r and ssh commands to first, copy the whole directory to the server, and then second, ssh into the server and run the tests
on the server all in one command. The image above shows the command used and the result of the directory being copied to the remote server and then the
tests being run. Overall it took about 5 seconds for the whole command to complete.



