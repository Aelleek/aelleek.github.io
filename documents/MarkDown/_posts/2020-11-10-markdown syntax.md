---
title: MarkDown Syntax
permalink: /documents/MarkDown/markdown syntax
sidebar:
  nav: markdown
aside:
    toc: false
tags: MarkDown 
---
# Syntax

## 1. 문단 구분을 위한 줄바꿈, 강제 개행

<div class="blue-div">
문단을 구별하려면 한 개 이상의 빈 줄을 문단 사이에 삽입하거나 줄의 마지막에 [Space bar] 를 두 번 이상 눌러 띄어쓰기를 하면 된다.
</div>

```Markdown
---
```


## 2. 헤더( Header )

<div class="blue-div">
제목, 문단별 제목을 쓸 때, 글의 구조(개요) 및 큰 틀을 잡을때 사용한다.

html 태그의 h1부터 h6까지 작성할 수 있다.
</div>

```Markdown
# h1
## h2
### h3
#### h4
##### h5
###### h6  
```

# 헤더 크기 (h1)
## 헤더 크기 (h2) 
### 헤더 크기 (h3) 
#### 헤더 크기 (h4) 
##### 헤더 크기 (h5)
###### 헤더 크기 (h6)  


## 3. 목록( Lists )

<div class="blue-div">
- 순서가 없는 List
* 의지박약
    - 이경원
    - 이천우
    - 박세훈
* 3257
    * 이경원  
    * 이천우
    * 김형근

순서가 필요하지 않은 목록에 사용 가능한 기호
- 대쉬
* 별표
+ 더하기

- 순서가 있는 List
1. 첫번째
2. 두번재
3. 세번째
    1. 첫번째
    2. 두번째
</div>

```Markdown
Unordered
* 의지박약
    - 이경원
    - 이천우
    - 박세훈
* 3257
    * 이경원  
    * 이천우
    * 김형근

Ordered
1. 첫번째
2. 두번재
3. 세번째
    1. 첫번째
    2. 두번째
```


## 4. 강조( Emphasis )

<div class="blue-div">
문장 내 강조하고 싶은 단어를 눈에 띄게 표시한다.

- 이텔릭체는 *별표(asterisks)* 를 사용한다.
- 두껍게는 **별표(asterisks)** 를 사용한다.
- ***이텔릭체*와 두껍게**를 같이 사용할 수 있다.
- 취소선은 ~~물결표시(tilde)~~를 사용한다.
- <u>밑줄</u>은 `<u>  </u>`를 사용한다.
</div>

- 이텔릭체는 *별표(asterisks)* 를 사용한다.
- 두껍게는 **별표(asterisks)** 를 사용한다.
- ***이텔릭체*와 두껍게**를 같이 사용할 수 있다.
- 취소선은 ~물결표시(tilde)~를 사용한다.
- <u>밑줄</u>은 `<u>  </u>`를 사용한다.


## 5. 이미지( Images )

<div class="blue-div">
이미지 넣는 방법에는 3가지가 있다.

1. 원본 이미지 넣기.
2. 사이즈를 조절하여 이미지를 넣기.
3. 이미지를 넣은 후 링크 걸기.
</div>

```Markdown
![테스트 이미지1](assets/testImg.jpg)
<img src="assets/testImg2.jpeg" width="300" height="300">
[![테스트 이미지3](assets/testImg3.jpeg)](aelleek@github.io)
```

<div class="yellow-div">
teXt Jekyll 테마에서 제공하는 방법을 사용하면 img 태그를 사용하지 않아도 사이즈를 조절 할 수 있다.
</div>

```Markdown
![테스트 이미지2](assets/testImg2.jpg){:width:"800px" height="500px"}
![테스트 이미지3](assets/testImg3.jpeg){:width:"200px" height="200px"}
![테스트 이미지](assets/testImg.jpeg){:width:"400px" height="400px"}
```

<div class="blue-div">
- 이미지의 파일경로.
image의 파일경로는 작성한 파일이 위치한 폴더부터 접근한다. 또는 상위의 폴더부터 접근한다?
markdown syntax 파일은 MarkDown/_posts 폴더에 있고 이미지는 MarkDown/assets 폴더에 있는데
_posts 라는 특별한 폴더에 있기 때문에 MarkDown 폴더에서부터 assets에 접근하는 것인지 확인해 볼 것.

- 이미지의 크기.
이미지의 크기는 px 단위로 지정해 줄 수 있는데, width와 height 둘중 하나의 값을 높게 설정한다고 하더라도 더 작은 크기에 비례하여 사진이 출력된다.

- 이미지의 위치.
이미지를 연속으로 출력하는 경우, 두 이미지의 width 값이 100%가 넘지 않는다면 같은 라인에 출력된다.
원하는 CSS가 있다면 별도로 지정해주어야 한다.    
</div>

![테스트 이미지1](assets/testImg.jpeg)
<img src="assets/testImg2.jpg" width="300" height="300">
[![테스트 이미지3](assets/testImg3.jpeg){:width:"300px" height="300px"}](https://aelleek.github.io)


## 6. 하이퍼 링크( Links )

<div class="blue-div">
클릭하면 다른 페이지, 다른 부분으로 이동할 수 있다.

사용하는 방법에는 3가지가 있는데,
1. 하이퍼 링크가 된 단어를 클릭하면 설정된 URL로 이동하는 방법.
2. URL을 입력해서 주소 자체에 링크를 거는 방법.
3. 동일 파일 내에서 문단을 이동하는 방법.
4. 상대 경로로 서버 내 파일 이동.
</div>
<div class="yellow-div">
3번째 - 문단 매칭방법 : 
제목(header)를 복사 붙여넣기 후,
1) 특수문자제거
2) 스페이스를 갯수만큼 -로 변경
3) 대문자->소문자로 변경
예) “#Syntax” -> “#syntax”

문단으로 이동이라서 h1 태그에 해당하는 # 으로만 이동이 되는것같다??
</div>

```Markdown
1. [Aelleek's blog](http://aelleek.github.io)
2. <https://aelleek.github.io>
3. [동일 파일 내 문단 이동](# syntax)
```

1. [Aelleek's blog](http://aelleek.github.io)
2. <https://aelleek.github.io>
3. [동일 파일 내 문단 이동](#syntax)


## 7. 코드 블록( Code Blocks )


## 8. 인용 상자( BlockQuotes )

<div class="blue-div">
글을 인용할 경우 사용한다. 중복 형태로도 사용할 수 있다.
</div>

```Markdown
> 이경원
>> 최근 재미있게 본 글
>>> 오늘도 모두가 열심히 사는것 같아서 나만큼은 쓸모없게 살아야 겠다고 다짐했다.
```

> 이경원
>> 최근 재미있게 본 글
>>> 오늘도 모두가 열심히 사는것 같아서 나만큼은 쓸모없게 살아야 겠다고 다짐했다.


## 9. 테이블( Tables )

<div class="blue-div">
    
    
</div>


## 10. 체크 박스( Task Lists )


## 11. 인라인 코드( Inline code )


## 12. 수평선 ( hr )


## 13. 탈출 문자( Backslash Escapes )
