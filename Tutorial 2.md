# Python Course week 1. 


## Contents:
  - [Command line](#command-line)
  - [py Files](#py-files)
  - [Running py Files](#running-py-files)

 
## Command line
There are multiple ways to access files on a computer with the most user friendly way being the user interface which is provided to the user by clicking the following, ![Alt text](MS_document_icon.PNG?raw=true "Optional Title").

An alternative method to accessing files on your computer is available from *Command line/prompt*. On Windows this is most commonly referred to as *Command Prompt* though other systems use names interchangably i.e. *Terminal* on Mac. All of these offer a prompt methodology to navigate and use the computer, purely using the keyboard.

On Windows, to open *Command Prompt*:
  1. 'Click' on the start Window and type 'command propmpt' and press 'Enter'
  2. A window which looks like the following should open
  ![Alt text](Command_prompt.PNG?raw=true "Optional Title")
 
Congratulations, you have just opened your first *Command Prompt* session. But where to from here? Well, lets explore this tool a bit further. In the box, type the following:

```bash
cd Documents
```
followed by: 
```bash
dir
```
Now, without closing the *Command Prompt* window, open your Documents folder by clicking through the document icon. What do you notice about the contents in the *Command Prompt* methods vs the user interface method? 

The below two commands you used should be all you need initially for working with Python scripts.
```powershell
cd Documents
```
*Changes directory* from the current folder to a low-level folder, in the above case the 'Documents' folder. 
To move up a directory use: 

```bash
cd .. 
```

The other useful command is 
 ```bash
 dir
 ```
The above lists all the files in the current folder you are located in. 

Now you know the basics of using *Command Prompt* let's move to running creating a running a Python script using *Command Prompt*. 
You can now close *Command Prompt*.

## py Files
A .py file is a Python file or script that can run using a Python interpretter. I will asumme you know what Python is, however, if you woujld like to know more you can check out the website [here](https://www.python.org/doc/essays/blurb/). There is nothing special about these files except that they end in the extension '.py' and they contain Python code. A Python file can be called anything you like, a valid name might be 'Jackleekpoij.py'. Now we know a little about this special type of files how can we create one? 

A .py file be created by using any *text editor*, we will use 'Notepad'. 
'Click' the start menu and type in 'Notepad' and press 'Enter'. 
This should open a blank page for you to write. 
Within this file type: 
  print "Hello, World"
Now save the file by clicking *File*>*Save as*. 
When prompted for a name of the file type the following saving this file in your **Documents** folder: 
  'HelloWorld.py'
Now 'click' Save.

Congratulations, you have now created your first Python script. Did you notice the ending of the file, how it had to end in '.py'? 
But how can this file be run?

## Running py Files
With a Python script created it's now time to run some code. Let's start by opening *Command Prompt*. Navigate to the Documents folder to locate the newly created Python script by using the change directory commands, 'cd'. 

```bash
cd Documents
```
To check the file exists, use the 'directory' command to list all the files within the Documents folder. Your file called 'HelloWorld.py' should appear. 

Now to run this Python file, simply type in: 

```bash
python HelloWorld.py
```

What happend? Look at the above code you wrote into the Python scipt and change it such that the Python script now prints out your name. 

**Congratulations, you have now run your first Python script.**




