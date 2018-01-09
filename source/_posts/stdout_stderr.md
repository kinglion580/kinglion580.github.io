---
title: stdout_stderr
categories:
- linux
- challenge
tags:
- stdout
- stderr
---

# determine if output is stdout or stderr

## solution
- **redireciton**
> - standard input: `0`
> - standard output: `1`
> - standard error: `2`


- **print STDERR in red**
```bash
bash func 2> >(while read line; do echo -e "\e[01;31m$line\e[0m" >&2;done)
```
![实验楼](https://dn-simplecloud.shiyanlou.com/5962221513739678076-wm)

## references
- [determine if output is stdout or stderr](https://superuser.com/questions/453598/determine-if-output-is-stdout-or-stderr)
- [bash:print stderr in red color](https://serverfault.com/questions/59262/bash-print-stderr-in-red-color#)
