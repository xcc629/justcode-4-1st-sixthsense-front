# 스테이 포레스트

## 오류 안내

현재 카카오 지도 api 키가 다른 개발자분께 있어 설치하여도 실행되지 않는 오류가 있습니다.
해결 중에 있습니다.

## 설치 및 실행 방법
develop 브랜치 혹은 메인 브랜치를 클론 받은 후 
```
npm i 
```
로 패키지를 설치해주세요.

```
npm run start
```
명령어를 실행하면 `localhost:3000`에서 실행됩니다.

## 1. Introduce

- 스테이폴리오 클론코딩 프로젝트

> 클론코딩: 개발에만 집중할 수 있도록 기존 웹의 기획과 디자인을 참고하여 하나의 사이트를 완성해보는 프로젝트

- [프론트 깃헙](https://github.com/wecode-bootcamp-korea/justcode-4-1st-sixthsense-front)
- [백 깃헙](https://github.com/wecode-bootcamp-korea/justcode-4-1st-sixthsense-back)

<br>

## 2. 개발 기간 및 인원

- 개발 기간: 2022/03/28 ~ 2022/04/08 (2주)
- 개발 인원: Fullstack 5명( [김수빈](https://velog.io/@shorrysorry), [유다송](https://velog.io/@sonaki0811), [이정민](https://velog.io/@jml22), [임근홍](https://velog.io/@xcc629), [전하은](https://velog.io/@hani2525))

<br>

## 3. DEMO

<br>

- 프론트

---

<br>

[![스테이포레스트 데모](https://img.youtube.com/vi/WkTQ5fGVEXw/0.jpg)](https://www.youtube.com/watch?v=WkTQ5fGVEXw&feature=youtu.be)

- 이미지 클릭시 스테이포레스트 시연 영상을 보실 수 있습니다.

<br>

- 백엔드

---

[식스센스 백엔드 API 문서](https://documenter.getpostman.com/view/20004181/Uyr4Lfof)

<br>

## 4. TECH

- Front-End: React, React hook, React-Router-Dom, Sass,
- Back-End: Express, Prisma, Mysql
- 라이브러리: React-icons, moment.js

<br>

## 5. 구현 기능

<br>

### [프론트엔드]

<br>

#### 메인 페이지

---

- Modal - 뒷페이지 스크롤 방지 기능 구현.
- 언제떠날까요 Modal - moment.js를 활용한 커스텀 캘린더 제작.
- 슬라이드 Big / Medium / Small - 페이지가 무한정 넘어갈 수 있게 기능 구현.

<br>

#### 리스트 페이지

---

- 인원, 가격범위, 카테고리로 숙소 선택 기능 구현
- 리셋 버튼으로 선택한 내용들 초기화 기능 구현
- 각 방 선택 시 디테일 페이지로 이동

<br>

### 상세 페이지

---

- 숙소 사진 슬라이드
- 객실 사진 슬라이드
- 좋아요 UI
- 숙소 정보 API로 받아와 화면에 출력
  → 숙소 설명 | 숙소의 특징 | 숙소 근처 명소
- 지도 API
- FAQ

<br>

### 회원가입 및 로그인

---

- 회원가입 - 정규식 표현을 통한 회원정보 유효성 검사 기능 및 체크박스 all 체크 기능 구현
- 로그인 - 정규식 표현을 이용한 유효성 검사

<br>
<br>

### [백엔드]

<br>

### API 공통 & 패턴 및 테이블 설계

---

- [dbdiagram.io](http://dbdiagram.Id) 사이트 이용하여 관계형으로 테이블 설계.
- prisma를 사용하여 schema.prisma의 테이블 작성 후 migration.
- layered patten 적용해 controller, service, model로 구분.
- DB의 자원을 기준으로 users, dormitories, rooms로 URI 구분.

<br>

### GET dormitories , GET dormitories/images, GET dormitories/cities, GET rooms/images

---

- GET method로 숙소 전체 리스트, 이미지 전체, city 전체, 방 이미지 전체 가져오는 API 작성.
- statusCode: 서버문제(500) / Ok(200).
- model단에서 쿼리문 작성하여 service, controller로 차례대로 넘김.

<br>

### POST users/login , POST users/signup, Authorization Middleware

---

- Layerd Pattern으로 기능 분리
- Post method를 통해 필요한 값을 전달받아 회원가입 혹은 로그인을 하는 API 작성.
- login의 경우 해당 id에 대한 token이 발행되고, 로그인이 필요한 작업 실행 시, Authorization 미들웨어를 통해 유효한 토큰인지 인증인가를 거쳐서 실행됨.
- statusCode: 서버문제(500) / Ok(200) / Created(201)

<br>
<br>

---

---

<br>

- _이 프로젝트는 스테이폴리오 사이트를 참조하여 학습목적으로 만들었습니다._
- _실무수준의 프로젝트이지만 학습용으로 만들었기 때문에 이 코드를 활용하여 이득을 취하거나 무단 배포할 경우 법적으로 문제될 수 있습니다._
- _이 프로젝트에서 사용하고 있는 모든 이미지들은 무료 이미지 및 자가제작 이미지들입니다._
