## Gerenciamento e Execução de Processos

### Notas

* It's a best practice to use "/bin/su -" instead of just "su"
* "&" on the end of a command runs it in the background
* to stop bg commands, use the "kill %z[job id]" command
* use a ";" to execute commands on a sequential manner, on the same lane (e.g.: sleep 2 ; echo "hello world " ; sleep 2 ; echo "goodbye cruel world")

### Comandos Notaveis

* ps - report a snapshot of the current processes.
  * One of the core commands to use linux and manage processes, study this
  * Check the states available on man page
* jobs - lists commands running in the background
* bg [job id] - continues a suspended job on background
* fg - brings a background job on 
* pidof -- find the process ID of a running program.
* pstree - display a tree of processes
* kill - send a signal to a process
* pgrep,  pkill - look up or signal processes based on name and other attributes
* killall - kill processes by name
* killall5 -- send a signal to all processes.
* nohup - run a command immune to hangups, with output to a non-tty
* top - display Linux processes
  * should be studied and revised
* nice - run a program with modified scheduling priority
  * should be studied and revised
* renice - alter priority of running processes
* tload - graphic representation of system load average
* vmstat - Report virtual memory statistics

## Multiplexador de terminais

### Notas 

* On this class, the "screen" and "tmux" tools were approached
  * Use cases: detach the "screen" on which there's a job running which can't be interrupted (by remote connections dropping and such) and it becomes safer. 

### Dificuldades

* Review patch and diff

