---
title: 깃허브 블로그 시작!
permalink: /documents/GitHub Blog/Start GitHub Blog 
sidebar:
  nav: study
tags: GitHub Blog 
---

# 블로그 시작!

- 사용하려고 하는 목적

- blog directory 구조

- 사용하는 방법
    + 네비게이션 추가하는 방법
    + 문서 추가하는 방법
    + 문서 작성할 때 추가해야 하는것들




### 해야하는 것들
- documents 폴더 구조 정리하기

- 각 문서에 태그 설정하는 방법.
- 문서에 이미지 넣는 방법
- 표 쉽게 넣는 방법 찾아보기
- 내가 원하는 디자인의 블록을 설정할 수 있는지

- 홈 화면에 무엇을 넣을지
- about 화면에 무엇을 넣을지 
- 어떻게 넣을지



jekyll 디렉토리 구조

includes : 블로그 삽입 html
layouts : 블로그 레이아웃 html
posts : 블로그 컨텐츠들
sass : css 파일들
site : 지킬로 빌드된 블로그 내용들
assets : 이미지파일, js파일, css파일들
config.yml : 블로그 생성에 필요한 config가 적힌 파일들



https://devyurim.github.io/development%20environment/github%20blog/2018/01/01/blog-1.html



Ruby 설치 및 실행 방법

$ sudo gem install jekyll

$ sudo bundle install


jekyll 초기화 및 실행

$ jekyll new ./

$ jekyll build
$ jekyll serve --watch