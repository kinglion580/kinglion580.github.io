---
title: monitor_mysql
categories:
- linux
- challenge
tags:
- ps
- netstat
- crontab
---


# question

## monitor service with bash
### introduce

On the server, our services may be hung up for a variety of reasons, such as mongodb Out of memory, and the system is kill, resulting in the service can not work properly. So we need a simple monitoring script `check_service.sh` to view the status of our service in real time. If the service state is stopped, we can try to restart the service automatically.

The script can accept a parameter, which is the name of the service. The name of the service can use the service command to view, start and stop the state. For example, check the status of the MySQL service.
```
$bash /home/shiyanlou/check_service.sh mysql
Is Running
```
If the MySQL service is not running, the MySQL service is started and the following output information is printed:
```
$bash /home/shiyanlou/check_service.sh mysql
Restarting
```
If the service does not exist, the error information is output:
```
$bash /home/shiyanlou/check_service.sh notfoundservice
Error: Service Not Found
```

### target

1. The script is named `check_serive.sh`, and the path must be `/home/shiyanlou/check_service.sh`


2. The script can `accept a parameter`, the parameter is the name of the service, and the check_service.sh service name can be called in this way


3. If the service is running "is Running", if the service is stopped, the service is started, and if the service does not exist, output error information


4. `/home/shiyanlou/check_service.sh mysql` is put into crontab once a day, which can ensure that MySQL service can be restarted when it is hung up, and we need to manually start cron service.

### Hint

1. You can use `sudo service xxx start/status/stop` for service management
2. Use of command line position parameters
3. Service status information use can be judged by grep

### Knowledge point

- Bash process control
- The control of service and process
- Crontab

### keypoint

```bash
#!/bin/bash

if [ `ps -ef|grep -v grep|grep $1|wc -l` -gt 3 ];then
    echo "is Running"
else
    sudo service $1 start
    if [ `ps -ef|grep -v grep|grep $1|wc -l` -gt 2 ];then
        echo "Restarting"
    else
        echo "Error:Service Not Found"
    fi
fi
```

```bash
#!/bin/bash

if [ `netstat -at|grep $1|wc -l` -gt 0 ];then
    echo "is Running"
else
    sudo service $1 start
    if [ `netstat -at|grep $1|wc -l` -gt 0 ];then
        echo "Restarting"
    else
        echo "Error:Service Not Found"
    fi
fi
```
#### view the process
> - `ps -ef`
> - `grep -v` exclude the grep process
> - `wc -l` count row num
> - `netstat -at|grep mysql`
> - `pstree` show the derived relation between the proceses in a tree diagram way

#### start crontab
> `sudo service rsyslog start`
>
> `sudo cron -f &`
