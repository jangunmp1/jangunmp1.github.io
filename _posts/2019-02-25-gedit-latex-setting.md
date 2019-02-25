---
layout: post
title: Using Latex with Gedit
category: Tips
---

Using Latex with Gedit
===============

##1. gedit plugin install
```shell
$ sudo apt install gedit-plugins
```


##2. turn on plugin

`latex plugin`과 `synctex plugin` 을 켤 것

##3. use `external tools` to compile tex file.

```sh
#!/bin/sh

filename=$GEDIT_CURRENT_DOCUMENT_NAME
mastername=`cat .$filename.ini | grep master-filename | awk -F'= ' '{print $2}'` || 2
if [ -z "$mastername" ]; then
mastername=$filename
fi
shortmastername=`echo $mastername | sed 's/\(.*\)\.tex$/\1/'`


rubber -d --synctex $mastername
evince $shortmastername.pdf &

```

* `rubber` is a latex compiler.
+ .[filename].ini 파일이 있을 경우, 이 파일에 적혀있는 master-filename의 값을 받아서 master tex file을 컴파일 함.
    - 이 파일은 gedit의 latex plugin에 의해 생성됨. 수동으로 생성할 경우 다음과 같은 형식으로 만들 것

        ```ini
        [LATEX]
        master-filename = paper.tex
        ```

## Some tips

각 서브파일 맨 위에다가 
```
% mainfile: paper.tex
```
라고 달아놓으면 서브파일에서도 synctex가 제대로 동작 (이거 없으면 forward search가 안됨)



