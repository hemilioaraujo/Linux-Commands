# Linux Commands

    A Linux terminal commands list that's commonly used.

## Navigation

|Command|Description|
|------|------|
|```pwd```|Where am I?|
|```ls```|List files and directory.|
|```ls -l```|List files and directories in an extended form.|
|```ls -lh```|List files and directories in an extended form and shows the file's unit of measurement.|
|```ls -a```|List all files and directories including the hidden ones.|
|```ls -la```|List all files and directories including the hidden ones in an extended form.|
|```cd <directory>```| Change to destination directory|
|```cd <directory>/<sub-directory>```| Change to destination sub-directory.|
|```cd ..```|Go back to previous directory.|
|```cd ../../```|Go back to previous directory.|
|```cd /```|Go to root directory.|
|```cd ~```|Go to home directory.|
|```clear```|Clear the terminal screen.|
|```Ctrl + l```|Clear the terminal screen.|

## File and directory manipulation

|Command|Description|
|------|------|
|```mkdir <name>```|Create a directory.|
|```mkdir -p <a>/<ab>/<abc>```|Create nested directories.|
|```touch <file>```|Create file.|
|```mv <file> <destination>```|Move file to destination directory.|
|```mv <origin>/<file> .```|Move file from origin to current directory.|
|```mv <directory> <new name>```|Rename directory.|
|```mv <file> <new name>```|Rename file.|
|```cp <file> <new copy>```|Copy file to a new file.|
|```cp -r <directory> <new directory>```|Copy directory to a new directory.|
|```rm <file>```|Remove file.|
|```rm -r <directory>```|Remove directory.|
|```cat <file>```|Shows the file contents.|
|```less <file>```|Shows the file contents.|

## History

|Command|Description|
|------|------|
|```history```|Shows commands history.|
|```Ctrl + r```|Start the interactive search on history or find the next occurrence when the interactive search has already started.|
|```!n```|Execute the command number 'n'.|
|```!!```|Repeat the last command.|
|```!<string>```|Repeat the last command that starts with 'string'.|
|```dirs -p```|Shows the history of visited directories.|

## Permissions

|Command|Description|
|------|------|
|```chmod xxx <file or directory>```|chmod changes the permissions of user, group or everyone to read, write or run the file.|

## Varieties

|Command|Description|
|------|------|
|```diff -qr <diretory1> <diretory2>```|Shows the differences between the directories. Argument ```-q``` shows modified or nonexistent files. Argument ```-r``` shows the differences between files content.|
|```man <command>```|Page of Manual of commands.|
|```whoami```|Who am i? Shows you username.|