# Comandos Linux

    Uma lista de comandos do terminal Linux que é comumente usada.

## Navegação

|Comando|Descrição|
|------|------|
|```pwd```|Onde estou?|
|```ls```|Exibe arquivos e diretórios.|
|```ls -l```|Exibe arquivos e diretórios de uma forma extendida.|
|```ls -lh```|Exibe arquivos e diretórios de uma forma extendida, com unidade de medida.|
|```ls -a```|Exibe arquivos e diretórios, inclusive os ocultos.|
|```ls -ltr```|Lista arquivos e diretórios por data.|
|```ls -la```|Exibe arquivos e diretórios, inclusive os ocultos, de uma forma extendida.|
|```ls -F```|Classifica o conteúdo em arquivos, diretórios, executáveis e outros.|
|```ls -F <diretório>```|Classifica o conteúdo de um diretório específico.|
|```ls -d */```| Lista apenas diretórios.|
|```cd <diretório>```|Vai para o diretório de destino.|
|```cd <diretório>/<sub-diretório>```|Vai para o sub-diretório de destino.|
|```cd ..```|Retorna para o diretório anterior.|
|```cd -```|Avança para o último diretório superior visitado (desfazendo "cd ..")```.|
|```cd ../../```|Retorna para o diretório anterior.|
|```cd /```|Vai para o diretório raiz.|
|```cd ~```|Vai para o diretório home.|
|```(cd .. ;ls -l)```|Executa o comando em um "sub shell", no caso do exemplo, continua-se no mesmo diretório, após a listagem do diretório anterior.|
|```clear```|Limpa a tela do terminal.|
|```Ctrl + l```|Limpa a tela do terminal.|
|```exit```|Fecha o terminal.|

## Manipulação de arquivos e diretórios

|Comando|Descrição|
|------|------|
|```mkdir <nome>```|Cria diretório.|
|```mkdir -p <a>/<ab>/<abc>```|Cria diretório aninhado.|
|```rmdir <diretório>```|Remove o diretório, apenas se estiver vazio.|
|```rmdir -p <a>/<ab>/<abc>```|Remove a estrutura de diretórios, apenas se os diretórios estivem vazios.|
|```touch <arquivo>```|Cria arquivo.|
|```touch -m <arquivo_ja_existente>```|Altera a data de modificação.|
|```touch -a <arquivo_ja_existente>```|Altera a data do ultimo acesso.|
|```touch -t 202106060606 <arquivo_ja_existente>```|Altera a data e a hora da ultima alteração.|    
|```mv <arquivo> <destino>```|Move arquivo para diretório de destino.|
|```mv <origem>/<arquivo> .```|Move arquivo da origem para para o diretório atual.|
|```mv <diretório> <novo nome>```|Renomeia o diretório.|
|```mv <arquivo> <novo nome>```|Renomeia o arquivo.|
|```mv -i```|Solicita confirmação do usuário, antes de sobreescrever um arquivo de mesmo nome.|
|```cp <arquivo> <nova cópia>```|Copia arquivo para novo arquivo.|
|```cp -r <diretório> <novo diretório>```|Copia diretório para novo diretório de forma recursiva.|
|```rm <arquivo>```|Remove arquivo.|
|```rm -r <diretório>```|Remove diretório de forma recursiva.|
|```rm -rf <diretório>```|Remove diretório de forma recursiva, força a remoção.|
|```rm -i <arquivo>```|Solicita confirmação do usuário, antes de remover um arquivo permanentemente.|
|```rm  -I```|Questiona uma vez antes de remover mais que três arquivos ou ao remover recursivamente.| 
|```cat <arquivo>```|Exibe o conteúdo do arquivo.|
|```cat -n <arquivo>```|Retorna todas a linhas numeradas.|
|```cat -b <arquivo>```|Retorna todas as linhas numeradas, exeto as linhas em branco|
|```cat -s <arquivo>```|Suprime linhas em branco repetidas. |
|```cat -A <arquivo>```|Exibe caracteres especiais.|  
|```nl <arquivo>```|Numera as linhas de um arquivo, ignorando as linhas em bracos. Igual ao cat -b|    
|```tac <arquivo>```|Exibe o conteúdo do arquivo ao contrário|
|```more <arquivo>```|Exibe o conteúdo do arquivo. Carrega todo o arquivo em memória de uma vez.|
|```less <arquivo>```|Exibe o conteúdo do arquivo. Carrega o arquivo usando streams, isso significa que o comando carrega somente a parte necessária do arquivo.(Suporta os comandos do vim)|
|```od```|Exibe o conteúdo de um texto em octal.Ex: echo "slayer" &#124; od|
|```od -tx```|Exibe o conteúdo de um texto em hexa.|    
|```cut```|Remove partes de cada linha de um arquivo.|
|```cut -d <delimitador> <arquivo>```|Informa o delimitador dos dados, diferindo colunas (usualmente , ou ;).|
|```cut -f <n°_da_coluna> <arquivo>```|Seleciona uma coluna específica de um arquivo.|
|```tr```|Altera ou deleta caracteres de um arquivo.|
|```wc```|Conta linhas, caracteres, bytes de um arquivo.|
|```wc -l <arquivo>```|Exibe quantas linhas um arquivo possui.|
|```wc- w <arquivo>```|Exibe quantas palavras um arquivo possui.|
|```wc -c <arquivo>```|Exibe quantos caracteres um arquivo possui.|   
|```sort```|Classifica o conteúdo de um arquivo.|
|```sort -n```|Classifica o conteúdo de um arquivo em ordem númerica.|
|```sort -r```|Classifica o conteúdo de um arquivo em ordem númerica decrescente.|
|```sort -k 2```|Ordena as linhas de acordo com o campo passado, no caso 2.|    
|```uniq```|Filtra linhas repetidas em uma coluna de dados.|
|```uniq -c```|Informa a quantidade de repetições de cada linha.|
|```uniq -d```|Informa o conteúdo das linhas duplicadas.|
|```sed```|Editor de texto não interativo.|
|```awk```|Linguagem de programção, trabalha linha por linha em arquivos ou saída de comandos para buscar o que foi solicitado.|
|```nano```|Editor de texto.|
|```emacs```|Editor de texto.|    
|```head```|Exibe as primeiras linhas de um arquivo.|
|```head -n3 <arquvio>```|Exibe as 3 linhas primeiras de um arquivo.|
|```head -c100 <arquivo>```|Exibe os 100 primeiros bytes de um arquivo.|    
|```tail <arquivo>```|Exibe as últimas linhas de um arquivo.|
|```tail -n5 <arquivo>```|Exibe as ultimas 5 linhas de um arquivo.|
|```tail -f <arquivo>```|Exibe a atulização de um arquivo em tempo real. Util para verificar logs.|    
|```strings```|Exibe caracteres de um arquivo.|
|```join <arquivo1> <arquivo2>```|Combina dois arquivos, através de um indice. As linhas devem estar na mesma ordem.|
|```join -j2 <arquivo1> <arquivo2> ```|Muda o indice a ser usado, no caso sera usada a segunda coluna.|
|```paste <arquivo1> <arquivo2> ```|Combina dois arquivos, linha por linha.|
|```split ```|Divide um arquivo em varios. Por padrão, a cada 1000 linhas.|    
|```echo```|Exibe uma mensagem na tela.|
|```file <arquivo>```|Exibe o tipo do arquivo.|    
|```chown <usuário> <arquivo>```|Altera o usuário que é dono do arquivo.|
|```chown :<grupo> <arquivo>```|Altera o grupo de usuários que são donos do arquivo. Este comando pode ser usado junto com o comando anterior.|
|```du```|Mostra estatísticas de uso do disco, isto informações sobre espaço em disco que arquivos ou pastas ocupam.|
|```du -h /folder_a```|Mostra o espaço em disco da pasta com caminho "/folder_a". A opção "-h" converte uma saída para um formato mais legível para humanos (por exemplo, Megabytes)|
|```tee```|Envia o conteúdo para a tela e para um arquivo. Exemplo: ls -l /home/ &#124; tee arquivosHome.txt|    

### Compressão de arquivos

Os comandos para comprimir arquivos podem ser utilizados em qualquer arquivo, não preicsa ser arquivos .tar.
Tais comandos possuem algumas diferenças no algoritimo, o que influencia na velocidade de compressão e tamanho final do arquivo comprimido.    

    
|Comando|Descrição|
|------|------|    
|```tar```|Agrupador de arquivos.|
|```tar -c```|Criar um arquivo a ser agrupado.|
|```tar -f```|Define o nome do arquivo.|
|```tar -v```|Verbose.|    
|```tar -x```|Extrair arquivos.|
|```tar -t```|Listar arquivos que existem dentro de um arquivo agrupado.|  
|```tar -p```|Mantem as permissoẽs dos arquivos que foram agrupados.|  
|```gzip```|Compressor de arquivos.|  
|```gzip <arquivo.tar>```|Comprime o arquivo .tar > .tar.gz|
|```gzip -d <arquivo.gz>```|Descomprime arquivo .gz|
|```gzip -kd <arquivo.gz>```|Descomprime arquivo e mantem o arquivo original.|    
|```gunzip <arquivo.gz>```|Descomprime arquivo .gz|
|```bzip2```|Compressor de arquivos.|
|```bzip2 -k <arquivo.tar>```|Comprime arquivo tar > tar.bz2, mantem o arquivo original.|
|```bzip2 -d <arquivo.bz2>```|Descomprime arquivo .bz2|
|```bunzip2 -d <arquivo.bz2>```|Descomprime arquivo .bz2|
|```xz```|Compressor de arquivos.| 
|```xz -k <arquivo.tar>```|Comprime o arquivo .tar > tar.xz, mantem arquivo original|
|```xz -d <arquivo.xz>```|Descomprime arquivo .xz|
|```unxz <arquivo.xz>```|Descomprime arquivo .xz|    
|```tar -zcvpf <arquivo_a_ser_criado.tar> </path/arquivo_a_ser_comprimido>```|Agrupa e comprime arquivos utilizando o tar e o gzip (.tar.gz ou tgz).|
|```tar -zxvf arquivo.tar.gz```|Extrai e descomprime o arquivos utilizando o gzip (tar.gz ou tgz).|
|```tar -jcvpf <arquivo_a_ser_criado.tar> </path/arquivo_a_ser_comprimido>```|Agrupa e comprime arquivos utilizando o tar e o bzip2 (.tar.bz2 ou tbz).|
|```tar -jxvf arquivo.tar.gz```|Extrai e descomprime o arquivos utilizando o bzip2 (tar.bz2 ou tbz).|  
|```tar -Jcvpf <arquivo_a_ser_criado.tar> </path/arquivo_a_ser_comprimido>```|Agrupa e comprime arquivos utilizando o tar e o xz (.tar.xz ou txz).|
|```tar -Jxvf arquivo.tar.gz```|Extrai e descomprime o arquivos utilizando o xz (tar.xz o txz).|
|```cpio```|Agrupador de arquvios, deve receber uma lista de arquivos como entrada. Ex: find ./ -name wordlist1* &#124; cpio -o &#124; gzip > backup.cpio.gz|
|```cpio -i < backup.cpio```|Desagrupar arquivos.|
|```gunzip -c backup.cpio \| cpio -i```|Descomprimir e desagrupar arquivos.|
    
    
### Busca em arquivos - Comando GREP - REGEX

|Comando|Descrição|
|------|------|
|```grep <padrao> <arquivo>```|Busca o padrão de caracteres em arquivo.|
|```grep -i <padrao> <arquivo>```|Busca o padrão de caracteres em arquivo, ignorando diferenças entre maiúsculas e minúsculas.|
|```grep -v <padrao> <arquivo>```|Busca o padrão inverso de caracteres em arquivo, retorna as linhas que não obedecem o padrão procurado.|
|```grep --color <padrao> <arquivo>```|Exibe o padrão encontrado colorido.|
|```grep -c <padrao> <arquivo>```|Retorna o número de linhas que obedecem o padrão procurado.|
|```grep -n <padrao> <arquivo>```|Exibe junto ao padrão encontrado o número da linha do arquivo onde o padrão econtra-se.|
|```grep -w <padrao> <arquivo>```|Busca o padrão de caracteres em arquivo, retorna apenas as linhas onde o padrão encontra-se em palavras completas. |
|```grep -R <padrao>```|Busca o padrão em diretórios e arquivos,recursivamente, hierarquicamente.|
|```grep -R -l <padrao>```|Busca o padrão em diretórios e arquivos,recursivamente, hierarquicamente, retornando o nome do arquivo que contém o padrão procurado|
|```fgrep```|Não aplica regex.|    
|```grep ^<padrao> <arquivo>```|Busca o padrão de caracteres no inicio de uma linha em arquivo.|
|```grep <padrao>$ <arquivo>```|Busca o padrão de caracteres no fim de uma linha em arquivo.|
|```grep s.r <arquivo>```|Busca por letra s seguida por qualquer caracter seguida pela letra r.|
|```grep -w -E j.{1,}y <arquivo>```|Busca por palavras iniciadas pela letra j e terminadas em y com 3 ou mais caracteres.|
|```grep ^[aeiou] -i <arquivo>```|Busca por linhas iniciadas por vogais minúsculas e maiúsculas em um arquivo.|
|```grep ^[1-5] <arquivo>```|Busca por linhas iniciadas por 1,2,3,4 ou 5 em um arquivo.|
|```grep -E```|Expande o conjunto regex, necessário a proteção dos caracteres especiais.|    
|```grep -E [aeiou]{2,3} <arquivo>```|Busca por linhas contendo duas ou três vogais unidas.|
|```grep -E -i '(ch\|x)[aeiou]```|Busca por linhas contendo CH ou X seguidos por vogais, ignorando maiúsculas e minúsculas.|
|```grep -E Go{2,}gle ```|Busca o padrão G seguido por 2 ou mais letras o. Reconhece Google Goooogle Gooooooooogle.|
|```grep -E Go?gle ```|Busca o padrão G seguido por 0 ou 1 letra o. Reconhece Gogle Ggle.|
|```egrep```|Expande o conjunto de regex, não é necessário proteger os caracteres especiais.|
|```egrep "b[aeio]u"```|Busca pelo padrão começado com 'b', seguido por 'a','e','i' ou 'o' e terminado em 'u'.|
|```egrep "b[a-z]g"```|Busca pelo padrão começado com 'b', que possuam qualquer letra em sequência, e terminado com 'g'.|
|```egrep "^A" <arquivo>```|Busca todas linhas começadas com 'A'.|
|```egrep "a$" <arquivo>```|Busca todas as linhas terminadas com 'a'.|
|```egrep -v "^$"```|Não exibe as linhas em branco.|
|```egrep "b[a-z]g*```|O '*' indica que a letra 'g' pode ou não estar na busca, ou pode ser repetida várias vezes.|
|```egrep "b[a-z]g+```|O '+' indica que o 'g' deve aparecer pelo menos uma vez.|
|```egrep "b[a-z]g?```|O '?' indica que o 'g' pode aparecer nenhuma ou apenas uma vez.|
|```egrep "b[a-z]g.```|O '.' indica que após a letra 'g' deve haver um caractere.|
    
    
### Busca de arquivos

|Comando|Descrição|
|------|------|
|```locate <arquivo>```|Busca o arquivo pelo nome. Exibe path de um diretório ou arquivo.|
|```locate -b <arquivo>```|Busca o arquivo pelo nome, listando apenas os arquivos que têm o termo de pesquisa em vez de retornar diretórios que levam aos arquivos.|
|```locate -e <arquivo>```|Busca o arquivo pelo nome, e retorna a entrada de arquivos existentes no momento que o comando Linux locate é executado.|
|```locate -q  <arquivo>```|Busca o arquivo pelo nome, e desativa a exibição de erros encontrados no processo de busca.|
|```locate -c  <arquivo>```|Busca o arquivo pelo nome, e mostra o número de arquivos correspondentes, ao invés dos nomes dos arquivos.|
|```find```|Busca por arquivos em uma hierarquia de diretórios.|
|```find <diretório> > <arquivo>```|Salvar resultado da busca em um arquivo|
|```find <diretório> -name <arquivo>```|Busca em um arquivo pelo nome|    
|```find <diretório> -mtime -days -ls```|Buscar arquivos modificados nos últimos N dias|
|```which```|Localiza arquivos/comandos incluidos no PATH|
    
## Histórico

|Comando|Descrição|
|------|------|
|```history```|Exibe o histórico de comandos.|
|```history -c```|Limpa o arquivo de histórico.|
|```Ctrl + r```|Inicia a busca interativa no histórico ou encontra a próxima ocorrência quando a busca interativa já foi iniciada.|
|```!n```|Executa o comando número 'n'.|
|```!!```|Repete o comando anterior.|
|```!<string>```|Repete o comando anterior que inicia com 'string'.|
|```dirs -p```|Exibe o histórico de diretórios visitados.|

## Permissões

|Comando|Descrição|
|------|------|
|```chmod xxx <arquivo or diretório>```|Altera as permissões do usuário, grupo ou todos para ler, escrever ou executar o arquivo.|
|```chmod -R xxx <diretório>```|Altera a permissão de todos arquivos e diretórios que estão no diretório recursivamente.|

Este comando usa uma string para representar as permissões.

![ inserir explicação aqui ][permissions]

* __( r )__ permitido leitura.

* __( w )__ permitido escrita.

* __( x )__ permitido executar.

### Exemplos

|Comando|Descrição|
|------|------|
|```chmod 111 <arquivo>```|Todos podem executar o arquivo.|
|```chmod 222 <arquivo>```|Todos podem escrever no arquivo.|
|```chmod 700 <arquivo>```|Somente o dono do arquivo tem todas as permissões.|
|```chmod 600 <arquivo>```|O dono do arquivo pode ler e escrever.|

## Variedades

|Comando|Descrição|
|------|------|
|```diff -qr <diretório1> <diretório2>```|Exibe as diferenças entre os diretórios. Argumento ```-q``` exibe arquivos modificados ou não existentes. Argumento ```-r``` exibe a diferença entre o conteúdo dos arquivos.|
|```info <comando>```|Ajuda sobre comando passado.|
|```man <comando>```|Manual do comando.|
|```man -k <descrição>```|Retorna comandos de acorda com adescrição passada.|
|```apropos <descrição>```|Retorna possiveis comandos de acordo com a descrição passada. Exemplo de uso: apropos download|  
|```whoami```|Quem sou eu? Exibe seu usuário.|
|```whatis```|Exibe o que é um comando.|
|```date```|Exibe data e hora.|
|```ps```|Exibe informações sobre processos.|
|```ps -aux```|Exibe informações sobre processos, usuários, tty.|
|```expr```|Avaliar expressões.|
|```sleep 1```|Pausa a execução por um determinado tempo, no caso 1 segundo.|
|```uname```|Exibe informações sobre o sistema.|
|```uname -r```|Exibe informações sobre o kernel.|
|```hostname```|Exibe ou seta hostname do sistema.|
|```curl```|Faz requisições web.|
|```curl google.com -O google.html```|Faz requisições web e faz download da página/arquivo.|    
|```ping```|Envia requisiçoes ICMP.|
|```lshw```|Lista hardware.|    
|```netstat```|Mostra conexões de rede, tabelas de roteamento, estatísticas de interface e conexões mascaradas.|
|```wget```|Baixar conteudo de uma página na web.|   
|```ssh```|OpenSSH SSH client (acesso remoto).|
|```base64```|Codifica/decodifica na Base64 o ARQUIVO, ou entrada padrão, para saída padrão.|
|```ldd```|Imprimi dependências de objetos compartilhados.|
|```type```|Informa se um comando é interno ou externo. Exemplo de uso: type cd|
|```traceroute```|Informa a rota (ou lista de servidores) que um pacote toma até chegar a seu host de destino. Exemplo de uso: traceroute 8.8.8.8|
|```alias```|Permite apelidos para comandos. Exemplo: Executar "alias lx = ls -lha" torna possível obter o mesmo resultado de "ls -lha" apenas executando "lx" |
|```unalias```|Remove um alias ativo.|
|```ip -br a```|Qual o meu IP na minha rede local? Este comando exibe o IP na rede local de cada placa de rede usando o novo pacote de rede do linux (iproute2util) |
|```ifconfig```|Qual o meu IP na minha rede local? Este comando exibe o IP (e também algumas outras informações) na rede local de cada placa de rede porém usando o pacote antigo de reded do linux (net-tools), caso queria ver apenas o IP de placas de rede sem fio você pode usar o "iwconfig"  |

## Monitoramento
    
Processos possuem permissões e prioridades, não é possivel matar os processos de outro usuário, somente o root consegue. Os valores nice de um processo podem ser definidos de -20 a +19, quanto menor o valor, mais prioridade o processo vai ter, por padrão o valor inicial é 0. Somente o root pode aumentar a prioridade de um processo, usuários comuns podem apenas diminuir.
    
|Comando|Descrição|
|------|------|
|```uptime```|Exibe hora, há quanto tempo o sistema está ligado, quantidade de usuários logados e load avarege(consumo médio de processos por CPU).|    
|```htop```| Exibe os processos em execução no sistema.|
|```vmstat```|Informações sobre processos , memória , paginação , E / S de bloco , traps , discos e atividade da CPU .|
|```free```|Exibe a quantidade de memória e swap utilizada pelo sistema, em kb.|
|```free -m / -g```|Exibe a quantidade de memória e swap utilizada pelo sistema, em mb / gb.|
|```ps```|Informações sobre os processos do usuário logado, somente no tty atual.|
|```ps -u```|Adicina algumas informçoes sobre sobre os processos no terminal atual.|    
|```ps -x```|Adiciona processos processos do usuario autal que estão em outro tty.|
|```ps -ax```|Exibe os processos de todos os usuarios.|
|```ps -f```|Exibe subprocessos em formato de árvore.|
|```ps -l/-w```|Exibe os processos e usuarios em um formato diferente.|
|```ps -C <nome do processo>```|Busca somente o processo passado.|
|```pstree```|Mostra os processos em hierarquia de execução, em formato de árvore.|
|```pstree -p```|Adiciona o PID na exibição.|
|```pgrep bash -u root```|Exibe o PID de todos os processos bash do usúario root.|  
|```echo $$```|Imprimi qual o PID do processo atual.|
|```echo $!```|Imprimi qual o PID do ultimo processo executado em background.|
|```echo $?```|Imprimi o exitcode do ultimo comando, 0 sucesso, >=1 erro.|
|```jobs```|Lista os processos rodando em background.|
|```jobs -l```|Lista os processos em background e exibe o PID.|
|```bg```|Muda o ultimo processo rodando em foreground para background (ctr+z para parar a execução (SIGSTOP) de um processo em foreground sem mata-lo).|
|```fg```|Muda o  ultimo processo em background para foregorund.|
|```fg/bg <job ID>```|Muda o job passado.|
|```nohup```|Evita que o processo recebe sinais, execeto SIGKILL e envia a saída de um processo em backgorund para o arquivo nohup.out |
|```watch <comando>```|Executa um comando periodicamente, mostrando os resultados.|
|```watch -nX <comando>```|Exexuta um comando a cada X segundos, o padrão é 2 segundos.|
|```nice <comando>```|Executa um processo com o valor de prioridade modificado, por padrão com o valor +10.|
|```nice -n 15 <comando>```|Executa um processo com prioridade +15 (baixa prioridade).|
|```nice -15 <comando>```|Executa um processo com prioridade +15 (baixa prioridade).|
|```nice -n -15 <comando>```|Executa um processo com prioridade -15 (Alta prioridade).|
|```nice --15 <comando>```|Executa um processo com prioridade -15 (Alta prioridade).|
|```renice```|Altera a prioridade de um processo já em execução.|
|```renice -n 6 <PID>```|Altera para 6 a prioridade do processo que foi passado.|
|```renice 6 <PID>```|Altera para 6 a prioridade do processo que foi passado.|
|```renice -n -6 <PID>```|Altera para -6 a prioridade do processo que foi passado.|
|```renice -6 <PID>```|Altera para -6 a prioridade do processo que foi passado.|
|```renice -n 6 -u <usuário>```|Altera para 6 a prioridade de todos os processos do usuário que foi passado.|
|```renice -n 6 -g <grupo>```|Altera para 6 a prioridade de todos os processos do grupo que foi passado.|    

KILL
    
|Comando|Descrição|
|------|------|    
|```kill -s```|Envia um sinal para um processo. Exemplo: kill -9 1337 .Envia sigkill para o processo com PID 1337.|
|```kill -l```|Lista sinais.|
|```killall <nome do processo>```|Mata os processos que o usuário seja dono, baseado no nome passado.|
|```pkill <nome do processo>```|Encontra o processo e envia o sinal, baseado no nome passado.|
    
Alguns sinais:
    
|Sinal|Descrição|
|------|------|
|```SIGHUP```|Pode ser usado para terminar, reiniciar, ou fazer que o processo releia suas configuraçõeso, código 1.|
|```SIGINT```|Interrompe o processo, código 2.|
|```SIGQUIT```|Fecha o processo, código 3.|
|```SIGKILL```|Mata o processo abruptamentem, código 9.|
|```SIGTERM```|Solicita ao processo que finalize, sinal padrão docomando kill, código 15.|
|```SIGSTOP```|Para o processo, não pode ser ignorado, código 19.|
|```SIGSTP```|Para o processo, pode ser ignorado, código 20.|
   
    
## Gerenciador de pacotes (apt-get)

|Comando|Descrição|
|------|------|
|```sudo apt-get install <pacote>```|Instala pacote.|
|```sudo apt-get install -f```|Encontra e corrige pacotes danificados.|
|```sudo apt-get remove <pacote>```|Remove pacote. Mantendo os arquivos de configuração do usuário.|
|```sudo apt-get purge <pacote>```|Remove pacote completamente.|
|```sudo apt-get update```|Verifica se existe atualização no repositório de pacotes.|
|```sudo apt-get upgrade```|Verifica se existe atualização do sistema.|
|```sudo apt-get autoremove```|Remove todos os pacotes obsoletos e desnecessários.|
|```sudo apt-get autoclean```|Limpa o cache do gerenciador de pacotes.|
|```sudo apt list --upgradable```|Lista pacotes que podem ser atualizados.|    
|```sudo apt-cache search <pesquisa>```|Encontra pacotes no repositório.|
|```sudo apt-cache show <nome_do_pacote>```|Exibe a descrição sobre o pacote.|

## Execução de comandos

|Comando|Descrição|
|------|------|
|```&```|Executar em segunda plano (./script.sh &).|
|```bash -xv```|Abre outro bash em formato debug (bash -xv script.sh).|
|```;```|Executa um comando apos outro.|
|```\|```|Direciona a saida de um comando para outro.|
|```&&```|Só executa o comando caso o comando anterior não retorne erro.|
|```\|\|```|Só executa o comando caso o comando anterior retorne erro.|

### Executando um comando dentro de outro

|Comando|Descrição|
|------|------|
|```echo "A versão do kernel é:" `uname -r` ```|Utilizando crase.|
|```echo "A versão do kernal é:" $(uname -r)```|Utilizando $().|    
    
## XARGS

|Comando|Descrição|
|------|------|
|```xargs```|Executa um comando com argumentos em uma determinada lista, por padrão executa o comando echo sobre a entrada padrão, para sair Ctrl + D.|
|```xargs -a <arquivo> -n 2```| Lê os argumentos de um arquivo não da entrada padrão, exibindo dois por linha.|
|```xargs -a <arquivo> mkdir```| Cria uma lista de diretórios baseada em um arquivo.|
|```find . -type f -print | xargs -0 md5sum```| Calcula o HASH MD5 de todos os arquivos no diretório corrente.|
|```xargs -a hosts -P 10 -n1 -I '{}' ping '{}' -q -c 1 -w 1``` | Varre todos IPS no arquivo hosts de maneira paralela, substituindo as chaves pelo IP.|

## Redirecionamento de entreada e saida

|Comando|Descrição|
|------|------|
|```/dev/null```|Lugar nenhum, lixeira.|
|```>```|Envia a saida de um comando para um arquivo, sobrescreve o arquivo.|
|```>>```|Envia a saida de um comando para um arquivo, concatena com conteudo já existente.|
|```2>```|Saida de erro.|
|```2>>```|Saida de erro.|
|```2>1```|Redireciona saida de erro e de sucesso para o mesmo arquivo.|
|```2>>1```|Redireciona saida de erro e de sucesso para o mesmo arquivo.|
|```<<<```|Redireciona o que segue como se fosse o conteudo de um arquivo texto. Exemplo: tr a-z A-Z <<< "comandos linux.txt". Saída: COMANDOS LINUX.TXT |
|```tr a-z A-Z << end```| A variavel "end"(pode ser qualquer string) indica ao shell que a entrada termina naquele ponto, e então ele irá enviar a entrada para o comando. Exemplo: tr a-z A-Z << end <enter> até que a string definida seja escrita todas as letras serão exibidas em caixa alta end.|
    
## Variáveis

|Comando|Descrição|
|------|------|
|```VARIAVEL=valor```|Delcaração de variável.|
|```unset VARIAVEL```|Remove variável.|
|```env```|Muda o valor de uma variável para o proximo comando. Exibir variáveis globais.|
|```set```|Exibe todas variáveis do ambiente, locais e globais.|
|```export```|Exporta uma variável.|
|```echo $VARIAVEL```|Exibe uma variável na tela.|
    
### Algumas Variáveis do Sistema

|Variável|Descrição|
|------|------|
|```DISPLAY```|Indica às aplicações gráficas onde as janelas deverão ser exibidas.|
|```HISTFILE```|Arquivo do histórico de comandos.|
|```HISTFILESIZE```|Quantidade de linhas/comandos armazenados no arquivo de histórico.|
|```HOME```|Diretório home do usuário atual.|
|```LOGNAME e USER```|Nome do usuário atual.|
|```PATH```|Diretórios que o Linux busca por arquivos executáveis.|
|```PS1```|Aparência do prompt do shell.|
|```PWD```|Diretório atual.|
|```OLDPWD```|Diretório anterior.|

## Partições

|Comando|Descrição|
|------|------|    
|```df```|Relatar o uso de espaço em disco do sistema de arquivos.|
|```dd```|Converte e copia arquivos, usado para copiar uma partição inteira, para outra partição, para um arquivo, ou um arquivo para uma partição.Ex: dd if=/dev/sdb5 of=particao.img (if=entrada df=saida). Util para criar pendrive bootavel.|
|```lsblk```|Lista dispositivos e partições|   

## Algoritimos de hash para checksum
Utiliza-se a flg -c para comparar o aqruivo com a hash original e a hash gerada com arquivo baixado.

|Comando|Descrição|
|------|------|     
|```md5sum```|Gera hash em md5|
|```sha1sum```|Gera hash em sha1|
|```sha256sum```|Gera hash em sha256|
|```sha512sum```|Gera hash em sha512|
    
## VIM
    
### Edição
|Comando|Descrição|
|------|------|    
|```a```|Editar a partir do próximo caractere.|
|```A```|Editar a partir do fim da linha.|
|```i```|Editar a partir do caractere atual.|
|```o```|Editar a partir da proxima linha.|
|```O```|Editar a partir Linha Anterior.|
|```s```|Deletar char e editar.|
|```S```|Deletar linha e editar.|
|```C```|Deletar ate o final da linha e editar.|
|```r```|Realocar um caractere.|
|```R```|Modo De Realocação.|
|```U```|Desfazer mudanças.|
|```ESC```|Sair do modo de inserção.|

### Modo Visual
    
|Comando|Descrição|
|------|------|    
|```v```|Entrar no modo visual.|
|```V```|Entrar no modo visual(linha).|
|```d / x```|Recortar/deletar seleção.|
|```s```|Realocar seleção.|
|```y```|Copiar seleção.|
|```ESC```|Sair do modo visual.|

### Sair
    
|Comando|Descrição|
|------|------|    
|```:qa```|Fechar todos arquivos.|
|```:qa!```|Fechar todos arquivos sem salvar.|
|```:w```|Salvar.|
|```:w <novo_arquivo>```|Salvar e sair, caso  o arquivo não possua nome.|
|```:wq / :x```|Salvar e fechar.|
|```:q```|Fechar arquivo.|
|```:q!```|Fechar arquivo sem salvar.|
|```ZZ```|Salvar e sair.|
|```ZQ```|Sair sem checar mudanças.|

### Navegação

Buscar string

|Comando|Descrição|
|------|------|    
|```b/w```|string anterior/próxima.|
|```ge/e```|Final da string anterior/próxima.|

Linhas

|Comando|Descrição|
|------|------|    
|```0```|Inicio da linha.|
|```^```|Inicio da linha(pula identação).|
|```$```|Final da linha.|

Caracteres 
    
|Comando|Descrição|
|------|------|
|```f<char>```|Vai até o char indicado (próximo).|
|```F<char>```|Vai até o char indicado (anterior).|

Documento
    
|Comando|Descrição|
|------|------|
|```gg```|Primeira Linha.|
|```G```|Ultima linha.|
|```:n```|Vai até linha n.|
|```nG```|vai até linha n.|

Clipboard
    
|Comando|Descrição|
|------|------|
|```x```|Deletar caractere.|
|```dd```|Recortar/deletar linha.|
|```dN```|Recortar/deletar a linha do cursor e mais n abaixo. Substitua N por um número.|
|```yy```|Copiar linha.|
|```yN```|Copiar linhas do cursor e mais n abaixo. Substitua N por um número.|
|```p```|Colar.|
|```P```|Colar antes.|
|```u```|Recupera linha apagada.|

Pesquisa
|Comando|Descrição|
|------|------|
|```?<string>```|Pesquisar, do final para o começo.|
|```/<string>```|Pesquisar, do começo para o final.|
|```n```|Próxima ocorrência.|
|```N```|Ocorrência anterior. |

Lista de operadores

|Comando|Descrição|
|------|------|   
|```d```|Deletar.|
|```y```|Copiar.|
|```C```|Deletar e inserir.|
|```>```|Identação para direita.|
|```<```|Identação para esqueda.|
|```=```|Auto identação.|
|```g~```|Trocar caixa.|
|```gU```|Caixa alta.|
|```gu```|Caixa baixa.|
|```:!<cmd>```|Executa um comando externo.|
|```:e/:e!```|Atualiza o arquivo, caso tenha sido modificado enquanto aberto.|
|```:X```|Criptografa o arquivo.|
|```:shell```|Saída temporária para o shell, retorna com ctrl+d.|
|```:x,y mov z```|Move as linhas x e y para a linha z.|
|```:h```|Abre o manual de ajuda do Vim.|

Identação
    
|Comando|Descrição|
|------|------|
|```:set tabstop=8```|Determina o número de colunas inseridas ao utilizar tecla TAB.|
|```:expandtab```|Produz o número apropiado de espaços ao pressionar a tecla TAB.|
|```:retab```|Converte o arquivo com a nova configuração de tab.|   
    
## tmux
    
|Comando|Descrição|
|------|------|
|```tmux```|Terminal multiplexer.|
|```tmux ls/list-sessions " ```|Lista sessões do tmux.|
|```tmux kill-session -t <x>```|Encerra sessão x do tmux|    
|```tmux attach -t <numero> " ```|Conecta na sessão x do temux.|
|```tmux new -s <nome> " ```|Abrir uma nova conexão, caso já existir alguma.|
|```ctrl+b :kill-session ```|Encerra sessão do tmux.|
|```ctrl+b d ```|Desconecta do tmux.|
|```ctrl+b c ```|Cria uma nova aba.|
|```ctrl+b , ```|Renomeia uma aba.|
|```ctrl+b p ```|Volta uma aba.|
|```ctrl+b n ```|Avança para a próxima aba.|
|```ctrl+b l ```|Volta para a aba anterior.|
|```ctrl+b f ```|Procurar aba.|
|```ctrl+b w ```|Lista todas as abas.|
|```ctrl+b & ```|Matar aba.|
|```ctrl+b <número> ```|Vai para aba numero x.|
|```ctrl+b % ```|Divide a janela ao meio, verticalmente.|
|```ctrl+b " ```|Divide a janela ao meio, horizontalmente.|
|```ctrl+b <seta direcional> ```|Alternar entre janelas.|
|```ctrl+b (mantendo pressionado) <seta direcional>  ```|Aumentar/diminuir tamanho da janela.|
|```ctrl+b o ```|Alternar entre janelas.|

## screen
|Comando|Descrição|
|------|------|
|```screen```|Terminal multiplexer.|
|```screen -ls```|Mostra se o screen esta ativo.|
|```screen -r```|Retorna a sessão screen.|
|```screen <comando>```|Inicia o screen rodando o comando passado.|
|```ctrl+a c ```|Cria uma nova aba.|
|```ctrl+a n```|Ir para a próxima aba.|
|```ctrl+a d```|Sai da sessão do screen, mantém a execução em segundo plano.|
|```ctrl+a n```|Ir para a próxima aba.|
|```ctrl+a s```|Divide janela ao meio, horizontalmente.|     
|```ctrl+a a```|Desfazer.|
|```ctrl+a TAB```|Mudar para próxima aba.|
|```ctrl+a X```|Fechar aba.|     
|```exit```|Fecha a aba atual do screen.|    
    
[permissions]: https://github.com/hemilioaraujo/Linux-Commands/blob/master/img/permissionsPT.PNG?raw=true
"String representation"
