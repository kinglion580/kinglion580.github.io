
---
title: sed_markdown
categories:
- linux
- challenge
tags:
- sed
---

# question

## optimize markdown documents with sed

### introduce

You are the document inspector of the shiyanlou, need to check document format every day, a document found in different marks appear blank between too much (provisions require only a blank document appeared in 2, 3 cases), and all the image formats are written into the link, need you use this document to quickly repair Sed.

For example, a document does not regulate instances and link errors:
```
## title one

## Title Two



## Title Three

[picture-1] (https://www.shiyanlou.com/test.png)
```

Title Two and Title Three require only one empty line directly.

you should execute the Sed script in this way:
```
Sed -f /home/shiyanlou/fix-format.sed document
```

After execution, the document is turned into:
```
## title one

## Title Two

## Title Three

[picture-1] (https://www.shiyanlou.com/test.png)
```

### target

1. The script path must be placed in the `/home/shiyanlou/fix-format.sed`
2. The way to call is: `sed -f /home/shiyanlou/fix-format.sed` document
3. Delete extra repeat blank lines in a document
4. revising the format of the picture link

### Hint

1. sed matching empty lines

2. the hints of the picture link are all in [picture-xxx] format, and the suffix of the address is.Png or.Jpg

3. test document download link: http://labfile.oss.aliyuncs.com/courses/980/test-document.md

### Knowledge point

- regular expression
- Sed

# keypoint
- **delete rows retain only one line**
```
/^$/{
  N
  /^\n$/D
}
```
- **replace**
```
s/\[picture/\!\[picture/
```
*Note that the escape character*

# references

- [my-knowledge-sed](https://github.com/kinglion580/syl_linux/blob/master/knowlege/sed.md)
