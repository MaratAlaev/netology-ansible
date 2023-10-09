# Установка ClichHouse 

## Версии

08-ansible-02-playbook основная версия

## Запуск плейбука

Переходим в директорию playbook 
и выполянем запуск

Пример команды 
bash'''
ansible-playbook -i ./inventory/prod.yml --ask-become-pass  site.yml
'''

### Требования

- **Ansible 2.12+**

### Описание действий

Таски:

Get clickhouse distrib - скачивает пакеты rpm для ClichHouse
в случае того если пакет clickhouse-common-static версии noarch не будет найден
скачается версия x86_64  

Install clickhouse packages - устанавливает пакеты ClichHouse

Create database - создает базу данных, после рестарта сервиса ClichHouse
и проверяет вернувшийся код ответа 

Get Vector distrib - скачивание архива с Vector

Create Vector directory - создание директории в которую будет установлен Vector

Unarchive vector shell - разархивирование выполняетя с помощью команды в shell 
так как модуль unarchive не может разархивировать файл

Move bin file - установка бинарника

Move systemctl - установка сервиса

Edit config - замена конфиг файла Vector 
на шаболн из директории templates

Хендлеры:

Start clickhouse service - рестарт сервиса ClichHouse
Start vector - перезапус сервиса vector 