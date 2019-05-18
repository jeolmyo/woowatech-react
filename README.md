우아한테크1기 React with Typescript 과정을 복습한다. 
> 갓민태님의 교육과정 사이트 - https://codebrew.kr/

# 1일차
tsx - UI를 포함한 타입스크립트.
ts - 걍!

ES7 기반. BABEL 로 translate 한다.

typescript 를 사용하려면 타입 디파인이 돼 있어야 하고, npm에 @types 로 시작하는 모듈들을 사용하면 된다.
리액트도 @types/react 를 추가해줘야 한다.

UI를 포함하고 있는 파일에서는, 리액트 모듈을 반드시 import 해줘야한다. 리액트가 js 표준이 아니어서, 따로 translator 가 처리를 하는데 이걸 할지 말지를 import 여부로 판단한다.

번들러가 js 파일이 아닌 녀석들도 import 시킬 수 있게 해준다. (하지만 보통 서비스에서는 이렇게는 안씀. 성능 등 이슈)

react는 컴포넌트 만드는 방법을 3가지 재공함.
Component, PureComponent, Functional Component
FC 는 LifeCycle 을 관리 할 수 없다.

타입스크립트의 타입 기술 방법
const <변수명>: <타입>

리액트에서 쓰이는 html 마크업들은 실제 html 이 아니지만 98% 동일. 리액트에서는 tag 를 컴포넌트라고 부르고, 기본 제공되는건 소문자, 사용자 정의는 대문자로 시작하는게 컨벤션이다.

UI를 리턴하면, 다른데에서 import 해서 tag 안에 쓰면 된다.

모든 컴포넌트는 Props (Properties) 로 데이터를 주고 받는다.
컴포넌트가 가지고 있는 자체상태가 있는데, 이를 Local State 라고 한다.

UI와 비지니스로직은 분리한다. 컴포넌트는 값을 받을수만 있고 내보낼 순 없음. 그래서 function 을 받아서 callback 으로 이벤트를 호출한다.

리액트는 class를 정의하지만 개발자가 직접 객체를 만들지는 않는다. 리액트가 직접 생성한다.

디렉토리에서 index.ts가 디렉토리의 루트역할을 한다. 여기에 export  문을 기술해 주면, 사용하는 쪽에서는 해당 디렉토리만 import 해주면 된다. 이로써 디렉토리안의 구조 변화가 외부로 전파되지 않게 할 수 있다.




