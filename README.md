
## Задание 1
Проведите разведку системы и определите, какие сетевые службы запущены на защищаемой системе:

sudo nmap -sA < ip-адрес >

sudo nmap -sT < ip-адрес >

sudo nmap -sS < ip-адрес >

sudo nmap -sV < ip-адрес >

В качестве ответа пришлите события, которые попали в логи Suricata и Fail2Ban, прокомментируйте результат.

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/f9319282-77d2-43dd-9e61-b757a17917b7)
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/550940cd-3d61-4592-a101-704240dbc942)

### Cканирование nmap
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/ffd2d19b-c47f-4dcd-ba5f-d0a5e97b57d8)

### Логи Suricata:
nmap -sA, нет записи в логах, все ACK пакеты были проигнорированы межсетевым экраном.

Остальные сканирования были помечаны как трафик с потенциальной угрозой в соответствии с установленными правилами в 
 /var/lib/suricata/rules
 
при nmap -sT
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/63e505dc-1f08-4872-a352-47da05462398)


при nmap -sS
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/446b3ad7-5c79-494c-930e-5cc0597822cb)

при nmap -sV

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/74d4f320-dea1-413e-9ebe-17fbc7b924b0)

### Логи Fail2Ban:

В логах Fail2Ban не было записей, так как в правилах одна запись sshd

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/96a3252e-6ee1-4adf-9540-b72d40f27ee8)


## Задание 2

