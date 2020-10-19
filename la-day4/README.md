## Coringas

### Notas

* ?: qualquer caracttere na posição
* [a-z]\: determina range de caracteres aceitável
  * utilizar "^" nega os caracteres listados (ex: m[^a-b] - procura por arquivos que começam com m sem ser seguido por a e b)
* {a-z}\: procura por segmentos (ex: x{zd,ze,zm})

## Comandos Diversos

### Notas

* inode
  * Cada diretório e arquivo é identificado no kernel como um número de nó i (inode). 
  * Um inode é, na realidade, uma estrutura de dados que possui informações sobre um determinado arquivo ou diretório como, por exemplo, dono, grupo, tipo e permissões de acesso.
  * O inode é exclusivo somente para o dispositivo (partição) dentro do qual ele está contido. Portanto, para identificar um arquivo, o kernel deve ter o número de dispositivo e o inode do arquivo.
  * Um arquivo possui um único inode, não importa por quantos nomes este arquivo é identificado no sistema. Logo, é o conjunto de inodes que indica o número de arquivos/diretórios que o sistema possui.

### Comandos notaveis

* id - print real and effective user and group IDs
* df - report file system disk space usage
* ln - make links between files
  * -s, --symbolic: make symbolic links instead of hard links
* du - estimate file space usage
  * --inodes: list inode usage information instead of block usage
* find - search for files in a directory hierarchy
  * -maxdepth levels: Descend at most levels (a non-negative integer) levels of directories below the starting-points.  -maxdepth 0 means only  apply the tests and actions to the starting-points themselves.
  * -type: File is of type
    * b: block (buffered) special
    * c: character (unbuffered) special
    * d: directory
    * p: named pipe (FIFO)
    * f: regular file
    * l: symbolic link; this is never true if the -L option or the -follow  option is in effect, unless the symbolic link is broken.  If you want to search for symbolic links when -L is in effect, use -xtype.
    * s: socket
    * D: door (Solaris) To  search  for  more  than one type at once, you can supply the combined list of type letters separated by a comma `,' (GNU  ex‐ tension).
  * -mtime n: File's data was last modified n*24 hours ago.  See the comments for -atime to understand how rounding affects the interpretation of file modification times. (ex: find -mtime -1 - for files modified less than 1 day ago / find -mtime +1 for files modified more than 1 day ago)
  * -mmin: same as mtime but for minutes
    * **use prefix: -a -c -m for time and min, to change from acessed (-a), modified (-m), created (-c)**
  * -user / -uid / -gid / -group: to find based on owner
  * -mount: to search only for files on mounted file systems
  * -size: filter by size
* grep, egrep, fgrep, rgrep - print lines that match patterns
  * -v, --invert-match: Invert the sense of matching, to select non-matching lines.
  * -f FILE, --file=FILE: Obtain patterns from FILE, one per line.  If this option is used multiple  times  or  is  combined with the -e (--regexp) option, search for all patterns given.  The  empty  file  contains  zero patterns, and therefore matches nothing.
  * -r, --recursive: Read  all  files  under  each  directory, recursively, following symbolic links only if they are on the command line.  Note  that if no  file  operand  is  given,  grep  searches  the  working directory.  This is equivalent to the -d recurse option.
  * tip: study 'man grep'
* nl - number lines of files
  * study 'man nl'
* sort: - sort lines of text files
  * -r, --reverse: reverse the result of comparisons
  * -c, --check, --check=diagnose-first: check for sorted input; do not sort
  * check 'man sort' for more sorting options
* head - output the first part of files
* tail - output the last part of files
* time - run programs and summarize system resource usage
* dmesg - print or control the kernel ring buffer
* sync - Synchronize cached writes to persistent storage
