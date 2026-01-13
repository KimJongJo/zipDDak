# 집딱

```
집 수리 전문가 매칭, 자재 구매, 공구 대여를 한 곳에서 지원하는
집딱의 프로젝트 레포지토리입니다.

평소 주변에서 집 수리나 시공에 대해 전혀 모르는 사람들이 어디서부터 시작해야 할지 몰라 막막해하는 모습을 자주 보았습니다.
전문적인 분야이다 보니 일반인이 정보를 얻기 어렵고,
특히 전문가를 찾는 일부터 필요한 자재와 고가의 공구를 마련하는 일까지,
모든 과정을 개별적으로 해결해야 하는 불편함이 크다는 사실을 알게되었습니다.

만약 전문가 매칭, 자재 구매, 그리고 공구 대여 까지 이 모든 과정을 한 플랫폼에서 한 번에 해결할 수 있다면,
초보자들도 훨씬 쉽고 편리하게 집을 고칠 수 있을 것 같다는 생각이 들었습니다.

그래서 사용자는 간편하게 견적 요청과 공구 대여를 하고,
전문가와 판매업체는 자유롭게 상품 등록과 상담을 진행할 수 있는 통합 플랫폼 "집딱"을 개발하게 되었습니다.

Kakao Map, Login(Kakao, Google, Naver), Toss Payments API, 스마트택배 API를 사용했습니다.

사용자, 전문가, 판매업체, 사이트관리자라는 액터로 나뉩니다.
사용자 - 공구 대여, 커뮤니티, 자재 구매, 견적요청, 전문가 매칭, 판매업체 입점 신청
전문가 - 견적서 작성, 회원 매칭, 멤버십, 정산, 포트폴리오 작성
판매업체 - 상품 등록, 주문 관리, 반품/교환 관리
사이트관리자 - 회원/전문가/판매업체 관리, 전문가 전환 신청 처리/판매업체 입점 신청 처리, 정산, 통계

인원 : 4명
프로젝트 기간 : 2025/11 ~ 2025/12
맡은 역할 : 회원서비스(커뮤니티/자재구매/장바구니/견적요청)
            사이트 관리자 서비스(회원관리/전문가 전환 신청 처리/업체 입점 신청 처리/이용 내역 관리/정산 관리/통계)
```

---

Table
<img width="1081" height="651" alt="image" src="https://github.com/user-attachments/assets/23e65d6e-6ac4-429b-9ea6-b0c635f7a7b5" />


<details>
<summary>
개발 환경
</summary>

  
| Environment | Detail |
| --- | --- |
| 환경 | Windows |
| 언어 | Java, Javascript, HTML5, CSS3, JavaScript, jQuery, MySQL |
| 프레임워크 / 라이브러리| React, Spring Boot |
| 보안 | Spring Security, JWT |
| 데이터베이스 | JPA(QueryDSL) | 
| 툴 | eclipse, HeidiSQL, Postman, VScode |
| WAS | Apache Tomcat 9.0 |
| API | Kakao Map, Login(Kakao, Google, Naver), Toss Payments, 스마트택배 |
| 협업 | Github, Notion, Draw.io, Figma |

  
</details>

## 메인화면
<img width="1033" height="885" alt="zipddakMain" src="https://github.com/user-attachments/assets/fd03457d-30f4-4b6c-97a1-b03464fc8b4c" />

메인 화면은 통합 검색 기능을 가장 중심에 배치하였습니다. <br>
사용자가 필요한 정보를 찾기 위해 들이는 수고를 줄이고자 전문가, 자재, 공구 등 각 카테고리별 추천 상품을 바로 노출하도록 설계하였습니다. <br>
이를 통해 시공 지식이 부족한 사용자라도 복잡한 과정 없이 쉽고 빠르게 서비스를 탐색할 수 있습니다.

### 견적 요청
<img width="1243" height="887" alt="zipddakRequest" src="https://github.com/user-attachments/assets/a8357888-7868-49d6-a6fb-73b1339880aa" />

수리, 인테리어, 컨설팅 등 각 서비스 유형에 딱 맞는 맞춤형 질문 세트를 구성하였습니다. <br>
특히 사용자가 어렵게 느끼지 않도록 대화형 UI를 도입하여, 질문에 답하다 보면 자연스럽게 상세 견적 요청서가 완성될 수 있도록 기능을 구현하였습니다.

### 장바구니
<img width="1288" height="892" alt="zipddakCart" src="https://github.com/user-attachments/assets/ea7aa6d2-d23b-4711-80d9-0e02d96df7c1" />

사용자의 구매 편의를 위해 브랜드별 상품 자동 분류 로직을 적용하였습니다. <br>
또한 동일한 상품을 중복으로 추가할 경우 수량이 자동으로 합산되도록 처리하였으며, <br>
입점 브랜드별 정책에 따른 배송비가 실시간으로 산출되도록 구현하여 결제 전 정확한 금액 확인이 가능합니다.

### 자재 구매
<img width="1453" height="893" alt="zipddakPayment" src="https://github.com/user-attachments/assets/bbb25f41-47f5-4075-bf0e-af5861c0f05a" />

자재 구매 시 사용자에게 편리한 결제 환경을 제공하고자 Toss Payments API를 연동하였습니다. <br>
이를 통해 카드, 계좌이체 등 다양한 결제 수단을 지원하며, 결제 승인부터 취소에 이르기까지 전체 주문 라이프 사이클을 안정적으로 관리할 수 있도록 시스템을 구축하였습니다.

### 관리자 페이지 - 통계
<img width="1426" height="734" alt="zipddakAdmin" src="https://github.com/user-attachments/assets/870b87ea-4008-48fb-a156-535e9ed730dc" />

관리자 페이지에는 서비스의 성장 지표를 효율적으로 관리할 수 있도록 데이터 시각화 대시보드를 구축하였습니다. <br>
전월 대비 매출 비교와 월별 수익 구조, 그리고 회원 수의 증감 지표를 한눈에 파악할 수 있도록 구성하여 데이터에 기반한 의사결정이 가능하도록 구현하였습니다.


