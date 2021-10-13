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
|```cd <diretório>```|Vai para o diretório de destino.|
|```cd <diretório>/<sub-diretório>```|Vai para o sub-diretório de destino.|
|```cd ..```|Retorna para o diretório anterior.|
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
|```touch <arquivo>```|Cria arquivo.|
|```mv <arquivo> <destino>```|Move arquivo para diretório de destino.|
|```mv <origem>/<arquivo> .```|Move arquivo da origem para para o diretório atual.|
|```mv <diretório> <novo nome>```|Renomeia o diretório.|
|```mv <arquivo> <novo nome>```|Renomeia o arquivo.|
|```cp <arquivo> <nova cópia>```|Copia arquivo para novo arquivo.|
|```cp -r <diretório> <novo diretório>```|Copia diretório para novo diretório de forma recursiva.|
|```rm <arquivo>```|Remove arquivo.|
|```rm -r <diretório>```|Remove diretório de forma recursiva.|
|```rm -rf <diretório>```|Remove diretório de forma recursiva, força a remoção.|
|```cat <arquivo>```|Exibe o conteúdo do arquivo.|
|```tac```|Exibe o conteúdo do arquivo ao contrário|
|```more <arquivo>```|Exibe o conteúdo do arquivo. Carrega todo o arquivo em memória de uma vez.|
|```less <arquivo>```|Exibe o conteúdo do arquivo. Carrega o arquivo usando streams, isso significa que o comando carrega somente a parte necessária do arquivo.(Suporta os comandos do vim)|
|```cut```|Remove partes de cada linha de um arquivo.|
|```tr```|Altera ou deleta caracteres de um arquivo.|
|```wc```|Conta linhas, caracteres, bytes de um arquivo.|
|```sed```|Editor de texto não interativo.|
|```awk```|Linguagem de programção, trabalha linha por linha em arquivos ou saída de comandos para buscar o que foi solicitado.|
|```nano```|Editor de texto.|
|```head```|Exibe as primeiras linhas de um arquivo.|
|```tail```|Exibe as últimas linhas de um arquivo.|
|```strings```|Exibe caracteres de um arquivo.|
|```grep```|Busca caracteres ou strings em diretórios e arquivos.|
|```grep -R```|Busca caracteres ou strings em diretórios e arquivos,recursivamente, hierarquicamente.|
|```locate```|Exibe path de um diretório ou arquivo.|
|```find```|Busca por arquivos em uma hierarquia de diretórios.|
|```echo```|Exibe uma mensagem na tela.|
|```echo $VARIAVEL```|Exibe uma variável na tela.|
|```tar```|Compressor de arquivos.|
|```tar -czvp arquivo_a_ser_criado.tar /path/arquivo_a_ser_comprimido```|Comprime o arquivo.|
|```tar -xzvf arquivo.tar.gz```|Extrai o arquivo.|
|```gzip```|Compressor de arquivos.|
|```gzip -d arquivo.gz```|Extrai arquivo.|
|```gzip -9 arquivo```|Comprime arquivo.|
|```chown <usuário> <arquivo>```|Altera o usuário que é dono do arquivo.|
|```chown :<grupo> <arquivo>```|Altera o grupo de usuários que são donos do arquivo. Este comando pode ser usado junto com o comando anterior.|

## Busca em arquivos - Comando GREP

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
|```grep ^<padrao> <arquivo>```|Busca o padrão de caracteres no inicio de uma linha em arquivo.|
|```grep <padrao>$ <arquivo>```|Busca o padrão de caracteres no fim de uma linha em arquivo.|
|```grep s.r <arquivo>```|Busca por letra s seguida por qualquer caracter seguida pela letra r.|
|```grep -w -E j.{1,}y <arquivo>```|Busca por palavras iniciadas pela letra j e terminadas em y com 3 ou mais caracteres.|
|```grep ^[aeiou] -i <arquivo>```|Busca por linhas iniciadas por vogais minúsculas e maiúsculas em um arquivo.|
|```grep ^[1-5] <arquivo>```|Busca por linhas iniciadas por 1,2,3,4 ou 5 em um arquivo.|
|```grep -E [aeiou]{2,3} <arquivo>```|Busca por linhas contendo duas ou três vogais unidas.|
|```grep -E -i '(ch\|x)[aeiou]```|Busca por linhas contendo CH ou X seguidos por vogais, ignorando maiúsculas e minúsculas.|
|```grep -E Go{2,}gle ```|Busca o padrão G seguido por 2 ou mais letras o. Reconhece Google Goooogle Gooooooooogle.|
|```grep -E Go?gle ```|Busca o padrão G seguido por 0 ou 1 letra o. Reconhece Gogle Ggle.|

## Busca em arquivos - Comando LOCATE

|Comando|Descrição|
|------|------|
|```locate <arquivo>```|Busca o arquivo pelo nome.|
|```locate -b <arquivo>```|Busca o arquivo pelo nome, listando apenas os arquivos que têm o termo de pesquisa em vez de retornar diretórios que levam aos arquivos.|
|```locate -e <arquivo>```|Busca o arquivo pelo nome, e retorna a entrada de arquivos existentes no momento que o comando Linux locate é executado.|
|```locate -q  <arquivo>```|Busca o arquivo pelo nome, e desativa a exibição de erros encontrados no processo de busca.|
|```locate -c  <arquivo>```|Busca o arquivo pelo nome, e mostra o número de arquivos correspondentes, ao invés dos nomes dos arquivos.|

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
|```man <comando>```|Manual do comando.|
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
|```ping```|Envia requisiçoes ICMP.|
|```netstat```|Mostra conexões de rede, tabelas de roteamento, estatísticas de interface e conexões mascaradas.|
|```wget```|Baixar conteudo de uma página na web.|
|```ssh```|OpenSSH SSH client (acesso remoto).|
|```base64```|Codifica/decodifica na Base64 o ARQUIVO, ou entrada padrão, para saída padrão.|
|```ldd```|Imprimi dependências de objetos compartilhados.|
|```type```|Informa se um comando é interno ou externo. Exemplo de uso: type cd|

## Monitoramento

|Comando|Descrição|
|------|------|
|```htop```| Exibe os processos em execução no sistema.|
|```vmstat```|Informações sobre processos , memória , paginação , E / S de bloco , traps , discos e atividade da CPU .|
|```free```| Observar e monitorar o uso da memória do sistema.|
|```ps```|Exibe informações sobre processos.|
|```ps -aux```|Exibe informações sobre processos, usuários, tty.|
|```kill -s```|Envia um sinal para um processo.|
|```kill -l```|Lista sinais.|
|```echo $$```|Imprimi qual o PID do processo atual.|
|```echo $!```|Imprimi qual o PID do ultimo processo executado em background.|
|```echo $?```|Imprimi o exitcode do ultimo comando, 0 sucesso, >=1 erro.|

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
|```apt-cache search <pesquisa>```|Encontra pacotes no repositório.|
|```apt-cache show <nome_do_pacote>```|Exibe a descrição sobre o pacote.|

## Execução de comandos

|Comando|Descrição|
|------|------|
|```&```|Executar em segunda plano (./script.sh &).|
|```bash -xv```|Abre outro bash em formato debug (bash -xv script.sh).|
|```;```|Executa um comando apos outro.|
|```|```|Direciona a saida de um comando para outro.|
|```&&```|Só executa o comando caso o comando anterior não retorne erro.|
|```||```|Só executa o comando caso o comando anterior retorne erro.|

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

## Variáveis

|Comando|Descrição|
|------|------|
|```VARIAVEL=valor```|Delcaração de variável.|
|```unset VARIAVEL```|Remove variável.|
|```env```|Muda o valor de uma variável para o proximo comando. Exibir variáveis globais.|
|```set```|Exibe todas variáveis do ambiente, locais e globais.|
|```export```|Exporta uma variável.|

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

[permissions]: https://github.com/hemilioaraujo/Linux-Commands/blob/master/img/permissionsPT.PNG?raw=true
"String representation"
