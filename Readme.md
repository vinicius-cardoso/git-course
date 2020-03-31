# Aprendendo a usar Git e GitHub

- criar diretório: `mkdir`
- entrar no diretório: `cd <nomedodiretorio>`
- sair do diretório: `cd ..`
- exluir diretorio: `rm -rf <nomedodiretorio>`
- iniciar o git: `git init`
- criar/modificar arquivo (Vim): `vim <nomedoarquivo>`
- modo de inserção: `$ i`
- modo de comando: tecla esc
- salvar e sair (write e quit): `$ :wq`

# Ciclo de Vida dos Status dos Arquivos

- **Untracked** (nao marcado):
  arquivo adicionado no repositorio mas ainda nao visto pelo Git. 

- **Unmodified** (nao modificado):
  arquivo exite no Git mas ainda nao foi modificado

- **Modified** (modificado):
  arquivo modificado

- **Staged** (temporario):
  arquivo em versionamento

# Comandos básicos

- `git status`: reportar como esta o diretorio

- `git add <arquivo>`: torna o arquivo 'untracked' em 'unmodified' e 'modified' em 'staged'

- `git commit -m <"mensagem">`: adicionar alteraçoes no arquivo e uma mensagem<br>
  `git commit -am <"mensagem">`: mostra a ultima modificacao

- `git log`: ver as versoes e informacoes do arquivo<br>
  `git log --author="<nomedoautor>"`: mostra apenas alteracoes feitas pelo autor citado<br>
  `git log --graph`: mostra em forma grafica o que esta acontecendo com os branches e versoes

- `git shortlog`: mostra em ordem alfabetica, autores(quantidade de logs) e logs<br>
  `git shortlog -sn`: mostra so quantidade de commits e a pessoa

- `git show <hash>`: mostra adicoes (linhas) no arquivo

- `git diff`: mostra a ultima modificacao antes de commitar<br>
  `git diff --name-only`: mostra apenas os arquivos modificados

- `git checkout <nomedoarquivo>`: retorna o arquivo pra antes da ultima edicao<br> 
  `git checkout -b <nomedobranch>`: cria um branch<br>
  `git checkout <nomedobranch>`: muda para o branch citado

- `git branch`: mostra em qual branch voce esta<br>
  `git branch -D <nomedobranch>`: deleta o branch 

- `git reset Head <nomedoarquivo>`: remover o arquivo do stage<br>
  `git reset --soft <hasharquivoanterior>`: retirar a modificacao<br>
  `git reset --mixed <hasharquivoanterior>`: retirar o commit e voltar pra modified<br>
  `git reset --hard <hasharquivoanterior>`: resetar o commit totalmente

- `git remote add origin <git@github.com:vinicius-cardoso/nomedorepositorio.git>`: cria arquivos a partir de um repositorio existente (via SSH)<br>
  `git remote add origin <https://github.com/vinicius-cardoso/nomedorepositorio.git>`:cria arquivos a partir de um repositorio existente (via HTTPS)

- `git push -u origin master`: envia todos os arquivos para o repositorio determinado / origin: pra onde vai / master: de onde vem<br>
  `git push origin master --tags`: passa as tags pro arquivo no GitHub<br>
  `git push origin :<tag ou branch>`: deleta uma tag ou branch remoto

- `git clone <endereco>`: clona um repositorio 

- `git merge <nomedocommit>`: faz o merge

- `git rebase <nomedocommit>`: faz o rebase

- `git stash`: cria um arquivo para salvar modificacoes<br>
  `git stash apply`: aplica as mudancas guardadas<br>
  `git stash list`: mostra a lista de stashes<br>
  `git stash clear`: limpa a stash

- `git config --global alias.<atalho><comando>`: cria um atalho para um comando

- `git tag`: mostra as tags existentes<br>
  `git tag -a <versao> -m <comentario>`: cria uma tag da versao do arquivo<br>
  `git tag -d <versao>`: deleta a tag

- `git revert <hash>`: apaga as ultimas linhas mas nao apaga o commit 

# Conceitos

**Commit:** Alteracao em um arquivo

**Fork:** Copia um repositorio (e diferente de clone)

**Pull Request:** Avisa a pessoa a qual voce copiou o repositorio sobre mudancas que voce fez

**Branch:** E um ponteiro para alteracoes no arquivo 

**Merge:** Uniao de branches atraves da criacao de um novo commit para unir commits paralelos 

**Rebase:** Uniao de branches atraves da movimentacao de commits
