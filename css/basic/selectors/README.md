# 선택자 (Selectors)

### Type 선택자
HTML `태그를 직접 지정`할 때 사용
```css
  h1 {
    color: #06f;
  }

  strong {
    color: #ffc82c;
  }
```

### Class 선택자
해당 `class를 지정`할 때 사용.  
class는 여러 곳에서 사용할 수 있으므로, 한 번 정의해서 여러 곳에 사용할 경우 사용한다.  
스페이스바를 구분자로 여러 개의 클래스를 가질 수 있다.
```css
  .red {
    color: #ff4949;
  }

  /* red클래스 이면서(and) blue 클래스 */
  .red.blue {
    color: #ffc82c;
  }

  /* red클래스 및(or) blue 클래스 */
  .red, .blue {
    font-style: italic;
  }
```

### ID 선택자
해당 `ID를 지정`  
ID는 식별자로 html 문서에서 1개만 존재해야만 한다.
```css
  #kimbug {
    font-style: italic;
  }
```

### 자식 선택자 (child)
바로 아래에 있는 태그를 자식이라고 한다. `>로 선택`
```css
  section > h2 {
    color: green;
    font-size: 40px;
  }
```

### 자손 선택자 (descendant)
아래에 있는 모든 태그를 자손이라고 한다. `공백으로 구분`
```css
  section h2 {
    color: #ff4949;
  }
```

### 형제 선택자 (sibling)
li처럼 같은 레벨에 있는 태그를 형제라고 한다.  
> `~`로 뒤에 있는 모든 형제 선택  
`+`로 바로 뒤에 있는 하나의 형제만을 선택
```css
  .active ~ li {
    color: purple;
  }

  .active + li {
    color: aqua;
  }
```

### 구조적 가상 클래스 (Structural Pseudo-classes)
대표적으로 first-child, last-child, nth-child
```css
  ol > li:first-child {
    color: #06f;
  }

  ol > li:last-child {
    color: #ffc82c;
  }

  ol > li:nth-child(3) {
    color: #ff4949;
  }

  /* 짝수 자식에만 적용. 근데 이런식으로 거의 안 씀 */
  ol > li:nth-child(2n) {
    color: green;
  }
```

### 동적 가상 클래스 (User Action Pseudo-classes)
대표적으로 hover, active, focus
```css
  a:hover {
    color:orange;
  }

  a:active {
    background-color: purple;
  }

  input:focus {
    border-color: #06f;
  }
```

### CSS 선택자 우선순위
1순위(금 **🥇**) : ID  
2순위(은 **🥈**) : Class, Pseudo-Class  
3순위(동 **🥉**) : Type  

- 순위가 같으면?  
-> 그 다음 순위가 많은 순서로

- 모든 순위가 같으면?  
-> 나중에 선언된 것이 적용

예시)  
#gnb.tab-nav : **🥇🥈**  
header.main-header : **🥈🥉**  
#gnb.tab-nav ul : **🥇🥈🥉**  
#gnb.tab-nav ul:last-child : **🥇🥈🥈🥉**

### rule breaker
선택자 우선순위를 깨는 것들이 있음.

> inline style
```html
  <p style="font-size: 32px;">
  </p>
```

> !important  
```css
  * {
    color: yellow !important;
  }
```