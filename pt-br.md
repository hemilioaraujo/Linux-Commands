# Comandos Linux

    Uma lista de comandos do terminal Linux que é comumente usada.

## Navegação

|Comando|Descrição|
|------|------|
|```pwd```|Onde estou?|
|```ls```|Exibe arquivos e diretórios.|
|```ls -l```|Exibe arquivos e diretórios de uma forma extendida.|
|```ls -lh```|Exibe arquivos e diretórios de uma forma extendida com unidade de medida.|
|```ls -a```|Exibe arquivos e diretórios inclusive os ocultos.|
|```ls -la```|Exibe arquivos e diretórios inclusive os ocultos de uma forma extendida.|
|```cd <directory>```|Vai para o diretório de destino.|
|```cd <directory>/<sub-directory>```|Vai ara o sub-diretório de destino.|
|```cd ..```|Retorna para o diretório anterior.|
|```cd ../../```|Retorna para o diretório anterior.|
|```cd /```|Vai para o diretório raiz.|
|```cd ~```|Vai para o diretório home.|
|```clear```|Limpa a tela do terminal.|
|```Ctrl + l```|Limpa a tela do terminal.|

## Manipulação de arquivos e diretórios

|Comando|Descrição|
|------|------|
|```mkdir <name>```|Cria diretório.|
|```mkdir -p <a>/<ab>/<abc>```|Cria diretório aninhado.|
|```touch <file>```|Cria arquivo.|
|```mv <file> <destination>```|Move arquivo para diretório de destino.|
|```mv <origin>/<file> .```|Move arquivo da origem para para o diretório atual.|
|```mv <directory> <new name>```|Renomeia o diretório.|
|```mv <file> <new name>```|Renomeia o arquivo.|
|```cp <file> <new copy>```|Copia arquivo para novo arquivo.|
|```cp -r <directory> <new directory>```|Copia diretório para novo diretório de forma recursiva.|
|```rm <file>```|Remove arquivo.|
|```rm -r <directory>```|Remove diretório de forma recursiva.|
|```cat <file>```|Exibe o conteúdo do arquivo.|
|```more <file>```|Exibe o conteúdo do arquivo. Carrega todo o arquivo em memória de uma vez.|
|```less <file>```|Exibe o conteúdo do arquivo. Carrega o arquivo usando streams, isso significa que o comando carrega somente a parte necessária do arquivo.(Suporta os comandos do vim)|
|```chown <user> <file>```|Altera o usuário que é dono do arquivo.|
|```chown :<grupo> <file>```|Altera o grupo de usuários que são donos do arquivo. Este comando pode ser usado junto com o comando anterior.|

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
|```diff -qr <diretory1> <diretory2>```|Shows the differences between the directories. Argument ```-q``` shows modified or nonexistent files. Argument ```-r``` shows the differences between files content.|
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