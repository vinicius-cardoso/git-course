# Aprendendo a usar Git e GitHub

- criar diretório: `mkdir`
- entrar no diretório: `cd <nomedodiretorio>`
- sair do diretório: `cd ..`
- exluir diretório: `rm -rf <nomedodiretorio>`
- iniciar o git: `git init`
- criar/modificar arquivo (Vim): `vim <nomedoarquivo>`
- modo de inserção: `$ i`
- modo de comando: tecla esc
- salvar e sair (write e quit): `$ :wq`

# Ciclo de Vida dos Status dos Arquivos

- **Untracked** (não marcado):
  arquivo adicionado no repositório mas ainda não visto pelo Git. 

- **Unmodified** (não modificado):
  arquivo exite no Git mas ainda não foi modificado

- **Modified** (modificado):
  arquivo modificado

- **Staged** (temporario):
  arquivo em versionamento

# Comandos básicos

- `git status`: reportar como esta o diretorio

- `git add <arquivo>`: torna o arquivo 'untracked' em 'unmodified' e 'modified' em 'staged'

- `git commit -m <"mensagem">`: adicionar alteraçoes no arquivo e uma mensagem<br>
  `git commit -am <"mensagem">`: mostra a última modificacao

- `git log`: ver as versões e informações do arquivo<br>
  `git log --author="<nomedoautor>"`: mostra apenas alterações feitas pelo autor citado<br>
  `git log --graph`: mostra em forma gráfica o que esta acontecendo com os branches e versões

- `git shortlog`: mostra em ordem alfabética, autores (quantidade de logs) e logs<br>
  `git shortlog -sn`: mostra só quantidade de commits e a pessoa

- `git show <hash>`: mostra adições (linhas) no arquivo

- `git diff`: mostra a última modificacao antes de commitar<br>
  `git diff --name-only`: mostra apenas os arquivos modificados

- `git checkout <nomedoarquivo>`: retorna o arquivo pra antes da última edição<br> 
  `git checkout -b <nomedobranch>`: cria um branch<br>
  `git checkout <nomedobranch>`: muda para o branch citado

- `git branch`: mostra em qual branch você esta<br>
  `git branch -D <nomedobranch>`: deleta o branch 

- `git reset Head <nomedoarquivo>`: remover o arquivo do stage<br>
  `git reset --soft <hasharquivoanterior>`: retirar a modificação<br>
  `git reset --mixed <hasharquivoanterior>`: retirar o commit e voltar pra modified<br>
  `git reset --hard <hasharquivoanterior>`: resetar o commit totalmente

- `git remote add origin <git@github.com:vinicius-cardoso/nomedorepositorio.git>`: cria arquivos a partir de um repositório existente (via SSH)<br>
  `git remote add origin <https://github.com/vinicius-cardoso/nomedorepositorio.git>`: cria arquivos a partir de um repositório existente (via HTTPS)

- `git push -u origin master`: envia todos os arquivos para o repositório determinado / origin: pra onde vai / master: de onde vem<br>
  `git push origin master --tags`: passa as tags pro arquivo no GitHub<br>
  `git push origin :<tag ou branch>`: deleta uma tag ou branch remoto

- `git clone <endereco>`: clona um repositório 

- `git merge <nomedocommit>`: faz o merge

- `git rebase <nomedocommit>`: faz o rebase

- `git stash`: cria um arquivo para salvar modificações<br>
  `git stash apply`: aplica as mudanças guardadas<br>
  `git stash list`: mostra a lista de stashes<br>
  `git stash clear`: limpa a stash

- `git config --global alias.<atalho><comando>`: cria um atalho para um comando

- `git tag`: mostra as tags existentes<br>
  `git tag -a <versao> -m <comentario>`: cria uma tag da versao do arquivo<br>
  `git tag -d <versao>`: deleta a tag

- `git revert <hash>`: apaga as últimas linhas mas não apaga o commit 

# Conceitos

**Commit:** Alteração em um arquivo

**Fork:** Copia um repositório e cria uma conexão com o repositorio original

**Pull Request:** Avisa a pessoa a qual você copiou o repositório sobre mudanças que você fez

**Branch:** E um ponteiro para alterações no arquivo 

**Merge:** União de branches através da criação de um novo commit para unir commits paralelos 

**Rebase:** União de branches através da movimentação de commits
