# Домашнее задание к занятию 2 «Работа с Playbook» - Сергей Ситкарёв

1. Подготовьте свой inventory-файл prod.yml.

Указал локальную машину в качестве хоста [prod.yml](https://github.com/SSitkarev/ansible-02/tree/main/inventory/prod.yml).

2. Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает vector. 
Конфигурация vector должна деплоиться через template файл jinja2. 
От вас не требуется использовать все возможности шаблонизатора, просто вставьте стандартный конфиг в template файл. 
Информация по шаблонам по ссылке. не забудьте сделать handler на перезапуск vector в случае изменения конфигурации!

Т.к. виртуалка у меня была на Debian, так же переписал установку clickhouse [site.yml](https://github.com/SSitkarev/ansible-02/blob/main/site.yml).

3. При создании tasks рекомендую использовать модули: get_url, template, unarchive, file.

4. Tasks должны: скачать дистрибутив нужной версии, выполнить распаковку в выбранную директорию, установить vector.

5. Запустите ansible-lint site.yml и исправьте ошибки, если они есть.

Использовал версию ansible [core 2.14.3], модуля ansible-lint в ней не обнаружено...

![Задание1](https://github.com/SSitkarev/ansible-02/blob/main/img/5.jpg)

6. Попробуйте запустить playbook на этом окружении с флагом --check.

![Задание1](https://github.com/SSitkarev/ansible-02/blob/main/img/6.jpg)

![Задание1](https://github.com/SSitkarev/ansible-02/blob/main/img/7.jpg)

7. Запустите playbook на prod.yml окружении с флагом --diff. Убедитесь, что изменения на системе произведены.

![Задание1](https://github.com/SSitkarev/ansible-02/blob/main/img/8.jpg)

8. Повторно запустите playbook с флагом --diff и убедитесь, что playbook идемпотентен.

![Задание1](https://github.com/SSitkarev/ansible-02/blob/main/img/9.jpg)

9. Подготовьте README.md-файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги. 
Пример качественной документации ansible playbook по ссылке. Так же приложите скриншоты выполнения заданий №5-8

10. Готовый playbook выложите в свой репозиторий, поставьте тег 08-ansible-02-playbook на фиксирующий коммит, в ответ предоставьте ссылку на него.

Добавлю как результат проделанной работы скриншот подключения к clickhouse серверу

![Задание1](https://github.com/SSitkarev/ansible-02/blob/main/img/10.jpg)
