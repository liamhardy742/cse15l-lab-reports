# Week 1 Lab Report
Liam Hardy
CSE 15L


## How to Install Visual Studio Code

1. Click this [link](https://code.visualstudio.com/) to navigate to the VS code website and click the download link shown below 
![Image](VS Code First Screenshot.png)

3. Select the version that matches your machine's specificities, be sure to account for the 
![Image](VS Code Second Screenshot.png)

## How to log in to your course specific ieng6 account and remotely connect to a server

1. If you do not know your ieng6 account information, follow [these](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit) instructions. After that, open Visual Studio Code and open a terminal window as shown below.
![Image](VS Code Opening a Terminal.png)

2. In order to remotely connect to a server, we will use `ssh`. Type `ssh <insertUsername>@ieng6.ucsd.edu`, where `<insertUsername>` is replaced with your username for your ieng6 account. If this server is new to your machine, you will be told that the host's authenticity has not been verified. In order to verify, type `yes` and press enter. You will then be prompted for a password. Enter the password for your ieng6 account and now you are connected to the server. The process after completion is shown below
![Image](*complete process*)


## How to test some commands while logged on remotely
1. Once remotely connected you can test commands by executing them in the same terminal window you used to connect to the server. Now you may type whatever commands you wish, some of the most basic being
- cd
- cd ~
- ls
- ls lat
- mkdir
- pwd
- cat
