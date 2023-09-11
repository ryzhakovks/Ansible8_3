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


