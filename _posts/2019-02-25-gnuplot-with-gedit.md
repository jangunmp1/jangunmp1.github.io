---
layout: post
title: Using Gnuplot with Gedit
category: Preferences
---

#### Gedit의 external tools에 다음을 추가.

```bash
#!/bin/sh
#cd $GEDIT_CURRENT_DOCUMENT_DIR
echo $GEDIT_CURRENT_DOCUMENT_NAME
gnuplot $GEDIT_CURRENT_DOCUMENT_NAME
output=$(cat $GEDIT_CURRENT_DOCUMENT_NAME | grep "set output" | awk '{print $3}' | sed 's/'\''//g')
evince $output
```

참고: 단축키를 지정 하면 편하다 (예: ctrl + f11)

