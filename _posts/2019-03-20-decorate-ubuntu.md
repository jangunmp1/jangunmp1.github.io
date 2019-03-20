---
layout: post
title: 우분투 꾸미기 
category: Preferences
---

우분투 18.04 버전을 설치하자마자 보이는 보라색 화면은 영 맘에 들지 않음.
아이콘도 별로고, 창 모양도 뭔가 모르게 지저분해보임.

요즘 대세인 material design으로 flat하게 꾸며보자.

## 1. 사전 작업

### gnome-tweak-tool 설치

ubuntu는 기존에는 unity를 기본 데스크탑 환경으로 사용하였는데, 18.04 버전부터 gnome을 사용한다.
gnome-tweak-tool은 gnome 데스크탑 환경을 설정하는데 사용되는 도구이다.

다음 명령어로 gnome-tweak-tool을 설치한다.

```bash
sudo apt install gnome-tweak-tool
```

### gnome-extension 설치

{https://extensions.gnome.org/}[https://extensions.gnome.org/]에 접속하여 다음 두 gnome extension을 설치한다.

1. User Themes (그놈 쉘의 대쉬, 패널 등을 꾸미는게 가능하도록 해줌)
2. Dash To Panel (그놈 쉘의 상단 바와 대쉬를 없애고, 화면 아래에 패널을 만들어줌 (마치 윈도우 처럼) )

## 2. flat-plat-blue 테마 설치

1. {flat-plat-blue github 저장소}[https://github.com/peterychuang/Flat-Plat-Blue] 를 참고하여 flat-plat-blue 테마 설치
2. gnome-tweak-tool --> 모양새(appearance) --> 프로그램 부분과 쉘 부분 각각을 `Flat-Plat-Blue`로 수정

## 3. papirus 아이콘 팩 설치

1. 아래 명령어로 papirus 아이콘 팩 설치
```bash
sudo apt install papirus-icon-theme
```
2. gnome-tweak-tool --> 모양새(appearance) --> 아이콘 부분을 `Papirus`로 수정

## 4. Breeze 마우스 커서 테마 설치

1. 아래 명령어로 breeze 커서 테마 설치
```bash
sudo apt install breeze-cursor-theme
```
2. gnome-tweak-tool --> 모양새(appearance) --> 커서 부분을 `Breeze_Snow`로 수정


## 5. 고해상도 모니터 설정

화면 해상도가 높아서 글씨가 너무 작게 보일 때

### 글씨 크기 키우기
1. gnome-tweak-tool --> 글꼴 --> 스케일 상수를 적당히 수정 (1.25 등의 소수점 표현 가능)

### 아이콘 크기 키우기
1. 탐색기 (nautilus) 에서 키보드의 `ctrl` 키를 누른 상태에서 마우스 스크롤을 하여 아이콘 크기 조절

### 커서 크기 키우기
1. 설정 --> 접근성 --> 커서크기 부분을 조절

