Задача 1

<img width="1536" height="1101" alt="screen2" src="https://github.com/user-attachments/assets/8e7b6e59-d453-48a9-a0f6-757433dd3b10" />

Задача 3

<img width="1280" height="815" alt="screen3" src="https://github.com/user-attachments/assets/72ea10cd-233e-413b-8f9f-0f42def3fcdd" />

Задача 4

<img width="1968" height="394" alt="screen4" src="https://github.com/user-attachments/assets/9d28cb57-9519-4c01-a211-679aa86bc6c2" />
<img width="952" height="1063" alt="screen4(2)" src="https://github.com/user-attachments/assets/01bdd2ab-5820-447a-8740-927a3a55465b" />

fork: https://github.com/RoughJudah/shvirtd-example-python

Задача 5:
Скрипт backup.sh
```
#!/bin/bash

MYSQL_ROOT_PASSWORD=$(cat /opt/project/.env | grep MYSQL_ROOT_PASSWORD | awk -F= '{print $2}')
MYSQL_DATABASE=$(cat /opt/project/.env | grep  MYSQL_DATABASE| awk -F= '{print $2}')

docker run --rm --env-file /opt/project/.env  --entrypoint "" -v /opt/backup:/backup --link=mysql:alias --network=project_backend my-mysqldump:latest mysqldump --opt -h alias -u root -p"${MYSQL_ROOT_PASSWORD}" "--result-file=/backup/dumps.sql_$(date +%F_%T)" ${MYSQL_DATABASE}
```
Cron-task:
```
*/1 * * * * /opt/project/backup.sh
```

<img width="753" height="145" alt="screen5" src="https://github.com/user-attachments/assets/92fa8372-1a80-4431-bb05-4807326edb07" />

Задача 6:

<img width="1181" height="427" alt="screen6" src="https://github.com/user-attachments/assets/b780d19e-2707-4040-90ff-1637247a5e08" />
<img width="819" height="411" alt="screen6(2)" src="https://github.com/user-attachments/assets/45e99def-22aa-4e6e-8753-1694f97e0ba9" />
<img width="1010" height="364" alt="screen6(3)" src="https://github.com/user-attachments/assets/578ad39c-dae1-4250-a6fa-703ec84ea610" />
<img width="809" height="485" alt="screen6(4)" src="https://github.com/user-attachments/assets/1868114f-4b00-4107-a6ae-7114c3a0ff1a" />

Задача 6.1:

<img width="1280" height="375" alt="4" src="https://github.com/user-attachments/assets/20aefa75-84b8-4646-bdd0-c0bbb47d5d24" />
