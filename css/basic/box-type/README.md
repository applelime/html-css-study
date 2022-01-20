# Box Model, Sizing, Type

### Box Model
- Content : `컨텐츠`가 들어가는 곳  
- Padding : `안쪽 여백`, content와 border 사이의 공간
- Border : `테두리`. 굵기/스타일/색상을 꼭 명시해야 함.
- Margin : `요소와 요소 사이의 간격`을 나타낼 때

> 속기형  
top right bottom left 순서대로 적용 -> `시계방향`  
bottom 이 없으면 top과 세트로 적용  
left가 없으면 right와 세트로 적용
```css
  .box {
    padding: 10px 20px 30px 40px;
    margin: 20px 40px; /* 상하 20px, 좌우 40px */
  }
```

### Box Sizing
박스 사이즈를 잡는 방법 (width, height)
- content-box : 기본값. 사이즈를 잡을 때 `content 부분의 길이`로 계산 됨.
- border-box : 사이즈를 잡을 때 `border까지 포함한 길이`로 계산 됨.  

그렇기에 대부분 border-box를 사용한다.
```css
  * {
    box-sizing: border-box;
  }
```

### Box Type
Display 속성을 통해 Box Type을 설정할 수 있다.  
Box Type은 Block, Inline, Inline Block, Flex로 구분할 수 있으나,  
Flex는 별개의 요소라 뒤에서 설명함.

- Block : 하나의 블록으로 기본적으로 `1줄을 차지`함.  
width를 선언하지 않으면, `width = 부모의 content-box의 100%`  
width를 선언하면, `남는 공간을 margin으로 자동채움`  
따로 부모의 height를 선언하지 않으면, `자식 요소의 height 합 = 부모의 height`

- Inline : 인라인 요소로 글쓰는 것과 마찬가지로 `옆으로 쭉 배치`되며, 공간이 부족하면 내려감  
width, height 및 padding/border/margin의 top,bottom 설정 불가

- Inline Block : Inline처럼 기본적으로는 `흐르지만`, Block처럼 `영역을 잡을 수 있다.`