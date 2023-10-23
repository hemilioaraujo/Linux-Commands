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
|```ls -ltr```|List files and directories by date.|
|```ls -la```|List all files and directories including the hidden ones in an extended form.|
|```cd <directory>```| Change to destination directory|
|```cd <directory>/<sub-directory>```| Change to destination sub-directory.|
|```cd ..```|Go back to previous directory.|
|```cd ../../```|Go back to previous directory.|
|```cd /```|Go to root directory.|
|```cd ~```|Go to home directory.|
|```(cd .. ;ls -l)```|Execute the command in a "sub shell", in the case of the example, continue in the same directory, after listing the previous directory.|
|```clear```|Clear the terminal screen.|
|```Ctrl + l```|Clear the terminal screen.|
|```exit```|Close the terminal.|
|```ctrl + c```|Terminates an application currently running in the terminal|

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

## Search for terms in files - GREP Command

|Command|Description|
|------|------|
|```grep <term> <file>```|Fetch character pattern in file.|
|```grep -i <term> <file>```|Searches the character pattern in file, ignoring differences between upper and lower case.|
|```grep -v <term> <file>```|Searches for the inverse pattern of characters in file, returns the lines that do not conform to the pattern.|
|```grep --color <term> <file>```|Displays the pattern found in color.|
|```grep -c <term> <file>```|Returns the number of lines that match the pattern you are looking for.|
|```grep -n <term> <file>```|Displays next to the pattern found the line number of the file where the pattern is found.|
|```grep -w <term> <file>```|Searches for the pattern of characters in file, returns only the lines where the pattern is in complete words. |
|```grep -R <term>```|Search the pattern in directories and files, recursively, hierarchically.|
|```grep -R -l <term>```|Searches the pattern in directories and files, recursively, hierarchically, returning the name of the file containing the pattern you are looking for.|
|```grep ^<term> <file>```|Searches for the character pattern at the beginning of a line in file.|
|```grep <term>$ <file>```|Searches for the character pattern at the end of a line in file.|
|```grep s.r <file>```|Searches for the pattern letter s followed by any character followed by the letter r.|
|```grep -w -E j.{1,}y <file>```|Searches for words starting with the letter j and ending with y with 3 or more characters.|
|```grep ^[aeiou] -i <file>```|Search for lines beginning with lowercase and uppercase vowels in a file.|
|```grep ^[1-5] <file>```|Search for lines starting with 1,2,3,4 ou 5 in a file.|
|```grep -E [aeiou]{2,3} <file>```|Search for lines containing two or three joined vowels.|
|```grep -E -i '(ch\|x)[aeiou]```|Searches for lines containing CH or X followed by vowels, ignoring upper and lower case.|
|```grep -E Go{2,}gle ```|Search for G followed by 2 or more letters o. Recognizes Google Goooogle Gooooooooogle.|
|```grep -E Go?gle ```|Search by letter G followed by 0 or 1 letter o. Recognizes Gogle Ggle.|

## Search files - Command LOCATE

|Command|Description|
|------|------|
|```locate <file>```|Search for the file by name.|
|```locate -b <file>```|Search for the file by name, listing only the files that have the search term instead of returning directories that lead to the files.|
|```locate -e <file>```|Search for the file by name, and returns the entry of existing files at the time the Linux locate command is executed.|
|```locate -q  <file>```|Search for the file by name, and disable the display of errors found in the search process.|
|```locate -c  <file>```|Search for the file by name, and shows the number of matching files, instead of the file names.|


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

|Command|Description|
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
|```whatis```|Displays what a command is.|
|```date```|Displays date and time.|
|```ps```|Displays information about processes.|
|```ps -aux```|Displays information about processes, users, tty.|
|```expr```|Evaluate expressions.|
|```sleep 1```|Pauses execution for a certain time, in this case 1 second.|
|```uname```|Displays system information.|
|```uname -r```|Displays information about the kernel.|
|```hostname```|Displays or sets system hostname.|
|```curl```|Make web requests.|
|```ping```|Send ICMP requests.|
|```netstat```|Shows network connections, routing tables, interface statistics and masked connections.|
|```wget```|Download content from a web page.|
|```ssh```|OpenSSH SSH client (remote access).|
|```base64```|Base64 encodes / decodes the FILE, or standard input, to standard output.|

## Monitoring

|Command|Description|
|------|------|
|```htop```|Displays processes running on the system.|
|```vmstat```|Information about processes, memory, paging, block I / O, traps, disks and CPU activity.|
|```free```|Watch and monitor system memory usage.|
|```stat <file\|directory>```|Prints the given file or directory INode informations.|

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
