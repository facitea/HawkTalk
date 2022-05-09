# HawkTalk

## 1차 기획안(학습 목표)
> ### 개요
- Social Media/Messenger 융합
- 차세대 메신저 서비스 구축

> ### 목적
- 1020세대를 타겟으로 오락성을 갖춘 가벼운 웹애플리케이션 개발

> ### 기술
- 웹 애플리케이션 기반(Javascript)
- node.js / express.js 기반 서버
- React.js

> ### 기능/기술
- Social Media로서 간단한 CRUD 기능 구현(twitter 벤치마킹)
- 간단한 

> ### 수익모델
- 광고연동

> ### 부가기능(오락요소 등/금지어 방장설정가능 등)

## 2차 목표
- 하이브리드앱 or 네이티브앱으로 확장(모바일 애플리케이션 스택)
- 수익모델 확장(과금 요소 추가 등)



프로토타입 구현 1.5개월
html/css/js

백엔드 구현 1.5개월
node.js



로그인(메인)

회원가입

회원정보수정

채팅창

나+설정

인스타처럼
Hawktalk 홈 메시지 안내 나 검색
센터로 고정

기본=로그인-회원가입
로그인됐으면

vue 적용 3개월
vue.js

백엔드 적용 3개월
express.js

9개월 프로젝트

=============================
vue 학습 내용


라우터 링크 - 링크형식으로 누르면 화면 전환됨
ㄴ링크 누르면 /about 형식처럼 주소도 변함

views 폴더에 라우팅 될 페이지 정리

index.js 파일에서 라우트 레벨에서 코드를 분할하는 것

{
    path: '/about',
    name: 'about',
    // route level code-splitting
    // this generates a separate chunk (about.[hash].js) for this route
    // which is lazy-loaded when the route is visited.
    component: () => import(/* webpackChunkName: "about" */ '../views/AboutView.vue')
  }

이런식으로 라우트하면 방문했을때 리소스를 로드하게 됨.

prefetch 기능은 미래에 사용될 가능성이 잇는 리소스를 캐시에 저장해두는 것 - 잘못사용하면 렌더링 시간이 늘어날 수 있다.
ㄴ첫 화면을 가장 마지막에 가져온다
ㄴ리소스가 크지 않다면 기능을 사용하지 않더라도 사용자 접속 시점에 다운받아도 매끄럽게 동작한다
ㄴ리소스가 매우 크다면 미리 받는게 나을수도 있음

views 폴더에 우리가 페이지라고 부르는 화면 하나하나에 해당하는 vue 컴포넌트 파일을 생성하고
components 폴더에는 다른 vue 파일에서 호출해서 공통으로 사용할수 있는 vue 컴포넌트 파일을 생성하고 관리

snippet 기능 - 코드 작성한거 등록해놓고 단축키로 코드 가져오기

v-html : 태그 형식으로 html 코드를 넣을수 있음

<input type="text" v-model="valueModel" />
ㄴv-model을 통해 value값을 data에 저장하는듯
ㄴv-model.number로 하면 숫자로 저장됨

textarea v-model="@@@"로 해야 텍스트에어리어 사용가능

===================================================
22/4/3
vue 전체 기본 형식 파악 및 이식
->디자인과 함께 router link 관한 학습 이루어져야 함.

22/4/9
일주일 간 해야할 것
트위터 처럼 게시판을 구성하되
https://chb2005.tistory.com/36

참고하여 한 글에 3줄 가량의 텍스트만 보관할 수 있도록
폰트 등 사용 불가
공개 비공개 정도로 사용

22/4/25
SNS에 집중한 것인 만큼 모바일 친화적인 반응형으로 구성할 필요가 있다.
다만, 메신저로서의 기능은 페이스북 메신저 처럼 별개의 앱을 빌드하는 것이 좋겠다.
고로, SNS로서의 기능. 커뮤니티로서의 기능을 기본적으로 구축한 후 메신저 기능을 만들자.

https://code-study.tistory.com/22
제이쿼리 통해서 무한 스크롤이 된다.

22/5/7
git push -u origin +master
pull 해도 안되면 이렇게라도 해야한다.

22/5/9
error  'user' is defined but never used  no-unused-vars

다음과 같은 에러가 뜰 경우, 에러가 발생한 줄 옆에

 

// eslint-disable-line no-unused-vars

위의 주석을 달아주면 해결된다

https://gyoogle.dev/blog/web-knowledge/vue-knowledge/Vue.js%20+%20Firebase%EB%A1%9C%20%EC%9D%B4%EB%A9%94%EC%9D%BC%20%ED%9A%8C%EC%9B%90%EA%B0%80%EC%9E%85,%20%EB%A1%9C%EA%B7%B8%EC%9D%B8%20%EA%B5%AC%ED%98%84.html

https://codingapple.com/unit/firebase-installation-with-npm/?id=9822

이 두개로 파이어베이스 연동 성공
최신버전 말고 구버전 쓰면 됨 ㅠㅠ-
