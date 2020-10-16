## Comandos para lembrar

* su - 
  * Assume usuário, com "-" o root, com todas as caracteristicas do mesmo
* cat /etc/shells
  * Para checar os shells disponíveis 
* df -h
  * mostrar partições
* half: desligar máquina 


### Notas

* LSB: Linux Standard Base
* Diretório home do usuário root: /root
* cat /etc/shells
  * Diretório onde os shells disponíveis ficam salvos
* cd -
  * Retorna ao diretório anterior
* Diretórios vs arquivos
  * "d" no inicio das permissões do arquivo/diretório (ex: drwxr-xr-x)
  * "-" significa arquivo comum de texto
  * "l" link simbolico (pense em atalho)
  * "b" dispositivo de bloco, armazenamento de info
  * "c" dispositivo de caractere, transferencia de info
* sda(a,b,c,d,...): SCSI(Small Computer System Interface) disk A
* sda1~4: partições primárias
* sda5~9: partições lógicas
* /opt: Pacotes estático de aplicações - Pòuco utilizado ultimamente
* /proc: infos virtuais dinamicas do kernel e processos
* tmpfs: temporary file system
*  /srv: arquivos estáticos (ex: paginas web do apache)
   * Srv is a serve folder. It holds site specific data to be served by the system for protocols such as, ftp, rsync, www, cvs etc. To be compliant distributions include this folder but I have not seen it used much.
* /var/run: depreciado, agora é mais utilizado /run, mudança recente
* /var/tmp: arquivos "não tão temporarios", são preservados em reboot

## FHS

Significados dos diretórios (extraido de https://pt.wikipedia.org/wiki/Filesystem_Hierarchy_Standard):

Material auxiliar: https://www.nixtutor.com/linux/understanding-the-linux-directory-layout/

* /bin - Binários de usuários, essenciais no boot
* /sbin - Binários do superusuário, essenciais no boot
* /boot - Arquivo do gerenciador de partida e kernel, símbolos
* /dev - Dispositivos do sistema
* /etc - Arquivos de configuração globais
  *  /etc/opt - Arquivos de configuração para aplicativos em /opt
  *  /etc/X11 - Arquivos de configuração para o X Window System 11
* /home - Armazenamento de dados de contas de usuários normais
* /root - Armazenamento de dados de contas do superusuário
* /lib - Bibliotecas essenciais do sistema, de binários localizados em /bin e /sbin
* /mnt - Sistema de arquivos montado temporariamente
* /media - Ponto de montagem de mídias removíveis (como pen-drives, cd-rom)
* /opt - Pacotes estático de aplicações
* /proc - systema de arquivos virtual, onde pode fazer a interação com o kernel e processos do sistema
* /tmp - Arquivos temporários. Conteúdo geralmente apagado no reboot nas distribuições
* /usr - (unix system resources) - Hierarquia secundária (não essenciais no boot) para dados compartilhados de usuários
  *   /usr/bin - O mesmo que a hierarquia /bin, mas contém binários não essenciais ao
  *   funcionamento da máquina ou para o recovery
  *   /usr/include - Diretório padrãod para headers
  *   /usr/lib - O mesmo que a hierarquia /lib, mas não essenciais ao boot
  *   /usr/sbin - O emsmo que o /sbin, mas não essenciais ao boot da máquina
  *   /usr/share - Dados compartilhados independentes de arquitetura
  *   /usr/src - Armazenamento de código fonte da máquina
  *   /usr/X11R6 - - X Window Sysem, versão 11R6
  *   /usr/local - Armazenamento de binários não distribuidos na instalação principal da máquina, ou seja, fora do sistema de empacotamento. Também é o local de armazenamento terciário de dados
* /var - Arquivos que são gravados comf requencia (logs, páginas web, email, imagens, etc)
  *   /var/lock - Arquivos de lock, usados para controlar corretamente os recursos em uso
  *   /var/log - Arquivos de log, usado para logs em geral
  *   /var/mail - Caixas de e-mail dos usuários do sistema em formato mailbox
  *   /var/run - Contém dados sobre a execução do sistema desde seu primeiro boot (daemons e usuários)
  *   /var/spool - Spooling de tarefas (fila de impressão, cache de pacotes, proxy, etc)
  *   /var/spool/mail - Antigo local da caixa de correio de usuários (deve ser usado /var/mail)
  *   /var/tmp - Arquivos temporários. Quando usado em modo multi-usuário.