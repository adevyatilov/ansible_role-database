роль database
--------------
 
 Установка postgresql, cоздание пользователя и базы данных 


Переменные роли
--------------

  * ``varсr_`` (variable when calling the role) - перменные, которыe передаются при вызове роли
  * ``def_`` (define) - перменные определенные в файле defaults/main.yml
  * ``varcr_db_name``     - имя базы данных 
  * ``varcr_db_user``     - имя пользователя базы данных
  * ``varcr_db_password`` - пароль для пользователя базы данныx
  * ``def_database_port`` - порт БД


Пример Playbook
----------------
```yaml
# secret.yaml - файл с переменной varcr_db_password

  - hosts: web
    vars_files:
      secret.yaml 
    roles:
      - role: database
        varcr_db_name: bd
        varcr_db_user: user
        varcr_locale: en_US.UTF-8
```
