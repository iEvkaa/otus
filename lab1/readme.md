# Команды IOS. Базовая конфигурация устройств
## Топология
![](https://github.com/iEvkaa/otus/blob/main/lab1/images/lab1.png)
## Таблица адресации
![](https://github.com/iEvkaa/otus/blob/main/lab1/images/Lab1-2.png)
## Задачи
⦁	Отобразите конфигурацию устройства.
⦁	Протестируйте сквозное соединение, отправив эхо-запрос.
⦁	Протестируйте возможности удаленного управления с помощью Telnet.
## Решение
Подключим между собой коммутатор и пк с помощью консольного кабеля. Для этого соединим порт rs-232 (com port) с консольным портом коммутатора специальным кабелем.
Далее с пк через терминал подключимся к коммутатору и произведем его настройку.
Для начала зайдем на нужным нам интерфейс, в нашем случае это 0/6, и включим его.

Switch(config)#interface fa0/6
Switch(config-if)#no shutdown
Switch(config-if)#

Далее перейдем в интерфейс vlan 1, в котором зададим ему адрес и так же включим его.

Switch(config)#interface vlan 1
Switch(config-if)#ip address 192.168.1.2 255.255.255.0
Switch(config-if)#no shutdown

Так же настроим терминальные линии.

line VTY 0 5

![](https://github.com/iEvkaa/otus/blob/main/lab1/images/lab1-3.png)
