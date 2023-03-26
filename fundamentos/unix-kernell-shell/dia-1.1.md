# Dia 1, seção 1, mod. 1 - Unix, Kernel e Shell

Nos anos 60 surge o Unix, desenvolvido por Ken Thompson e Dennis Ritchie utilizando linguagem de programação C;

Permitiu que vários usuários utilizassem o computador ao mesmo tempo sem que a atividade de um interfira no outro;

Permite que o usuário execute várias tarefas ao mesmo tempo;

Tem portabilidade: podendo ser adaptado para os mais diversos sistemas computacionais sem maiores dificuldades;

Atualmente diversos sistemas operacionais são baseados no Unix, entre eles o Linux e o Mac OS;

Kernel: responsável por fazer a ligação entre o hardware e o software;

Shell,  é a interface entre o sistema operacional (SO), o usuário e o núcleo, ou seja, entre o SO, você e o Kernel. Ele lê a linha de comando, interpreta seu significado, executar o comando e devolver o resultado para o usuário. Utiliza-se a interface gráfica (pasta de arquivo e etc) e a linha de comando (terminal). Existem vários tipo, os que eu mais utilizarei: bash e zsh;

Foram apresentados os comandos mais utilizados no dia a dia de programador, e suas funcionalidades, como ls, pwd, cd, mkdir e vários outros;

Além disso, foi possível aprender comandos de Inputs e Outputs.

## Exercício 1:

Utilizando o terminal, aplique o comando de criação de diretórios que você aprendeu: crie um diretório chamado unix_tests e navegue até ele.
mkdir unix_tests 
cd unix_tests

Crie um arquivo de texto com o nome trybe.txt.
touch trybe.txt

Crie uma cópia do arquivo trybe.txt com o nome trybe_backup.txt.
cp trybe.txt trybe_bakcup.txt

Renomeie o arquivo trybe.txt.
mv trybe.txt trybe1.txt

Dentro de unix_tests, crie um novo diretório chamado backup.
mkdir backup 

Mova o arquivo trybe_backup.txt para o diretório backup.
mv trybe_backup.txt /home/rafaela/unix_tests/backup

Dentro de unix_tests, crie um novo diretório chamado backup2.
mkdir backup2

Mova o arquivo trybe_backup.txt da pasta backup para a pasta backup2.
cd backup
mv trybe_backup.txt /home/rafaela/unix_tests/backup2

Apague a pasta backup.
cd ..
rmdir backup

Renomeie a pasta backup2 para backup.
mv bakcup2 backup

Apague o diretório backup.
rm -rf backup

Limpe o terminal.
clear

### Exercício 2:

Crie um novo diretório chamado unix_tests_search e navegue até ele.
mkdir unix_tests_search
cd unix_tests_search

Na pasta unix_tests_search, baixe um arquivo com os nomes de todos os países do mundo utilizando o comando curl. 
curl -o countries.txt "https://gist.githubusercontent.com/kalinchernev/486393efcca01623b18d/raw/daa24c9fea66afb7d68f8d69f0c4b8eeb9406e83/countries"

Mostre todo o conteúdo do arquivo countries.txt na tela.
cat countries.txt

Mostre o conteúdo de countries.txt, página por página, até encontrar a Zambia.
less countries.txt + espaço até encontrar Zambia 

Mostre novamente o conteúdo de countries.txt página por página, mas agora utilize um comando para buscar por Zambia.
less countries.txt 
/Zambia 

Busque por Brazil no countries.txt.
grep Brazil countries.txt

Busque novamente por brazil, mas agora utilize o lower case e não considere letras maiúsculas ou minúsculas.
grep -i countries.txt

Crie um novo arquivo chamado phrases.txt e adicione algumas frases à sua escolha.
touch phrases.txt 
cat >> phrases.txt 
Só sei que nada sei 
Vamos mudar o mundo!
JavaScript é uma linguagem de programação
Ctrl + d para sair 

Conte o número de palavras do arquivo phrases.txt.
wc -w phrases.txt

Conte o número de linhas do arquivo phrases.txt.
wc -l phrases.txt 

Liste todos os arquivos que terminem com txt.
find . -name “*.txt”

