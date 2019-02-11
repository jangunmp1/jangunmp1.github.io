---
layout: post
title: 가상머신 디스크 이미지 크기 줄이기 
category: Tips
---

### 1. client 내에서 다음 명령어를 통해 사용되지 않는 영역을 모두 0으로 채운다.

  ```bash
  sudo dd if=/dev/zero of=test.file bs=4M && sync
  sudo rm test.file
  ```

### 2. host 컴퓨터에서 다음 명령어로 가상머신 디스크 이미지 크기를 줄인다.

  ```bash
  VBoxManage modifyhd --compact yourImage.vdi
  ```
