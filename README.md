#  Использование Ansible

## Версии

08-ansible-03-playbook основная версия

## Запуск плейбука

Переходим в директорию playbook 
и выполянем запуск

Пример команды 
```bash
ansible-playbook -i ./inventory/prod.yml site.yml
```

### Требования

- **Ansible 2.12+**

### Описание действий

Таски:

Get clickhouse distrib - скачивает пакеты deb для ClichHouse
в случае того если пакет clickhouse-common-static версии noarch не будет найден
скачается версия x86_64  

Install clickhouse packages - устанавливает пакеты ClichHouse

Replace line - убирает комментарий со строки отвечающий за прослушивание хостов
делается для того чтобы получить доступ к clickhouse извне 

Create database - создает базу данных, после рестарта сервиса ClichHouse
и проверяет вернувшийся код ответа 

Create table - создает таблицу в созданной базе данных

Install Vector- установка vector на двух хостах

Edit config vector - настраивает конфиги для двух хоств 

Install nginx - установка пакета nginx

Edit config Nginx - настройка конфига nginx

Edit host Nginx - настройка хоста

Install lighthouse - установка lighthouse

Restart Vectors - перезапуск сервисов vector

Хендлеры:

Start clickhouse service - рестарт сервиса ClichHouse

Start vector - перезапус сервиса vector 

Restart Nginx - перезапус nginx
