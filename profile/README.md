# 👗 나만의 온라인 가상 피팅룸 TryItOn   

<img width="1478" height="806" alt="image" src="https://github.com/user-attachments/assets/cac9a77a-d731-489f-932e-cdd543e5d073" />  

- ~~배포 URL : https://tio-style.com/~~
- ~~Test ID : tryiton15@gmail.com~~
- ~~Test PW : Test123!~~
> ❗ Notice: 현재 도메인은 사용 불가합니다.

<br>

## 프로젝트 소개   

- 사진을 찍어 나만의 캐릭터를 생성하여 나의 캐릭터에 가상 피팅할 수 있는 서비스입니다.
- (개인화 추천 시스템을 도입하여) 옷 추천부터 결제까지 할 수 있는 이커머스 기능입니다.
- 마음에 드는 착장한 아바타를 스토리로 공유하여 포스트잇 형태의 댓글을 남기며 커뮤니티 기능도 즐길 수 있습니다.

<br>  

## 팀원 구성   

<div align="center">

| **김성광** | **임재홍** | **설현아** | **조윤호** | **이시현** |
| :------: |  :------: | :------: | :------: | :------: |  
| [@badapodo](https://github.com/badapodo) | [@ahpicl64](https://github.com/ahpicl64) | [@hyeona01](https://github.com/hyeona01) | [@Yunkick](https://github.com/Yunkick) |  [@sihyun10](https://github.com/sihyun10) |
| <img src="https://avatars.githubusercontent.com/u/128721477?v=4" width="200"> | <img src="https://avatars.githubusercontent.com/u/183704741?v=4" width="200"> | <img src="https://avatars.githubusercontent.com/u/126868156?v=4" width="200"> | <img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/d9f3ad15-e070-4c1b-97ad-0dad8cb38f11" /> |  <img src="https://avatars.githubusercontent.com/u/92582664?v=4" width="200">  |  

</div>

<br>

## 1. 기술 스택

- Front : Next.js (TypeScript), Zustand, Tailwind CSS, Axios
- Back-end : Spring Boot, JPA / MySQL, JWT, OAuth
- FitDit api 사용
- 버전 및 이슈관리 : Github, Github Issues
- 협업 툴 : Notion
- CI/CD : Git, Github Actions, AWS Codedeploy
- Infra : AWS, RDS(MySQL 8.8), ElastiCache(Redis), Lambda, AWS CloudFront(CDN), AWS Route53(DNS)
- 테스트 / 모니터 : nGrinder, granafa K6, AWS Cloudwatch

<br>  

## 2. 커밋 컨벤션  

| 태그         | 설명                                                    |
|------------|-------------------------------------------------------|
| `feat`     | 새로운 기능 추가                                             |
| `fix`      | 버그 수정                                                 |
| `docs`     | 문서 수정 (README 등)                                      |
| `style`    | 코드 포맷팅, 세미콜론 누락 등 (기능 변경 없음)                          |
| `refactor` | 코드 리팩토링 (기능 변경 없음)                                    |
| `test`     | 테스트 코드 추가 및 리팩토링                                      |
| `chore`    | 빌드 설정, 패키지 매니저 등 기타 변경                                |
| `merge`    | 브랜치 병합 작업 (e.g. `feat/auth` → `develop`), 충돌 해결 포함 |  

<br>  

## 3. 역할 분담  

### 🦭 김성광 (팀장)     

- 의류 착용 모델 적용
- 이미지 처리 병렬화

### 🐻 임재홍  

- CI/CD, 인프라 구축
- DB 설계 및 관리
- 성능 개선 및 테스트

### 🐰 설현아  

- 로그인, OAuth
- 개인화 추천 시스템

### 🐻‍❄️ 조윤호

- socket 통신
- 결제 기능
- 착장 캐싱

### 🐒 이시현  

- UI/UX : 메인 홈 페이지, 아바타 모달, 상품 카드
- 검색 엔진

<br>  

## 4. 개발 기간 

- 전체 개발 기간 : 6/26 ~ 7/23
- 아이디어 선정 : 6/19 ~ 6/25
- MVP 제작 기간 : 6/26 ~ 7/9
- 폴리싱 : 7/10 ~ 7/ 23

<br>  

## 5. 페이지별 기능  

### [초기화면 - 홈]  

- 비로그인 유저 : 첫 페이지에 착장 체험 서비스, 옷 구경, 스토리 구경
- 로그인 유저 : 아바타 착장 (가상피팅), 스토리 작성, 옷장, 장바구니
  - 유저 프로필 정보와 행동을 기반으로 **개인화 추천 알고리즘**이 구현되어있습니다.
  - 나에게 맞는 추천 상품, 내 연령대가 많이 찾는 상품, TIO 인기 상품

<img width="2396" height="872" alt="image" src="https://github.com/user-attachments/assets/a968c5e6-78cb-45b1-a3ef-cfbca19b86c2" />  

<br> 

### [회원가입]  

- 구글 계정 또는 이메일 주소 인증 코드 6자리 입력 후, 가입이 가능합니다.
- 이메일 주소의 형식이 유효하지 않거나 이미 가입된 이메일일 경우 회원가입이 되지 않습니다.
- 비밀번호는 8자 이상으로 영문, 숫자, 특수문자를 포함해야한다.
- 닉네임, 생년월일, 성별, 전화번호, 선호 스타일, 키 몸무게 신발 사이즈를 작성해주어야한다.
- (자신의 아바타를 생성하기 위해) 전신이 잘 보이도록 정면에서 찍은 사진을 업로드해주어야한다.
  - 사진을 업로드하고 싶지 않거나 사진이 없을 경우 다음에 추가하기를 클릭하면 기본 아바타가 생성된다.

| ![이미지1](https://github.com/user-attachments/assets/07613ae8-11f0-40f2-9608-2c86fef5da00) | ![이미지2](https://github.com/user-attachments/assets/4496f8ef-0259-4de0-ae9d-6520b07bcd13) |
|--------------------------|--------------------------|


### [검색기능]  

- 브랜드명과 제품명을 검색 조건으로 하여 검색어 필터링
- 유저가 검색을 하면 자동완성 결과를 최대 6개 띄워줍니다. (제품명 기준)

<img width="2296" height="880" alt="image" src="https://github.com/user-attachments/assets/8b1ce2f9-c763-4171-8452-5a47aac6c64f" />  

<br>  

### [아바타 가상 피팅]  

- 마음에 드는 옷을 발견하면 아바타 아이콘을 눌러 옷을 입힐 수 있습니다.
  - 옷을 다 입게 되면 Desktop에서는 왼쪽 아바타 영역에서 바로 확인할 수 있으며, 알림으로도 알려줍니다.
  - 모바일에서는 알림으로 확인할 수 있습니다.
- 입혀본 옷의 정보(카테고리명, 제품명)가 표시됩니다.
- 유저가 한번 입혀본 옷은 캐싱을 적용하여 나중에 또 입혀보게 되면 빠르게 입혀집니다.
  - 상의 단일 피팅 or 하의 단일 피팅 : 각각 상의 또는 하의 정보로 캐시 키를 부여하여 캐시 이미지를 저장
  - 상의 착용 중, 하의 변경 : 상/하의 정보로 캐시 키 부여하여 캐시 이미지를 저장
  - 하의 착용 중, 상의 변경 : 상/하의 정보로 캐시 키 부여하여 캐시 이미지를 저장


### [옷장]  

- **옷장에 추가** 버튼을 통해 (최대 10개) 저장한 착장들을 볼 수 있습니다.
- **하트(찜하기)** 버튼을 누른 제품들 목록들이 카테고리별로 조회할 수 있습니다.  

<img width="2928" height="1544" alt="image" src="https://github.com/user-attachments/assets/dccb613f-b559-4b17-baa9-9962e9ae9516" />    

<img width="2288" height="960" alt="image" src="https://github.com/user-attachments/assets/51592981-ea93-4ed0-a953-d5bedd7553dc" />

<br>  

### [스토리]  

- 기본적으로 스토리 페이지는 인기순으로 정렬되어있습니다.
- 저장한 착장들 중 마음에 드는 것을 골라 스토리에 작성할 수 있습니다.
  - 배경 제거 기능을 활용하여 제거 후 배경색 선택하여 본인만의 스타일로 스토리를 게시할 수 있습니다.
- 스토리를 구경하며, 그 스토리에 올라온 착장 정보도 확인할 수 있습니다.
- 댓글 작성 기능을 활용하여 붙이고 싶은 위치에 댓글을 남길 수 있습니다.
- **스토리 관리** 기능을 통해, 본인이 올린 스토리를 삭제할 수 있는 기능도 있습니다.

<img width="900" height="400" alt="image" src="https://github.com/user-attachments/assets/db3bbdc4-3afa-4bb9-a1a6-3a4326f61b5e" />

### [결제]  

- 장바구니에 담은 상품들을 구매할 수 있습니다.
- 주문서에 배송지 정보를 설정 후, 결제 방법(토스페이, 네이버페이 등)을 선택해 결제하기를 진행 할 수 있습니다.
  - 현재 테스트 환경이기에 실제로 결제되지는 않습니다.
 
<img width="2536" height="1324" alt="image" src="https://github.com/user-attachments/assets/29085d49-46e1-4f34-81e7-1bd5119f185b" />
