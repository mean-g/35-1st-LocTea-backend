# 🍵 록차 Loctea (위코드 35기 1차 프로젝트)
- 록차는 오설록 쇼핑몰을 클론 코딩한 프로젝트입니다. 
- 개발에 집중하기 위해 기획, 디자인은 참고하고 기능은 직접 구현하였습니다.
- 기존 오설록 링크 : https://www.osulloc.com/kr/ko

<br>

## 🍵 사이트 선정 이유
- 멤버십으로 운영되는 사이트이므로 회원가입, 로그인, 장바구니 등 유저와 관련된 다양한 기능을 구현해 볼 수 있기 때문입니다.
- 커머스 사이트이므로 장바구니, 상품 구매, 주문 관리 기능을 구현해 볼 수 있기 때문입니다.
- 상품 종류와 카테고리가 상세히 나누어져 있어서 일대다 관계와 다대다 관계의 모델링을 해볼 수 있기 때문입니다.
- 다양한 필터링 기능을 구현하며 django 쿼리에 익숙해질 수 있으리라 생각했기 때문입니다.

<br>

## 🍵 개발 팀원
- 백엔드 3명 : 박정용, 조민지, 조예슬
- 프론트엔드 4명 : 김익현, 류승연, 이금관(PM), 최재홍

<br>

## 🍵 개발 기간
2022.7.18 ~ 7.29(2주)

<br>

## 🍵 백엔드 팀원 역할
- 박정용
   - DB 모델링
   - 장바구니 API
   - 주문배송 API
   
- 조민지 ✨
   - DB 모델링
   - 회원가입 API
   - 로그인 API
   - 로그인 데코레이터 (인가)
   - AWS 배포

- 조예슬
   - DB 모델링
   - 카테고리 API
   - 상품상세/상품목록 API
   - AWS 배포

<br>

## 🍵 DB 모델링
<img width="870" alt="스크린샷 2022-07-29 오후 5 02 46" src="https://user-images.githubusercontent.com/47664802/181713475-dec250ca-5c97-4223-9abf-932c85ef3fef.png">
   
<br>

## 🍵 백엔드 기술 스택
- Back-end : Python, Django, JWT, Bcrypt, Miniconda
- Database : dbdiagram.io, MySQL
- HTTP : Postman
- Common : Trello, Slack, Git & Github

<br>

## 🍵 프로젝트 사이트
- Youtube 시연영상 : https://youtu.be/grWXHlKwkyY
- LocTea 배포 주소 : http://1st-loctea.s3-website.ap-northeast-2.amazonaws.com

![화면_기록_2022-07-29_오후_5_14_33_AdobeExpress](https://user-images.githubusercontent.com/47664802/181719682-634c4dd5-c52c-40db-917d-bc361f809555.gif)
![화면_기록_2022-07-29_오후_5_15_53_AdobeExpress](https://user-images.githubusercontent.com/47664802/181719701-fd74d457-2aa2-492c-abfa-74bec8b78b8d.gif)
![화면_기록_2022-07-29_오후_5_16_20_AdobeExpress](https://user-images.githubusercontent.com/47664802/181719712-d4b14ec7-6c6b-401a-b9df-5b26a6e5052b.gif)
![화면_기록_2022-07-29_오후_5_22_17_AdobeExpress](https://user-images.githubusercontent.com/47664802/181719721-187ef397-7a65-4ac3-be21-c7ac834e7a9c.gif)
![화면_기록_2022-07-29_오후_5_22_42_AdobeExpress](https://user-images.githubusercontent.com/47664802/181719734-c9591829-befe-43c0-86f0-f43d93afc795.gif)
![화면_기록_2022-07-29_오후_5_21_28_AdobeExpress](https://user-images.githubusercontent.com/47664802/181719748-e84ae082-49b0-4af1-be01-0d5d19a86f67.gif)


<br>

## 🍵 API 명세서
https://charmed-skirt-18c.notion.site/API-ad9f438727804f96bec469adebec53cd


## 🍵 트렐로
![화면_기록_2022-07-29_오후_5_10_50_AdobeExpress](https://user-images.githubusercontent.com/47664802/181716089-6fbaf91a-a1e4-499e-9d47-9d6dee41c031.gif)

## 🍵 프로젝트 회고
1)  회원가입 API (/users/signup)
      - 사용자 정보 (name, username, password, email, mobile number, birth day)를 이용한 회원가입 API 구현하였습니다.
      - 다양한 예외 처리를 통해 에러 메시지를 반환하였습니다.
      - JWT와 Bcrypt를 사용해 비밀번호를 암호화하였습니다.
      - 다시 한번 회원가입 API를 구현하면서 해당 코드에 대한 이해도가 높아졌습니다.
      - username 정규식은 사용해 보지 않았는데, 이를 위해 다시한 번 정규식을 공부할 수 있는 시간이었습니다.

2)  로그인 API (/users/login)
      - 사용자 정보 중 일부인 username과 password를 이용해 로그인할 수 있는 API를 구현하였습니다.
      - 로그인 시 사용자에서 token을 발급합니다.
      - 회원가입 API에 등록되지 않은 사용자에 대한 에러와, keyerror를 반환하도록 했습니다.
      - 코드를 작성하면서 암호화와 token 발급에 대한 이해도가 높아졌습니다.
      
3)  로그인 데코레이터 (인가)
      - 토큰을 이용한 로그인 데코레이터를 구현하였습니다.
      - 토큰 검사를 통해 에러를 반환하도록 했습니다.
      - 데코레이터 사용은 처음이라 조금 헤맸지만 큰 문제 없이 구현했습니다.
      - 다음에 또 해당 기능을 구현해 볼 수 있으면 해당 코드에 대한 이해도가 조금 더 높아질 것 같습니다.
      
4)  AWS 배포
      - 배포를 통해 AWS 사용법을 숙지하였습니다.
      - 조금 더 사용해 볼 기회가 필요한 것 같습니다. 시간을 내서 다시 한번 보면 좋을 것 같습니다.
      
5)  느낀 점
      - 초반 업무 분담을 너무 사용자 입장에서 한 것 같아서 아쉽다. 다음번에는 개발자 입장에서 조금 더 섬세한 업무 분담을 해야겠다.
      - 팀 프로젝트는 처음이다 보니, 초반에 팀원 간의 소통이 다소 부족했었다. 그로 인해 페이스를 놓쳐 조금 힘들기도 했지만, 중반부부터 
        소통을 통해 다시 페이스를 찾았다. 또한 API 명세서 작성이나 회의록 작성이 다소 늦어져서 다음 프로젝트에서는 초반부터 팀원들과 
        원활한 소통을 해서 더욱 효율적이고 좋은 결과를 낼 수 있으면 좋겠다.
      - 공부가 부족했던 부분을 알게 되었고, 코드를 돌아보면서 많은 공부를 할 수 있었다. 다음에는 새로운 기능을 구현해 보고 싶다.
