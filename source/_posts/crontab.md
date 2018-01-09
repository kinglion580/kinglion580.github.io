---
title: crontab
categories:
- linux
- challenge
tags:
- crontab
---


# question
## Periodically pack a backup log

### introduce

You are the server administrator of the experiment building, and you need to back up the log files in the `/var/log` directory every day. After the backup is packed and compressed for a long time, the file name is stored in the format of the `year-month-day.Tar.gz`. For example, the file backed up in November 1, 2017 is 2017-11-01.tar.gz, and the files after the backup are stored in the `/home/shiyanlou/backup` directory.

Note that you need to use the method of incremental backup of the tar command to make a backup.

### target

1. Add planning tasks for shiyanlou users


2. `Every day at 3 a.m`., back up the `/var/log` directory to the `/home/shiyanlou/backup/year-month-day.Tar.gz` file, and note that it is an incremental backup.


3. Backup file naming format is `year-month-day.Tar.gz`


4. Write to crontab with a command, do not write the script
### Hint

Crontab sets a tar command for an incremental backup of the specified time.

### Knowledge point

Date formatted output string
Crontab set planning tasks
Tar command incremental backup mode

# keypoint
> 0 3 * * * tar -cvf /home/shiyanlou/backup/$(date +\%Y-\%m-\%d).tar.gz -g /var/log
> - `tar.gz`
> - `0 3`
> - `\%Y\%m\%d\%H\%M\%S`

- ## how to start cron
```bash
sudo service rsyslog start
sudo cron -f &
```

- ## check whether cron is started
```bash
ps aux|grep cron
or
pgrep cron
```

- ## edit
```
crontab -e
```

- ## list
```
crontab -l
```

- ## remove
```
crontab -r
```
