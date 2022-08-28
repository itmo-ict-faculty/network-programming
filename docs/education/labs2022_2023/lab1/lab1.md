<p align="center"><font size = 6><strong> Лабораторная работ №1 "Установка CHR и Ansible, настройка VPN"</strong></font></p>

<p align="center"><font size = 5><strong>Описание</strong></font></p>

Данная работа предусматривает обучение развертыванию виртуальных машин (VM) и вспомогательных средств для работы с частными сетями.

<p align="center"><font size = 5><strong>Цель работы</strong></font></p>

Целью данной работы является развертывание виртуальной машины с помощью Microsoft Azure и последующая настройка дополнительных средств для работы с сетями.

<p align="center"><font size = 5><strong>Правила по оформлению</strong></font></p>

Правила по оформлению отчета по лабораторной работе вы можете изучить по [ссылке](../reportdesign.md)

<p align="center"><font size = 5><strong>Ход работы</strong></font></p>

1. Необходимо развернуть вертуальную машину с помощью Microsoft Azure;
2. В бесплатном режиме Microsoft Azure предлагает только Ubuntu 16.4 поэтому необходимо обновит пакеты виртуальной машины. Сделать это можно с помощью данных команд:
   `sudo apt update & sudo apt ugprade` ;

3. Запустим обновление до последней версии Ubuntu:
   `sudo do-release-upgrade` ;

4. Теперь мы подготовим Ansible и запустим зависимости для python3:
   `sudo apt install python3-pip`
   `ls -la /usr/bin/python3.6`
   `sudo pip3 install ansible`
   `ansible --version` ;

5. После этого мы сделаем свой Wireguard/OpenVPN/L2TP сервер для организации VPN туннеля между вашим сервером автоматизации и вашим локальным CHR;
Что искать? (Wireguard/OpenVPN/L2TP сервер для Ubuntu 18) ЛЮБОЙ НА ВЫБОР
6. После этого необходимо на вашем компьютере установить VirtualBox а на него CHR (RouterOS) Что искать? (CHR на VirtualBox);
7. После этого вам надо поднять VPN туннель между вашим VPN сервером на Ubuntu 18 и VPN клиентом на RouterOS (CHR) Что искать? («Название вашего протокола» клиент RouterOS).

У вас должна получиться схема следующего вида:

![Схема](Scheme.jpg)

В итоге до CHR должны проходить пинги.