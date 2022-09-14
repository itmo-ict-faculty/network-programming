## Лабораторная работа №4 "Базовая 'коммутация' и туннелирование используя язык программирования P4"

### Описание
В данной лабораторной работе вы познакомитесь на практике с языком программирования P4, разработанный компанией Barefoot (ныне Intel) для организации процесса обработки сетевого трафика на скорости чипа. Barefoot разработал несколько FPGA чипов для обработки трафика которые были встроенны в некоторые модели коммутаторов Arista и Brocade.  

### Цель работы
Изучить синтаксис языка программирования P4 и выполнить 2 задания обучающих задания от Open network foundation для ознакомления на практике с P4.

### Правила по оформлению
Правила по оформлению отчета по лабораторной работе вы можете изучить по [ссылке](../reportdesign.md)

### Ход работы
Данную лабораторную работу рекомендуется начать с изучения [P416 Language Specification](https://p4.org/p4-spec/docs/P4-16-v1.2.3.pdf), этот документ поможет вам в первоначальном представлении о языке программирования P4.

Перед выполнением лабораторной работы вам необходимо выполнить следующие задачи:

> Желательно все делать на устройстве с архитектурой x86, [оригинальная инструкция](https://github.com/p4lang/tutorials/blob/master/README.md)  

- Склонировать репозиторий [p4lang/tutorials](https://github.com/p4lang/tutorials)
- Установить Vagrant и VirtualBox
- Перейти в папку `cd vm-ubuntu-20.04`
- Используя Vagrant развернуть тестовую среду `vagrant up`
- В результате установки у вас появится виртуальная машина с аккаунтами login/password `vagrant/vagrant` и `p4/p4`


>*Note*: Before running the `vagrant up` command, make sure you have enabled virtualization in your environment; otherwise you may get a "VT-x is disabled in the BIOS for both all CPU modes" error. Check [this](https://stackoverflow.com/questions/33304393/vt-x-is-disabled-in-the-bios-for-both-all-cpu-modes-verr-vmx-msr-all-vmx-disabl) for enabling it in virtualbox and/or BIOS for different system configurations.

Первой частью лабораторной работы является задание [Implementing Basic Forwarding](https://github.com/p4lang/tutorials/tree/master/exercises/basic).
В нем необходимо выполнить следующие задачи:
- В виртуальной машине перейдите в папку проекта и выполните задания описанные в [Implementing Basic Forwarding](https://github.com/p4lang/tutorials/tree/master/exercises/basic)
- Зафиксируете результаты и укажите результаты в вашем отчете

Второй частью лабораторной работы является задание [Implementing Basic Tunneling](https://github.com/p4lang/tutorials/tree/master/exercises/basic_tunnel)
В нем необходимо выполнить следующие задачи:
- В виртуальной машине перейдите в папку проекта и выполните задания описанные в [Implementing Basic Tunneling](https://github.com/p4lang/tutorials/tree/master/exercises/basic_tunnel)
- Зафиксируете результаты и укажите результаты в вашем отчете

### Результаты лабораторной работы
В результате данной работы у вас должно быть:
- 2 файла с исправленным программным кодом с расширением `.p4`.
- Схема связи нарисованная вами в [draw.io](https://app.diagrams.net) или Visio.
- Результаты пингов, проверки локальной связности.