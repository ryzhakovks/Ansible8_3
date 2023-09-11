# 08-ansible-03-yandex

## Что делает playbook

Плейбук на трех хостах выполнит установку:

- Clickhouse
- Lighthouse/Nginx	
- Vector/Nginx

## Какие у него есть параметры

- Все приложения будут установлены из RPM-пакетов
- IP хостов нужно задать в файле инвентаризации [prod.yml](playbook/inventory/prod.yml)
- Изменить переменные для соответствующих приложений, можно в файлах находящихся в одноимённых папках [group_vars](playbook/group_vars).
- Изменить конфиги приложений можно в дирректории [templates](playbook/templates)

## Доступ к БД clickhouse

- Переходим на сайт - указываем IP адрес сервера clickhouse-01, появится страница с доступом к БД clickhouse через web
- Переходим на сайт сервера clickhouse-02
- Можно проверитьстраницу clickhouse-03 там мы увидим стандартную страницу  Welcome to CentOS
- Переходим на сайт clickhouse-02, можно увидить логи с сервера clickhouse-03 (пример лога: 46.138.174.91 - - [10/Jun/2022:19:48:27 +0000] "GET /js/ace-min/mode-clickhouse.js HTTP/1.1" 200 12424 "http://51.250.31.18/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/102.0.5005.63 Safari/537.36" "-")
