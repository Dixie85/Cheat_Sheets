# Commands

## Navigation
**"ls"**  --- LIST --- 
   - lists files in the current working directory (use * as wild card ex.ls *.txt).
   - ***ls -R ~*** starting from the root, will print every nested directory and the files inside them. 
        > note: the command can be written from everywhere.  

***"mkdir"*** --- MAKE DIRECTORY --- 
   - creates a  new directory/new folder (ex. mkdir {name}).

***"touch"*** --- CREATE FILE --- 
   - creates a new file (ex. touch {name}.{extension} / touch myText.txt).


***"cat"*** --- CONCATENATE ---
   - print the content of a file in the terminal (ex. cat {file}).
       - **"head"** - print the beginning of the content of a file in the terminal (ex. head {file}).
       - **"tail"** - print the end of the content of a file in the terminal (ex. tail {file}).

***"man"*** --- MANUAL ---
        - opens manual for a command (ex. man whoami).

***"cd"***  --- CHANGE DIRECTORY ---
   - (ex. cd {name of an existing directory}).

       - ***"."(dot)***   --- This directory ---

       - ***".."(two dots)***  --- moves to the parent directory --- (ex.cd ..)

***"~"(tilde)*** 
  - represents the ROOT directory (ex. cd ~ moves to the root directory).
  - when a path is given, the pat must start with ~  (ex. ~/folderName/folderName2/).


## Copying, moving and removing files
### ***"cp"***  --- COPY ---
   - if location is not specified the file will be copyed in the same directory, but a different name must be given. 
   - a path must be provided if a file is copied in a different directory (ex. cp myDoc.txt ~/folderName/folderName2/).

### ***"mv"***  --- MOVE ---
   - moving the file in the same directory with a different name will RENAME the file (ex. mv myDoc.txt myText.txt).
   - a path must be provided if a file is moved in a different directory.

### ***"rm"***  --- REMOVE ---
   - permanently deleteing the specified file
   - used with the * (the wild card) will delete all file in the current directory (only files) (ex. rm *) 
   - "rm" can delete specific group of files if name or extension is added after * (the wild card) (ex. rm *.txt)  

## Removing directories - and using flags 
***"rmdir"*** --- REMOVE DIRECTORY ---
   - permanently deleteing the directory
### Flags

###   ***"- r"*** - Recursive, i.e. include all subfolders, and files permanently
### ***"- f"*** - Force (don’t ask questions)
   > note: Flags follow the original command (ex. rm -r -f ~/folderName/folderName2/) (ex. rm -rf ~/folderName/).


## Usefule video materials

[How to Install Linux Terminal on Windows 10](https://www.youtube.com/watch?v=LLlfLpvQg04)

[Install Linux Terminal on Windows 11 and customization](https://www.youtube.com/watch?v=VT2L1SXFq9U)

[Terminals - differences and benefits](https://www.youtube.com/watch?v=NVMNLlH9L8A)

[Tips for using Windows Terminal in Windows 11](https://www.youtube.com/watch?v=FC-gLkYWXLw)