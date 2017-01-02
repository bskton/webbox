# Vagrant бокс для веб-разработки
Шаблон для сборки бокса Vagrant, который можно использоваться для работы над веб-проектами.
## Системные требования
 * Ubuntu 16.04 64-bit
 * Packer 0.12.1
 * VirtualBox 5.1.12
 * Vagrant 1.8.6
 * Git 2.7.4
## Использование
Склонировать репозиторий на свой комьютер
```bash
~$ git clone https://github.com/bskton/webdev.git
```
Перейти в директорию webdev
```bash
~$ cd webdev
```
Собрать бокс с помощью packer
```bash
~/webdev$ packer build packer.json
```
Добавить бокс в список для Vagrant
```bash
~/webdev$ vagrant box add build/webdev-virtualbox-iso.box --name webdev
```
После этого можно можно инициализировать и запустить виртуальную машину под управление Vagrant на основе бокса webdev с помощью команд
```bash
~/vms/webdev-1$ vagrant init webdev
~/vms/webdev-1$ vagrant up
```