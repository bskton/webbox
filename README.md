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
~$ git clone https://github.com/bskton/webbox.git
```

Перейти в директорию webbox
```bash
~$ cd webbox
```

Собрать бокс с помощью packer
```bash
~/webbox$ packer build packer.json
```

Добавить бокс в список для Vagrant
```bash
~/webbox$ vagrant box add build/webbox-virtualbox-iso.box --name web
```

После этого можно можно инициализировать и запустить виртуальную машину под управление Vagrant на основе бокса webbox с помощью команд
```bash
~/vms/web-1$ vagrant init web
~/vms/web-1$ vagrant up --provider virtualbox
```