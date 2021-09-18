마크다운은 텍스트 기반의 마크업 언어로 쉽게 읽고 쓸 수 있으며, HTML로 변환이 가능한 언어로 관리가 쉽고 지원가능한 플랫폼과 프로그램이 다양하다.

하지만 모든 HTML의 마크업을 대신하지 못하고 표준이 없다.

Github내에 작성하느 README.md에서 md가 바로 마크다운의 약어이기도 하다.

## 문법 정리

### 제목(Header)

---

html의 `<h1~6/>`와 같은 사용이다.

```markdown
# 제목1

## 제목2

### 제목3

#### 제목4

##### 제목5

###### 제목6
```

### 문장(Paragraph)

---

- 줄바꿈 - 띄어쓰기 2번이상 또는 <br/>

  ```markdown
  동해물과 백두산이 마르고 닳도록  
  하느님이 보우하사 우리나라 만세<br>
  무궁화 삼천리 화려 강산<br/>
  대한 사람 대한으로 길이 보전하세
  ```

  동해물과 백두산이 마르고 닳도록 하느님이 보우하사 우리나라 만세<br>
  무궁화 삼천리 화려 강산<br>
  대한 사람 대한으로 길이 보전하세

### 강조(Emphasis)

---

- 기울기 - `_문장_` or `*문장*`

  ```markdown
  _Italic_
  ```

  _Italic_

- 두껍게 - `**문장**` or `__문장__`

  ```markdown
  **Bold**
  ```

  **Bold**

- 취소선 - `~~문장~~`

  ```markdown
  ~~Cancell Line~~
  ```

  ~~Cancelline~~

- 밑줄 - `<u>문장</u>`

  ```markdown
  <u>UnderScore</u>
  ```

  Underscore

### 목록(List)

---

- 순서 매기기

  ```markdown
  1. 첫번째
  2. 두번째
  ```

  1. 첫번째
  2. 두번째

- 글머리 기호 목록

  - `-` , `*` , `+`
  - `Tab` , `SpaceBar` 를 통해 들여쓰기

  ```markdown
  - 목록1
    - 목록1.1
      - 목록1.2

  * 목록2
    Tab 두번 하면 코드 블럭을 만들 수 있다.

  - 목록3
    - 목록3.1
      - 목록3.2
  ```

  - 목록1
    - 목록1.1
      - 목록1.2
  - 목록2

    ```
      Tab 두번 하면 코드 블럭을 만들 수 있다.
    ```

  - 목록3
    - 목록3.1
      - 목록3.2

### 링크(Links)

---

`["출력될 문장"] ("url")`

- `target="_blank"` 처럼 새 창 열기는 마크다운이 아닌 순수 html 코드로 작성

```markdown
<a href="https://google.com">GOOGLE</a>
[GOOGLE](https://google.com)

<a href="https://naver.com" title="NAVER로 이동">NAVER</a>
[NAVER](https://naver.com "NAVER로 이동")
```

[GOOGLE](https://google.com)

[NAVER](https://naver.com)

### 이미지(Images)

---

`!["이미지 설명"] ("이미지 경로 or URL")`

이미지에 링크삽입 - `!["이미지 설명"] ("이미지 경로 or URL")("Link URL")`

```markdown
![차콜색 커튼](https://i.pinimg.com/236x/d6/65/7d/d6657d1634ed34170ec7921a0d77e791.jpg)

![차콜색 커튼](https://i.pinimg.com/236x/d6/65/7d/d6657d1634ed34170ec7921a0d77e791.jpg)(https://www.pinterest.co.kr/pin/379569074847873765/)
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29a093a2-3310-499e-85d4-0129386907c0/Untitled.png)

링크가 삽입되지 않은 이미지

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29a093a2-3310-499e-85d4-0129386907c0/Untitled.png)

링크가 삽입된 이미지

### 인용(BlockQuote)

---

```markdown
> 첫번째 인용문
>
> > 두번째 인용문
> >
> > > 세번째 인용문
```

> 첫번째 인용문
>
> > 두번째 인용문
> >
> > > 세번째 인용문

### 코드 강조

---

- 인라인(Inline) 코드 강조

  ```markdown
  문장 내에서 코드 `code` 를 강조하고 싶을 때 사용할 수 있다.
  ```

  문장 내에서 코드 `code` 를 강조하고 싶을 때 사용할 수 있다.

- 블록(Block) 코드 강조

  `(백틱)세번으로 블록 코드의 영역을 앞 뒤로 지정하며, 첫 ``` 뒤에는 javscript, html, css 등의 코드 타입을 명시하고 다음 줄부터 코드 내용을 입력한다.

  ````markdown
  ```"javascript"
  function() {
  	console.log('Hello World!');
  }
  ```
  ````

  ```jsx
  function() {
  	console.log('Hellow World!');
  }
  ```

### 표(Table)

---

마크다운 테이블을 만드는 데 유용한 사이트 [https://www.tablesgenerator.com/markdown_tables](https://www.tablesgenerator.com/markdown_tables)

```markdown
| Table Header1 | Table Header2 | Table Header3 |
| :------------ | :-----------: | ------------: |
| **Cell**      |     Cell      |   <u>Cell</u> |
| Cell          |     Cell      |          Cell |
| Cell          |     Cell      |          Cell |
```

| Table Header1 | Table Header2 | Table Header3 |
| :------------ | :-----------: | ------------: |
| **Cell**      |     Cell      |   <u>Cell</u> |
| Cell          |     Cell      |          Cell |
| Cell          |     Cell      |          Cell |

로 출력되며, |---:|에는 우측정렬을 |:---:|인 경우 가운데 정렬을 한다.

### 원시 HTML(Raw HTML)

---

원시 HTML 문법을 사용하여 마크다운을 작성할 수 있다.

즉 마크다운으로 표현해 낼 수 없는 것을 원시 HTML 문법을 통해서 구현이 가능하다.

### 수평선(Horizontal Rule) : 구분선

---

- 구분짓는 수평선으로

  1. `---`
  2. `***`
  3. `___`

  ```markdown
  ---
  ---

  ---
  ```

  ***

  ***

  ***

  다음과 같이 수평의 구분선이 출력된다.
