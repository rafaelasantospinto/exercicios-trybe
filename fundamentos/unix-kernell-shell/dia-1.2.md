# Dia 2, seção 1, mod. 1 - Git

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

