---
title: find_and_pack
categories:
- linux
- challenge
tags:
- find
- exec
- cp
---


# questions
## Find and package the specified files
### introduce

The challenges you need to find the `/etc` directory to meet the needs of the file, then, package and compress the file into a `tar.gz` package.


First, create a folder `/home/shiyanlou/backup`, and all the files that need to be packaged will be copied to this directory.


Then, copy all the files larger than 12K to the `/home/shiyanlou/backup` directory in the /etc directory of the lab building, and we need to keep the directory structure. For example, the `/etc/apt/trusted.gpg` file is 14K, and it will be copied to the `/home/shiyanlou/backup/etc/apt/trusted.gpg` path position. Notice that there are many files in the subfolder under the `/etc` directory that are more than 12K and need to be copied.


After the copy is completed, the `/home/shiyanlou/backup` is packaged and compressed, and the generated packet `backup.tar.gz` is placed under the `/tmp/backup.tar.gz` path.


Click to submit the result after the completion of the above task.

### target
1. The compressed packet backup.tar.gz is placed under the `/tmp/backup.tar.gz` path
2. The compressed package backup.tar.gz contains all the files larger than 12K under the `/etc` directory, regardless of whether the shiyanlou user has access to the file or not.


Please do not use soft links, such as the need to complete the copy of the file past.


### Hint
- find, copy, pack, compress


### Knowledge point
- Linux file and directory operation
- Linux file lookup operation
- Tar command package
- Gzip command compression



# keypoint

## The find command looks up some files and copies them to the specified directory

> ```bash
> sudo find /etc -size +12k -exec cp --parents {} backup \;
> ```
>
> - `exec`
> - `cp --parents`

# references

- [find,cp,exec-sample](http://blog.csdn.net/longintchar/article/details/51493562)
- [find,cp,exec-detail](https://www.kafan.cn/edu/6999644.html)
- [Preserving directory structure application instances when CP copies](http://blog.csdn.net/wgembed/article/details/39668645)

# tools

- [linux command search](http://man.linuxde.net/)
