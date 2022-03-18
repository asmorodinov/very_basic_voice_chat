# very_basic_voice_chat

## Запуск клиента:

Ubuntu (python3):
```
sudo apt-get update && sudo apt-get install -y portaudio19-dev python3-pyaudio gcc
pip3 install -r requirements.txt
python3 client-tcp.py
Enter IP address of server --> localhost (пример)
Enter target port of server --> 8888 (пример)
```

## Запуск сервера:
Docker:
```
docker run -p 8888:5000 -i asmorodinov/basic_voice_chat 
Enter port number to run on --> 5000
```
Docker (альтернативный вариант):
```
docker build .
docker run -p 8888:5000 -i <ID только что собранного контейнера>
```
Ubuntu (python3):
```
sudo apt-get update && sudo apt-get install -y portaudio19-dev python3-pyaudio gcc
pip3 install -r requirements.txt
python3 server-tcp.py
Enter port number to run on --> 5000
```

## Функционал
Клиенты могут подключаться/отключаться/переподключаться к серверу, заходить в комнаты и выходить из них, отключать/включать микрофон, задавать логин.

Сервер организует передачу данных между клиентами (клиенты общаются только с сервером, по TCP)

## References
Основано на
https://github.com/domage/soa-curriculum/tree/main/examples/sockets-voice-chat

Которое основано на
https://github.com/TomPrograms/Python-Voice-Chat
