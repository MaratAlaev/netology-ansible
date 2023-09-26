# Домашнее задание к занятию 1 «Введение в Ansible»

## Подготовка к выполнению

1. Установите Ansible версии 2.10 или выше.
2. Создайте свой публичный репозиторий на GitHub с произвольным именем.
3. Скачайте [Playbook](./playbook/) из репозитория с домашним заданием и перенесите его в свой репозиторий.

## Основная часть

1. Попробуйте запустить playbook на окружении из `test.yml`, зафиксируйте значение, которое имеет факт `some_fact` для указанного хоста при выполнении playbook.
```
some_fact = 12
```
3. Проведите запуск playbook на окружении из `prod.yml`. Зафиксируйте полученные значения `some_fact` для каждого из `managed host`.
   ![image](https://github.com/MaratAlaev/netology-ansible/assets/46092593/29d2baac-9f8b-48d6-acbb-da9c54c7c240)

4.  Повторите запуск playbook на окружении `prod.yml`. Убедитесь, что выдаются корректные значения для всех хостов.
   ![image](https://github.com/MaratAlaev/netology-ansible/assets/46092593/647a8856-f088-4a9c-8849-4c156d05385e)

5. Посмотрите при помощи `ansible-doc` список плагинов для подключения. Выберите подходящий для работы на `control node`.
![image](https://github.com/MaratAlaev/netology-ansible/assets/46092593/5e76f32d-ae75-47d1-9971-829f3e9b6140)
