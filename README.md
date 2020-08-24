# Reverse-Shell-TTY-Cheat-Sheet
Simple TTY cheat sheet for shell stabilization

- Python
- Perl
- Linux OS 
- Ruby
- Lua

# TTY Shells

```
python -c 'import pty; pty.spawn("/bin/bash")'
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

python -c 'import pty; pty.spawn("/bin/bash")'
Control Z

Attacker 

stty raw -echo
fg
ENTER
ENTER
export TERM=xterm
```
