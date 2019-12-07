 # CSS 

## 목차
+ [CSS란](#css란)

+ [중복제거효과](#중복제거효과)

+ [선택자와 속성(selector,property)](#선택자와-속성(selector,property))

+ ★[box model](#box-model)

+ ★[grid model](#grid-model)

+ [미디어 쿼리란](#미디어-쿼리란)

----------------------

### CSS란

+ HTML - 정보전달집중 문서

+ CSS - 컬러나 박스 등을 사용하여 정적인 HTML문서을 꾸며준다

+ Javascript - 정적인web을 사용자에 움직임에따라 반응하도록 만들어준다(반응형) 
~~~
html문서 내부에
<style></style> 을 사용할수있지만
유지 보수에 유리하기 위해
보통 css 파일을 따로 만들어
링크시킨다(중복제거효과)
ex
<link rel="stylesheet" href="style.css">
                                문서제목
~~~

----------------------

### 중복제거효과

+ 코드가 깔끔해진다
+ 유지 보수가 쉬워진다
+ 가독성증가
+ 정보 전달 집중
+ 트래픽을 줄여준다

----------------------

### 선택자와 속성(selector,property)

#### 기본구조
~~~
ex)
selector(선택자) 

a{
        color:red;
        
        property:value(속성:값) ;(항상 세미클론완성)
}

 ,를 통해 2개이상 선택자도 가능하다

 #id element (id를 가진 부모태그(elemnet))
~~~

#### class와id

class="classname" 그룹화하다
~~~
.class name{


}
~~~
id="idname" id값설정
~~~
#id name{


}
~~~

우선적용<br/>
tag < class < id(단한번)<br/>

포괄적<br/>
tag > class > id(단한번)

----------------------

### box model

#### 기본성격

+ 화면 전체를 쓰는 블록레벨엘리먼트=블록(block level element)<br/>

+ 콘텐츠 크기만큼 쓰는 인라인레벨엘리먼트=인라인(iline level element)


바꿀수있다
{display: inline; or display: block;} 을 통해 바꿀수있다.
~~~
border:0px solid red 빨간테두리(박스)를만든다
                속성
                padding:?; 테두리와 컨텐츠 간격
                margin:?;  테두리와 테두리 사이 간격
                width:?;        폭
                heigh:?;        높이
            
        ■■■■■■■■■■■■■■■■■■■■ margin ■■■■■■■■■■■■■■■■■■■■■■■
        /                                                  /
        /     ■■■■■■■■■■■■■■■ border ■■■■■■■■■■■■■■■■■■■   /
        /     /                                        /   /
        /     /    ■■■■■■■■■■■ padding ■■■■■■■■■■■     /   /
        /     /    /          [content]          /     /   /
        /     /    ■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■     /   /
        /     /                                        /   /
        /     ■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■/   /
        /                                                  /
        ■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■
+ 적극적으로 개발자도구(F12)를 활용한다

boeder-top: px  특정 위아래좌우 테두리를 적용, padding,margin동일
        bottom
        left
        right


~~~

#### div와 span

: 의미도 없고 기능도 없다(디자인을 위해 그룹)
~~~
<div></div> block 모델을 만들어준다
<span></span> inline 모델로 만들어준다

+ a태그,텍스트는 (inline성격)
h1태그는(block)
미리 알아야한다
~~~

----------------------

### grid model

적용을 원하는 태그를 인라인인 경우<br/>
div(블록)또는 span(인라인)로 감싸고<br>
부모태그역시 div로 만든다

~~~
ex)
<style>
                                
        #grid{                                  
            border:5px solid pink;              
            display:grid;                               
            grid-template-columns: 150px 1fr;              
        }                                    3.id를{
                                                display:grid; 그리드로형식
                                                grid-template-columns: 열 몇대몇
                                                150px 1fr(150px 나머지 화면전체)
                    
    </style>

<body>
  <div id="grid">                   2.부모태그 div에 id를 준다
        <div>NAVIGATTION</div>      1.이렇게 div로 감싼다
        <div>ATTICLE</div>
    </div>
<body>
~~~

----------------------

### 미디어 쿼리란
: 다양한 디바이스에서 반응한다

~~~
@media(min-width:800px){
        최소 스크린이 800px이상일때 반응일때 ~~css을 ~적용한다
       (max-width:800px)최대 이하에서 반응


       
}
~~~



<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
박스모델 그리드는 많이 연습을 해봐야할거같다.
아직 갈일이 멀지만 힘내자