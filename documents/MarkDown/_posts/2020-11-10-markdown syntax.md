---
title: MarkDown Syntax
permalink: /documents/MarkDown/markdown syntax
sidebar:
  nav: markdown
aside:
    toc: false
tags: MarkDown 
---

## 1. 문단 구분을 위한 강제 개행

<div class="blue-div">
문단을 구별하려면 한 개 이상의 빈 줄을 문단 사이에 삽입하거나 줄의 마지막에 [Space bar] 를 두 번 이상 눌러 띄어쓰기를 하면 된다.
</div>

```Markdown
---
```


## 2. 헤더( Header )

<div class="blue-div">
"# 헤더 크기 (h1)"  
"## 헤더 크기 (h2)"  
"### 헤더 크기 (h3)"  
"#### 헤더 크기 (h4)"  
"##### 헤더 크기 (h5)"  
"###### 헤더 크기 (h6)"  
</div>

```Markdown
# h1
## h2
### h3
#### h4
##### h5
###### h6  
```
    

## 3. 목록( Lists )

<div class="blue-div">
순서가 없는 List
* Item 1
* Item 2
    * Item a
    * Item b

순서가 있는 List
1. Item 1
2. Item 2
3. Item 3
    1. Item a
    2. Item b

순서가 필요하지 않은 목록에 사용 가능한 기호
- 대쉬
* 별표
+ 더하기
</div>

```Markdown
Unordered
* Item 1
* Item 2
    * Item a
    * Item b

Ordered
1. Item 1
2. Item 2
3. Item 3
    1. Item a
    1. Item b
```


## 4. 강조( Emphasis )

<div class="blue-div">
- 이텔릭체는 *별표(asterisks)* 를 사용한다.
- 두껍게는 **별표(asterisks)** 를 사용한다.
- ***이텔릭체*와 두껍게**를 같이 사용할 수 있다.
- 취소선은 ~~물결표시(tilde)~~를 사용한다.
- <u>밑줄</u>은 `<u>  </u>`를 사용한다.
</div>

- 이텔릭체는 *별표(asterisks)* 를 사용한다.
- 두껍게는 **별표(asterisks)** 를 사용한다.
- ***이텔릭체*와 두껍게**를 같이 사용할 수 있다.
- 취소선은 ~~물결표시(tilde)~~를 사용한다.
- <u>밑줄</u>은 `<u>  </u>`를 사용한다.


## 5. 이미지( Images )

<div class="blue-div">
- 이미지의 파일경로.
image의 파일경로는 작성한 파일이 위치한 폴더부터 접근한다. 또는 상위의 폴더부터 접근한다?
markdown syntax 파일은 MarkDown/_posts 폴더에 있고 이미지는 MarkDown/assets 폴더에 있는데
_posts 라는 특별한 폴더에 있기 때문에 MarkDown 폴더에서부터 assets에 접근하는 것인지 확인해 볼 것.

- 이미지의 크기.
이미지의 크기는 px 단위로 지정해 줄 수 있는데, width와 height 둘중 하나의 값을 높게 설정한다고 하더라도 더 작은 크기에 비례하여 사진이 출력된다.

- 이미지의 위치.
이미지를 연속으로 출력하는 경우, 두 이미지의 width 값이 100%가 넘지 않는다면 같은 라인에 출력된다.
CSS는 별도...?
</div>

```Markdown
![테스트 이미지2](assets/testImg2.jpg){:width:"800px" height="500px"}
![테스트 이미지3](assets/testImg3.jpeg){:width:"200px" height="200px"}
![테스트 이미지](assets/testImg.jpeg){:width:"400px" height="400px"}
```


![테스트 이미지2](assets/testImg2.jpg){:width:"800px" height="500px"}
![테스트 이미지3](assets/testImg3.jpeg){:width:"200px" height="200px"}
![테스트 이미지](assets/testImg.jpeg){:width:"400px" height="400px"}


## 6. 하이퍼 링크( Links )


## 7. 코드 블록( Code Blocks )


## 8. 인용 상자( BlockQuotes )


## 9. 테이블( Tables )


## 10. 체크 박스( Task Lists )


## 11. 인라인 코드( Inline code )


## 12. 수평선 ( hr )


## 13. 탈출 문자( Backslash Escapes )
