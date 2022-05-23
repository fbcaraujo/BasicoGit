### Conceitos:
Repositórios => repositórios = Pastas = Projetos = Arquivos versionados.

Branch => Ramificações da linha principal (Main) das versões, podem ter várias ramificações, uma cada nova funcionalidade atribuída, também para um projeto com várias pessoas, e no qual vão testando as opções, definindo podem passar a principal. Branch Master ou mais atual Branch Main, é o que cria o tempo cronológico principal.

Commit => salvar as alterações feitas no projeto (arquivo) e postar para o Github.

Merge => fusão da Branch com a linha principal (Main), ou seja, trazer a versão ideal de um código, testada na Branch (linha alternativa), para a Main. Pode fazer Merge com outras Branch. Atentar para a junção de versões quando dois ou mais usuários estiverem usando a mesma linha de código e  a junção entrar em conflito.

Remote => comando para passar a referência do repositório local para o repositório remoto, e com isso executar os Commit.

Push => primeiro se realiza o Commit no repositório local para salvar e depois com o Push empurra a alteração para o repositório remoto.

Pull => ocorre quando é necessário puxar as alterações realizadas por outros membros no repositório remoto após executarem o Commit e o Push.

README.md arquivo com extensão de Markdown para gerar informações fora das linhas de código, em geral é uma instrução de como proceder com os códigos e informações gerais.

### Comandos:
git --version
versão

git init
iniciar repositório corrente, somente na primeira vez

git add "arquivo"
enviar do repositório local para a área de staging arquivos especificos

git add .
enviar do repositório local para a área de staging todos os arquivos

git status
informa situação dos arquivos na área de staging

git commit -m "descrição commit"
salvar as alterações do arquivo no repositório local do Git

git reset
desfaz um commit

git branch -M "main"
modifica nome da Branch Master para Branch Main

git remote add origin https://github.com/brunodsh/BasicoGit.git
vincular o repositório local com o remoto

git push -u origin main
enviar alterações do repositório atual para o remoto

git checkout -b "modelar"
criar uma nova branch / ramificação no repositório atual

git checkout main / modelar
parecido com o comando CD para mudar de repositório, nesse caso mudando de branch

git clone https://github.com/rafaballerini/GitTutorial.git
clonar repositório de outro usuário

git pull (dentro do diretório clonado)
atualizar as alterações realizadas no diretório clonado

### Comandos rápidos:
git add "arquivo"

git status

git commit -m "descrição commit"

git push -u origin main

### Comandos concatenando:
git add "arquivo" && git status && git commit -m "descrição commit" && git push -u origin main

### Commit branch secundária:
git checkout modelar

git add aprendendoGit.md

git status

git commit -m "descrição do commit"

git push origin modelar

### Merge da branch secundária para a main:
git checkout main

git merge modelar

git push origin main

### Clonar repositório de outro usuário git:
git clone https://github.com/rafaballerini/GitTutorial.git

### Atualizar repositório clonado de outro usuário git:
git pull

### Observações:
1. O parâmetro -u depois do "git push" só é necessário quando executar a primeira vez de um arquivo
2. O clone de repositório foi realizado no git da rafaballerini
3. Após um fork de um repositório de outro usuário, é possível sugerir alteração, com o pull request
4. 