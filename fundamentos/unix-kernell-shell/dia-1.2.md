# Dia 2, seção 1, mod. 1 - Git

O git funciona como uma linha do tempo na qual você pode criar vários pontos de acesso para as alterações realizadas em um projeto e acessá-las quando necessário;

O versionamento com o git consiste em três passos: ramificação (branch), captura de mudanças (commit) e mesclagem (merge);

A ramificação funciona como os ramos do seu projeto, ou seja, o seu projeto principal fica na branch main;

Você consegue criar outros ramos (outras branchs) que tem uma versão do projeto principal na qual você pode realizar modificações sem tanta cautela, pois suas ações não interferem na branch principal;

O projeto principal é aquele que fica na main. É essa branch que vai para a produção, ou seja, que será acessada pelas pessoas usuárias;

Após cada alteração é importante informar ao Git que deve adicionar essas alterações em um commit, isto é, uma mensagem com o que você alterou no projeto;

Na mesclagem você precisa atualizar sua branch com a main ou atualizar a main suas alterações. Esse processo é chamado de merge, ou seja, ele mescla as alterações;

Um repositório é uma pasta do seu computador na qual você pode armazenar arquivos, projetos e etc.;

Nessa pasta você pode criar versões, as branches;

Pode ser feito pelo terminal;

Repositório local: repositório do seu computador. Pode ser baixado ou criado por você;

Repositório remoto: pode ser acessado via internet. Em uma plataforma de hospedagem de código, como o GitHub;

Para encerrar foram apresentados comandos mais utilizados do git init ao git merge como o git status, git add e entre outros.

## Exercício 1

Crie uma pasta em seu computador;
mkdir git-test

Acesse a pasta que você acabou de criar;
cd git-test

Inicie o versionamento por meio do comando git init;
git init dentro da pasta que acabei de criar (git-test)

Abra a pasta no VS Code por meio do comando code .;
code . (já está habilitada a opção de abrir o VS Code automático)

Crie um arquivo chamado README.md;
touch README.md 

Adicione o arquivo novo em staging e realize um commit, como em git add . e git commit -m "Descreva a alteração realizada";
git add .
git commit -m "Meu primeiro commit"

Crie uma nova branch por meio do comando git checkout -b, como em git checkout -b adiciona-readme;
git checkout -b adiciona-readme

Faça uma alteração em README.md e, depois, realize um novo commit, como em git add . e git commit -m "Alterando o README";
Dentro de README.md eu acrescentei a frase: "Estou aprendendo a fazer repositórios, commitar e realizar o merge."
git status (para ver se houve modificação)
git add .
git commit -m "Alterando o README"

Retorne para a branch main e, em seguida, realize o merge das alterações por meio do comando git merge nome-da-branch, como em git merge adiciona-readme.
git checkout main 
git branch (para verificar se estou na branch main)
git merge atualiza-readme

### Exercício 2

Acesse a branch main e crie uma branch nova chamada atualiza-readme.
git checkout -b atualiza-readme

Acesse a branch atualiza-readme e crie um arquivo chamado infos.txt.
touch infos.txt

Adicione as alterações em staging e realize um commit.
git add .
git commit -m "Atualizações"

Adicione seu nome e sobrenome ao arquivo infos.txt.
cat >> infos.txt
Rafaela Pinto
Ctrl + d

Adicione novamente as alterações em staging e realize um commit.
git add .
git commit -m "Atualiza infos"

Crie uma branch nova a partir da branch atualiza-readme. A nova branch deve se chamar adiciona-infos.
git checkout -b adiciona-infos

Acesse a branch adiciona-infos e utilize sua criatividade para escrever o passo a passo de como o versionamento funciona no README.md. 
Fiz esse processo editando no VS Code.

Adicione as alterações em staging e realize o commit.
git add .
git commit -m "Detalhando passo-a-passo"

Volte para a branch atualiza-readme e realize o merge das alterações feitas na branch adiciona-infos.
git checkout atualiza-readme
git merge adiciona-infos

Retorne para a branch main e realize o merge das alterações.
git checkout main 
git merge atualiza-readme 

