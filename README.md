## 변수 생성방법

1. 기본변수 
```
  var testA="AAA";
  var testB=1;
  let testC=11111;
  let testD="AAA";
```
2. 상수 
```
  const TEST=111;
```    

## 엄격모드 적용 방법
```
  "use strict";
```

## 자료형
1.문자형

 큰따옴표: "Hello"
 작은따옴표: 'Hello'
 역 따옴표(백틱, backtick): `Hello`
```
  let str = "Hello";
  let str2 = 'Single quotes are ok too';
  let phrase = `can embed another ${str}`;
```
1.NaN
```
  console.log("숫자가 아님" / 2 );. // 말이 되지 않는 수식 계산 시 NaN 자료형을 반환
```
2.Infinity 
```
  console.log(Infinity); // 무한데 자료형 어느 숫자든 0으로 나누면 무한대를 얻을 수 있습니다.
```
3.null,undefined
```
  let test;
  console.log(test); <= 아무 값도 없을 경우 null이 아닌 undefined 값이 표시된다.
  test=null;
  console.log(test); <= 변수에 null 값을 적용할 경우만 변수 값이 null이 된다.
```

## 객체 생성방법
ㅇ


Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/JaewonDH/Web/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
