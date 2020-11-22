## Permissions on Linux

### Notes

        -         ||           rw-          ||           r--           ||         r--
                  ||           420          ||           420           ||         400
                  ||            6           ||            6            ||          4 
tipo do arquivo   ||   permissoes do dono   ||    permissoes do grupo  ||        outros

Tipo de arquivo                             
- - Arquivo de texto
l - Link simbolico
b - Dipositivo de Bloco
c-  Dispositivo de Caractere
s-  Socket
d - Diretorio

Permissões (Letra)            || Octal           || QUEM?
- - Ausencia de permissao     ||  0              || u => dono do arq
r - Permissao de leitura      ||  4              || g => grupo dono
w - Permissao de escrita      ||  2              || o => outros
x - Permissao de execução     ||  1              || a => all
t - stick bit                 ||  1(prefix)
S - SGID                      ||  2(prefix)
S - SUID                      ||  4(prefix)

---

* SUID and SGID enables whoever runs and/or uses the files to run them as the owners
* Extra reading:
  * https://www.thegeekstuff.com/2013/02/sticky-bit/

---

### Notable Commands

* umask - set file mode creation mask
* chmod - change file mode bits
  * Important: -R, --recursive change files and directories recursively
* chown - change file owner and group
* chgrp - change group ownership
