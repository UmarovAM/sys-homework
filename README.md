# Домашнее задание к занятию "ELK" - `Умаров Азиз`

### Задание 1. Elasticsearch
Установите и запустите Elasticsearch, после чего поменяйте параметр cluster_name на случайный.

Приведите скриншот команды 'curl -X GET 'localhost:9200/_cluster/health?pretty', сделанной на сервере с установленным Elasticsearch. Где будет виден нестандартный cluster_name.

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/6a831c4e-b596-40b5-a959-528d792b7376)


### Задание 2. Kibana
Установите и запустите Kibana.

Приведите скриншот интерфейса Kibana на странице http://<ip вашего сервера>:5601/app/dev_tools#/console, где будет выполнен запрос GET /_cluster/health?pretty.

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/64d14807-e50f-42ac-aa2d-256792c851cb)


### Задание 3. Logstash
Установите и запустите Logstash и Nginx. С помощью Logstash отправьте access-лог Nginx в Elasticsearch.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx.



![image](https://github.com/UmarovAM/sys-homework/assets/118117183/303f7cf3-027b-4285-988c-6dc865e7ca22)

не могу запустить Logstash

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/16b2e0be-a830-47b7-9776-37a311b0a973)


### Задание 4. Filebeat.
Установите и запустите Filebeat. Переключите поставку логов Nginx с Logstash на Filebeat.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx, которые были отправлены через Filebeat.
