## Comandos Internos e Externos Shell

### Notas

* Comandos internos tem mais performance que comandos externos
* No caso do comando estar presente tanto internamente quanto externamente, o comando interno sempre terá prioridade
  * Execução builtin antes de procurar no $PATH
* Para identificar quais comandos são internos ou internos:
  * which "nomedocomando"
  * man builtins
  * comando type dá a resposta objetiva a essa pergunta
* **POSIX**
  * Set minimo de instruções para executar no sistema, padrão universal
* Cenário comum de ataque é inserção de comandos alterados no $PATH

## Comandos de Manipulação de Diretórios

### Notas

* arquivos com "~" no fim, são, de acordo com a convenção adotada, arquivos de backup

### Comandos notáveis

* Comando "ls" aceita mais de um argumento (ex: diretórios diferentes: ls pasta1 pasta2)
  * drwxr-xr-x | 2 | karlcf | karlcf | 4.0K  | Sep 11 19:58 .
  * Permissões | Contador de pastas dentro do diretório, valor = 1 se for arquivo  | Dono | Grupo | Tamanho | Data da ultima modificação 
  * -f classifica por ordem de ultima alteração
  * Importante: estudar "man ls"
  * ls -latr 
* Comando mkdir
  * mkdir -p: para criar a estrutura de diretórios de uma só vez (ex: mkdir -p dir1/dir2/dir3)

## Comandos de manipulaçao de Arquivos

### NOTAS



### Comandos Notáveis

* cat: exibir conteudo do arquivo
  * -n: exibir número da linha
  * -s: ocultar linhas em branco repetidas
  * zcat / bzcat / xzcat : arquivos comprimidos
* tac : exibir conteudo do arquivo em ordem reversa
* cp -u: somente altera caso origem esteja mais atualizada que destino

