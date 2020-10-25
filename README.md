# Reverse-Shell-TTY-Cheat-Sheet
Simple TTY cheat sheet for shell stabilization
Prevents you from killing your reverse shells and adds proper shell functionality

- Python
- Script
- Perl
- Linux OS 
- Ruby
- Lua

# TTY Shells

```
python -c 'import pty; pty.spawn("/bin/bash")'
/usr/bin/script -qc /bin/bash /dev/null
perl —e 'exec "/bin/sh";'
perl: exec "/bin/sh";
echo os.system('/bin/bash')
/bin/sh -i
ruby: exec "/bin/sh"
lua: os.execute('/bin/sh')

```
# TTY Shell Stabilization Process

```
Victim

python -c 'import pty; pty.spawn("/bin/bash")' OR /usr/bin/script -qc /bin/bash /dev/null
Control Z

Attacker 

stty raw -echo
fg
ENTER
ENTER

Victim

export TERM=xterm
stty cols 132 rows 34
```
