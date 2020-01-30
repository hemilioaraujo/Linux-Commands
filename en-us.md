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
|```cp -r <directory> <new directory>```|Copy directory to a new directory on a recursive way.|
|```rm <file>```|Remove file.|
|```rm -r <directory>```|Remove directory on a recursive way.|
|```cat <file>```|Shows the file contents.|
|```more <file>```|Shows the file contents. Load all file on memory at one go.|
|```less <file>```|Shows the file contents. Load the file using streams, this means that the command load just the necessary part of file.(Can use vim's commands)|
|```chown <user> <file>```|Changes the user that's the file owner.|
|```chown :<grupo> <file>```|Changes the group of file owners. This command can be used together with the previus one. |

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
|```chmod -R xxx <directory>```|Changes the permissions of all files and directories that are in the directory recursively.|

This command uses a string that represents the permissions.

![ inserir explicação aqui ][permissions]

* __( r )__ read permitted.

* __( w )__ write permitted.

* __( x )__ execution permitted.

### Exemples

|||
|------|------|
|```chmod 111 <file>```|Everyone could execute the file.|
|```chmod 222 <file>```|Everyone could write to the file.|
|```chmod 700 <file>```|Only the owner has all the permissions.|
|```chmod 600 <file>```|The owner could read and write the file.|

## Varieties

|Command|Description|
|------|------|
|```diff -qr <directory1> <directory2>```|Shows the differences between the directories. Argument ```-q``` shows modified or nonexistent files. Argument ```-r``` shows the differences between files content.|
|```man <command>```|Page of Manual of commands.|
|```whoami```|Who am i? Shows you username.|

## Packet manager (apt-get)

|Command|Description|
|------|------|
|```sudo apt-get install <package>```|Installs a package.|
|```sudo apt-get install -f```|Finds and fixes broken packages.|
|```sudo apt-get remove <package>```|Removes a package. Leaves user configuration files.|
|```sudo apt-get purge <package>```|Removes a package completely.|
|```sudo apt-get update```|Verifies if exists packages repository updates.|
|```sudo apt-get upgrade```|Verifies if exists system updates.|
|```sudo apt-get autoremove```|Removes all obsolete and unnecessary packages.|
|```sudo apt-get autoclean```|Cleans the packet manager cache.|
|```apt-cache search <search>```|Finds packages in repository.|
|```apt-cache show <name_of_package>```|Shows a description about the package.|

[permissions]: https://github.com/hemilioaraujo/Linux-Commands/blob/master/img/permissionsEN.PNG?raw=true
"String representation"