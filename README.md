# SRIM-on-Mac

SRIM is a group of computer programs popular in the ion implantation research and technology community and widely used in other branches of radiation material science, used to calculate interaction of ions and matter.

Currently, SRIM is only available for Windows machines, but it is possible to run it on mac using Wineskin Winery. Follow the instructions below to proceed.

## Install Wineskin Winery

- Install Wineskin with 
```bash
brew install --no-quarantine gcenx/wine/unofficial-wineskin
```
- in the Applications folder, launch the newly installed *Wineskin* ;
- the *“Create new blank wrapper”* option should be disabled, we’ll need to download the wrapper engine to get it to work;
- if the “installed engines” window is empty, go on the “+” and the download and install the default option ;
- then under Wrapper Version click on “Update” (or something like that) ;
- if everything went okay, now the *“Create new blank wrapper”* option should be available ;
- name the wrapper *SRIM* or whatever you like ;
- wrapper creation could take 1-2 mins ;
- when the process is completed, click on *“View wrapper in Finder”* ;
- you’ll see the wrapper you just created inside a *Wineskin* folder: you can move this app wherever you like (for example, in the default Applications folder) ;
- in case you missd  *“View wrapper in Finder”*, the wrapper is located at ```~/Applications/Wineskin```

## Download SRIM

You could download SRIM from the official website [here](http://www.srim.org), but it would require again a Windows Machine to launch it and extract the files. You can download the already unzipped foldere using the link below:

- [SRIM-2013-Std.zip](https://drive.google.com/file/d/1J2ukPoioqhS_U1I3yUz8RLLQTmOE3VtP/view?usp=sharing) (from my Google Drive)

Then make sure to extract the .zip file.

## Setup SRIM

To proceed to the setup, do the following:

- right click on the wrapper you created and go to *Show Package Content* ;

- click on the Wineskin app inside the folder that just opened ;

- go on *“Install software”*, then *“Move a Folder Inside”* , and choose the folder ```SRIM-2013-Std``` I provided you ;

- you’ll be prompted to choose an executable: choose the path ending with just SRIM.exe from the list, and then confirm ;

- now proceed on *Advanced* for some further setup;

- go to the tab *Tools*, and then, among *Wine Tools*, choose *Command Line (cmd)* ;

- a Windows terminal should pop up, now we need to execute the setup script provided by SRIM ;

- to do so, run the following lines inside the terminal one by one:
```batch
cd %ProgramFiles%/SRIM-2013-Std/SRIM-Setup
```
```batch
"_SRIM-Setup (Right-Click).bat"
```

  (you most probably will need to type each line by yourself)

- if prompted to install the *VB Runtime*, accept ;

- if prompted to press a key to continue the installation, go ahead and press any key ;

- when the script terminates, close the terminal and wait for it to shutdown (if you see *“a tool is running”* in the upper left corner of *Wineskin Advanced”*, please wait for it to disappear) ;

- then close *Wineskin Advanced* and the SRIM opened folder ;

- now you can just open the wrapper as you would normally do for any other app, and enjoy SRIM!


