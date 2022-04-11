# Tutorial for CSE 15L Students

## 1. Installing VS Code

**VS code** is an IDE that we can use to write and execute code on. It can be downloaded [here](https://code.visualstudio.com/download) for all operating systems

![VS-Code-img](/vscode-pic.png)

## 2. Remotely Connecting

Connecting to a remote computer is done using the ssh command. The course specific account for you that you are going to ssh into can be found [here](https://sdacs.ucsd.edu/~icc/index.php). After find ing your account use the following command on your terminal to ssh into that remote computer:

`ssh <youraccount>@ieng6.ucsd.edu`

This should prompt you to enter your password and upon correctly entering it you should have access to the remote device.

![sshpic](/labreport-2.png)

## 3. Trying Some Commands

Now that you have access to the remote device you can try running some commands on it. Some examples would be:

- `ls` - list out elements that are inside the directory your in
- `cd _dirname_` - enter a directory
- `mkdir _dirname_` - create a new directory
- `touch _filename_` - create a new file

## 4. Moving Files With scp

You can now move files from your local device to the remote device. To do this you can either create a new file or use an existing file and enter the following command to move that file from your local machine to the remote one.

`scp <filename> <youraccount>@ieng6.ucsd.edu:~/`

It will prompt you for a password and upon corrctly entering it, it will copy the file to the root diretcory of the virtual machine.

## 5. Creating an SSH key

Usually when we try to ssh into a remote device we will be prompted for a password. However, we can skip this step by setting up a SSH key. To do this, on your local machine run the command

`ssh-keygen`

It will ask you for a location and a passphrase. You can specify a location or press enter and the computer will automatically allocate it somewhere. Do not add a passphrase. This command will generate two files for you : a public key file, and a private key file. We now need to scp the public key file to the remote device's authorized keys file using the following command:

`scp <filelocationofpublickeyfile> <youraccount>@ieng6.ucsd.edu:~/.ssh/authorized_keys`

After completing these steps, you should be able to ssh into the remote device without it prompting you for a password.

## 6. Optimizing Remote Running

There a certain tricks you can use to make running comands remotely more efficient. Some examples are:

- you can use semi-colons to chain multiple commands together. `javac file1.java; java file1`
- you can use quotes to run a command on the virtual machine you are trying to ssh to. `ssh <youraccount>@ieng6.ucsd.edu "pwd"`
- you can use the up arrow to access all previous commands you have typed on the terminal.
