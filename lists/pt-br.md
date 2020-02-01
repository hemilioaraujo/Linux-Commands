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
|```ls -ltr```|Lsta arquivos e diretóios por data.|
|```ls -la```|Exibe arquivos e diretórios inclusive os ocultos de uma forma extendida.|
|```cd <diretório>```|Vai para o diretório de destino.|
|```cd <diretório>/<sub-diretório>```|Vai ara o sub-diretório de destino.|
|```cd ..```|Retorna para o diretório anterior.|
|```cd ../../```|Retorna para o diretório anterior.|
|```cd /```|Vai para o diretório raiz.|
|```cd ~```|Vai para o diretório home.|
|```(cd .. ;ls -l)```|executa o comando em um "sub shell", no caso do exemplo, continua-se no mesmo diretóio após a listagem do diretóio anterior.|
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
|```tac```|Exibe o conteúdo do arquivo, ao contrario|
|```more <arquivo>```|Exibe o conteúdo do arquivo. Carrega todo o arquivo em memória de uma vez.|
|```less <arquivo>```|Exibe o conteúdo do arquivo. Carrega o arquivo usando streams, isso significa que o comando carrega somente a parte necessária do arquivo.(Suporta os comandos do vim)|
|```cut```|Remove partes de cada linha de um arquivo.|
|```tr```|Altera ou deleta caracteres de um arquivo.|
|```wc```|Conta linhas, caracteres, bytes de um arquivo.|
|```sed```|Editor de texto não interativo.|
|```awk```|Linguagem de programção, trabalha linha por linha em arquivos ou saida de comandos para buscar oque foi solicitado.|
|```nano```|Editor de texto.|
|```head```|Exibe as primeiras linhas de um arquivo.|
|```tail```|Exibe as ultimas linhas de um arquivo.|
|```strings```|Exeibe caracteres de um arquivo.|
|```grep```|Busca caracteres ou strings em diretórios e arquivos.|
|```grep -R```|Busca caracteres ou strings em diretórios e arquivos,recursivamente, hierarquicamente.|
|```locate```|Exibe path de um diretório ou arquivo.|
|```find```|Busca por arquvios em uma hierarquia de diretorios.|
|```echo```|Exibe uma menssagem na tela.|
|```echo $VARIAVEL```|Exibe uma variavel na tela.|
|```tar```|Compressor de arquivos.|
|```tar -czvp arquivo_a_ser_criado.tar /path/arquivo_a_ser_comprimido```|Compirme o arquivo.|
|```tar -xzvf arquivo.tar.gz```|Extrai o arquivo.|
|```gzip```|compressor de arquivos.|
|```gzip -d arquivo.gz```|Extrai arquivo.|
|```gzip -9 arquivo```|Comprime arquivo.|
|```chown <usuário> <arquivo>```|Altera o usuário que é dono do arquivo.|
|```chown :<grupo> <arquivo>```|Altera o grupo de usuários que são donos do arquivo. Este comando pode ser usado junto com o comando anterior.|

## Histórico

|Comando|Descrição|
|------|------|
|```history```|Exibe o histórico de comandos.|
|```Ctrl + r```|Inicia a busca interatica no histórico ou encontra a próxima ocorrência quando a busca interativa já foi iniciada.|
|```!n```|Executa o comando número 'n'.|
|```!!```|Repete o comando anterior.|
|```!<string>```|Repete o comando anterior que inicia com 'string'.|
|```dirs -p```|Exibe o histórico de diretórios visitados.|

## Permissões

|Comando|Descrição|
|------|------|
|```chmod xxx <arquivo or diretório>```|chmod altera as permissões do usuário, grupo ou todos para ler, escrever ou executar o arquivo.|
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
|```chmod 600 <arquivo>```|O dono do arquivo pode ler e escrever no mesmo.|

## Variedades

|Comando|Descrição|
|------|------|
|```diff -qr <diretório1> <diretório2>```|Exibe as diferenças entre os diretórios. Argumento ```-q``` exibe arquivo modificados ou não existentes. Argumento ```-r``` exibe a diferença entre o conteúdo dos arquivos.|
|```man <comando>```|Manual do comando.|
|```whoami```|Quem sou eu? Exibe seu usuário.|
|```whatis```|Exibe o que é um comando.|
|```date```|Exibe data e hora.|
|```ps```|Exibe informações sobre processos.|
|```ps -aux```|Exibe informações sobre processos, usuarios, tty.|
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


[permissions]: https://github.com/hemilioaraujo/Linux-Commands/blob/master/img/permissionsPT.PNG?raw=true
"String representation"
