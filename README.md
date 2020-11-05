# Oracle 18.4.0-xe  

Образ основан на github репозитории [oracle 18.4.0-xe](https://github.com/oracle/docker-images)

## Установка

    docker-compose up --build

или

    docker build --force-rm=true --no-cache=true -t zloybreg/oracle-database:18.4.0-xe

    docker run --name oracle18xe -p 1521:1521 -p 5500:5500 -e ORACLE_PWD=Admin123 -v C:\Users\dimag\docker-demo-db\oracle18xe:/opt/oracle/oradata zloybreg/oracle-database:18.4.0-xe

Время установки инстанса достаточно долгая. Все зависит от мощностей системы.  

Пременная среды:

    ORACLE_PWD=Admin123

Устанавливает пароль для учетных записей SYS, SYSTEM и PDBAdmin если переменную не указывать, то oracle во время устновки назначит свой пароль из openssl. Можно ознакомиться с файлом setPassword.sh
