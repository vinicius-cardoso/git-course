Apendendo a usar Git e GitHub

.............................................................................................

- criar diretorio: "mkdir"
- entrar no diretorio: "cd 'nomedodiretorio'"
- iniciar o git: "git init"
- criar/modficar arquivo (Vim): vim 'nomedoarquivo'
- modo de insercao: "i"
- modo de comando: tecla esc
- salvar e sair: ":wq" (write e quit)

.............................................................................................

Ciclo de Vida dos Status dos Arquivos:

- Untracked (nao marcado):
arquivo adicionado no repositorio mas ainda nao visto pelo Git. 

- Unmodified (nao modificado):
arquivo exite no Git mas ainda nao foi modificado

- Modified (modificado):
arquivo modificado

- Staged (temporario):
arquivo em versionamento

.............................................................................................

- git status: reportar como esta o diretorio

- git add 'arquivo': torna o arquivo 'untracked' em 'unmodified' e 'modified' em 'staged'

- git commit -m "'mensagem'": adicionar alteraçoes no arquivo e uma mensagem
-- git commit -am "'mensagem'": mostra a ultima modificacao

- git log: ver as versoes e informacoes do arquivo
-- git log --author="'nomedoautor'": mostra apenas alteracoes feitas pelo autor citado
-- git log --ref: mostra em forma grafica o que esta acontecendo com os branches e versoes

- git shortlog: mostra em ordem alfabetica, autores(quantidade de logs) e logs
-- git shortlog -sn: mostra so quantidade de commits e a pessoa

- git show 'hash': mostra adicoes (linhas) no arquivo

- git diff: mostra a ultima modificacao antes de commitar
-- git diff --name-only: mostra apenas os arquivos modificados

- git checkout 'nomedoarquivo': retorna o arquivo pra antes da ultima edicao 

- git reset Head 'nomedoarquivo': remover o arquivo do stage
-- git reset --soft 'hasharquivoanterior': retirar a modificacao
-- git reset --mixed 'hasharquivoanterior': retirar o commit e voltar pra modified
-- git reset --hard 'hasharquivoanterior': resetar o commit totalmente

- git remote add origin 'git@github.com:vinicius-cardoso/nomedorepositorio.git': cria arquivos a partir de um repositorio existente (via SSH)

- git push -u origin master: envia todos os arquivos para o repositorio determinado / origin: pra onde vai / master: de onde vem

-

