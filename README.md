# PPE Facility Management System

가스 측정기/분석기 전문 전자상거래 플랫폼

## 📋 프로젝트 소개

PPE Facility Management System은 가스 측정기와 분석기를 전문으로 하는 전자상거래 플랫폼입니다. 구매자와 판매자를 연결하는 B2B/B2C 통합 시스템으로, 화학물질 기반의 정확한 제품 분류 및 검색 시스템을 제공하며, 현금 및 포인트 결제 시스템을 지원합니다.

## 🚀 주요 기능

### 🏠 메인 페이지 ✅
- **모던한 랜딩 페이지**: 글래스모피즘 디자인과 부드러운 애니메이션
- **반응형 네비게이션**: 스크롤 시 배경 변화 및 블러 효과
- **히어로 섹션**: 그라데이션 배경과 강력한 CTA 버튼
- **서비스 소개**: 가스측정기/분석기 전문 서비스 하이라이트
- **회사 소개**: 블루시스템의 전문성과 신뢰성 강조
- **연락처 정보**: 지도, 주소, 연락처 등 상세 정보
- **푸터**: 회사 정보 및 링크 모음

### 👤 구매자 기능 ✅
- **고급 필터링 시스템**: 화학물질, 상태, 제품유형, 용도, 측정방식 등 다차원 검색
- **제품 상세 페이지**: 이미지, 가격, 포인트, 연관 화학물질 표시
- **장바구니 관리**: 수량 관리, 장바구니 추가/삭제, 선택/전체 상품 관리
- **구매 시스템**: 현금 결제 및 포인트 결제 지원
  - 포인트 환율: 100포인트 = 100,000원, 230포인트 = 200,000원
  - 선택 상품/전체 상품 구매 지원
- **주문 관리**: 주문 생성, 주문 목록 조회, 주문 상세보기, 주문 취소
- **포인트 시스템**: 포인트 조회, 포인트 사용 내역 (기본 구현 완료)
- **문의/리뷰 시스템**: 제품별 Q&A, 리뷰 작성/수정/삭제, 도움됨 카운트
- **견적 요청**: 제품별 견적 요청, 다중 상품 견적 요청, 견적 상태 관리
- **검교정 서비스**: 장비 검교정 요청, 진행상황 관리, 수정/삭제
- **회원 정보**: 프로필 페이지, 구매 내역, 리뷰 내역, 포인트 정보

### 🏪 판매자 기능 ✅
- **제품 등록**: 카테고리, 화학물질, 가격 등 상세 정보 입력
- **제품 수정**: 기존 제품 정보 업데이트
- **제품 관리**: 판매자별 제품 목록 관리
  - **카테고리 필터링**: 가스 측정기, 가스 분석기 등 카테고리별 상품 분류
  - **검색 기능**: 상품명, 모델명, 카테고리별 검색
  - **가격대 필터링**: 100만원 미만, 100만원~500만원, 500만원 이상
- **주문 관리**: 주문 접수, 주문 확인, 배송 처리 (기본 구현 완료)
- **대시보드**: 판매자 전용 대시보드
- **견적 관리**: 견적 요청 관리 페이지

### 👨‍💼 관리자 기능 ✅
- **통계 대시보드**: 전체 상품 수, 주문 수, 사용자 포인트 현황, 매출 통계
- **전체 상품 관리**: 모든 상품 조회, 수정, 삭제, 등록
- **주문 관리**: 전체 주문 현황, 상세 정보, 상태 변경, 페이징 처리
- **사용자 포인트 관리**: 세션별 포인트 잔액 및 사용 내역 관리
- **검색 및 필터링**: 상품명, 모델명, 카테고리별 검색
- **페이징 시스템**: 대량 데이터의 효율적인 페이지 처리
- **주문량 TOP 5**: 인기 상품 분석 및 통계
- **가격대별 상품 분석**: 저가/중가/고가 상품 분류 및 관리

## 🔧 최근 해결된 문제

### 판매자 상품관리 카테고리 필터링 문제
- **문제**: '가스측정기' 카테고리 선택 시 상품이 표시되지 않음
- **원인**: HTML 옵션 값과 데이터베이스 카테고리 값 불일치 (공백 차이)
- **해결**: 카테고리 필터 옵션을 '가스 측정기', '가스 분석기'로 통일하고 컨트롤러 로직 개선

### 연락처 페이지 애니메이션 문제
- **문제**: '연락처' 제목이 잠깐 보였다가 사라짐
- **원인**: CSS 애니메이션과 JavaScript 로직 충돌로 인한 요소 숨김
- **해결**: 히어로 섹션 요소들의 즉시 표시 로직 추가 및 CSS 우선순위 조정

## 🚧 추가 구현 예정 기능

### 🔐 인증 및 권한 관리
- **사용자 회원가입/로그인 시스템**: JWT 기반 인증 시스템
- **역할 기반 접근 제어**: 구매자, 판매자, 관리자 권한 분리
- **세션 관리 개선**: 현재 session_id 기반에서 실제 사용자 계정 기반으로 전환
- **비밀번호 암호화**: BCrypt를 사용한 안전한 비밀번호 저장
- **이메일 인증**: 회원가입 시 이메일 인증 시스템

### 💰 포인트 시스템 완성
- **포인트 적립 내역**: 상품 구매 시 포인트 적립 로그
- **포인트 사용 내역**: 포인트 사용 기록 및 잔액 관리
- **포인트 환급 시스템**: 포인트를 현금으로 환급하는 기능
- **포인트 만료 관리**: 포인트 유효기간 설정 및 만료 처리
- **포인트 이벤트**: 특정 상품 구매 시 추가 포인트 적립

### 🛒 고급 주문 관리
- **주문 상태 실시간 업데이트**: WebSocket을 통한 실시간 주문 상태 알림
- **배송 추적 시스템**: 택배사 API 연동을 통한 배송 추적
- **주문 취소/환불 처리**: 주문 취소 및 환불 프로세스 자동화
- **재고 관리**: 상품 재고 수량 관리 및 품절 처리
- **주문 알림**: 이메일/SMS를 통한 주문 상태 변경 알림

### 📊 고급 분석 및 통계
- **판매자 대시보드**: 판매자별 매출, 주문 현황, 인기 상품 분석
- **구매자 구매 패턴 분석**: 구매 이력 기반 추천 시스템
- **재고 최적화**: ABC 분석을 통한 재고 관리 최적화
- **수익성 분석**: 상품별 수익성 및 마진 분석
- **고객 세분화**: 구매 행동 기반 고객 분류

### 🔍 고급 검색 및 필터링
- **AI 기반 상품 추천**: 구매 이력 및 관심사 기반 상품 추천
- **자동완성 검색**: Elasticsearch를 활용한 실시간 검색 제안
- **가격 비교 기능**: 유사 상품 간 가격 비교
- **상품 비교**: 여러 상품을 동시에 비교하는 기능
- **저장된 검색**: 자주 사용하는 검색 조건 저장

### 📱 모바일 최적화
- **반응형 디자인 개선**: 모바일/태블릿 최적화
- **PWA (Progressive Web App)**: 오프라인 사용 가능한 웹앱
- **모바일 푸시 알림**: 주문 상태 변경 시 모바일 알림
- **터치 제스처**: 모바일 친화적인 인터랙션

### 🔧 시스템 개선
- **API 문서화**: Swagger/OpenAPI를 활용한 API 문서 자동 생성
- **로깅 시스템**: 구조화된 로그 관리 및 모니터링
- **캐싱 시스템**: Redis를 활용한 성능 최적화
- **파일 업로드**: 이미지 압축 및 CDN 연동
- **백업 시스템**: 자동 데이터 백업 및 복구

### 🌐 외부 서비스 연동
- **결제 시스템**: PG사 연동 (토스페이먼츠, 카카오페이 등)
- **택배사 API**: CJ대한통운, 한진택배 등 배송 추적 연동
- **이메일 서비스**: SendGrid, AWS SES를 활용한 이메일 발송
- **SMS 서비스**: 알림톡 및 SMS 발송 서비스
- **지도 서비스**: 배송지 검색 및 지도 표시

### 🔒 보안 강화
- **HTTPS 강제**: SSL/TLS 인증서 적용
- **CSRF 보호**: Cross-Site Request Forgery 방지
- **XSS 방지**: Cross-Site Scripting 공격 방지
- **SQL Injection 방지**: Prepared Statement 강화
- **Rate Limiting**: API 호출 제한으로 DDoS 방지

### 📈 성능 최적화
- **데이터베이스 최적화**: 인덱스 최적화 및 쿼리 성능 개선
- **이미지 최적화**: WebP 포맷 지원 및 지연 로딩
- **CDN 연동**: 정적 자원 CDN 배포
- **데이터베이스 샤딩**: 대용량 데이터 처리 최적화
- **캐시 전략**: 다층 캐시 시스템 구축

## 🛠️ 기술 스택

### Backend ✅
- **Spring Boot 3.x** - 웹 애플리케이션 프레임워크
- **Java 17** - LTS 버전으로 안정성과 최신 언어 기능 활용
- **Spring MVC** - 웹 계층 (REST API + View Controller)
- **Spring Data JPA** - 데이터 접근 계층
- **Hibernate** - ORM 프레임워크
- **Thymeleaf** - 서버 사이드 템플릿 엔진
- **Spring Security** - 보안 프레임워크 (기본 설정)

### Frontend ✅
- **HTML5/CSS3** - 마크업 및 스타일링
- **JavaScript (ES6+)** - 클라이언트 사이드 로직
- **Fetch API** - HTTP 요청 처리
- **DOM Manipulation** - 동적 UI 업데이트
- **Responsive Design** - 반응형 웹 디자인
- **CSS Grid & Flexbox** - 레이아웃 시스템

### Database ✅
- **MySQL 8.0** - 관계형 데이터베이스
- **JPA/Hibernate** - ORM 매핑
- **데이터베이스 스키마**: 34개 테이블 (Product, Order, User, Chemical 등)
- **관계형 설계**: 다대다, 일대다, 일대일 관계 구현

### Build & Development Tools ✅
- **Maven 3.8+** - 의존성 관리 및 빌드 자동화
- **Lombok** - 보일러플레이트 코드 제거
- **Spring Boot DevTools** - 개발 시 자동 재시작 및 라이브 리로드
- **Git** - 버전 관리 시스템

## 🏗️ 프로젝트 구조

### 📁 디렉토리 구조
```
src/main/java/com/ppe/facility/
├── controller/          # 웹 컨트롤러 (12개)
│   ├── MainController.java
│   ├── ProductController.java
│   ├── OrderController.java
│   ├── CartController.java
│   ├── QnaController.java
│   ├── ReviewController.java
│   ├── QuoteController.java
│   ├── CalibrationController.java
│   ├── AdminController.java
│   ├── SellerProductController.java
│   ├── SellerOrderController.java
│   └── ChemicalController.java
├── entity/             # JPA 엔티티 (15개)
│   ├── Product.java
│   ├── Order.java
│   ├── Chemical.java
│   ├── Review.java
│   ├── Qna.java
│   └── ...
├── service/            # 비즈니스 로직 (8개)
├── repository/         # 데이터 접근 계층 (8개)
└── util/              # 유틸리티 클래스

src/main/resources/
├── templates/          # Thymeleaf 템플릿 (30+ 개)
│   ├── main.html
│   ├── user_buyer/    # 구매자 페이지
│   ├── user_seller/   # 판매자 페이지
│   └── admin/         # 관리자 페이지
├── static/            # 정적 자원
│   ├── css/           # 스타일시트 (15개)
│   └── js/            # JavaScript (12개)
└── application.yml    # 설정 파일
```

### 🗄️ 데이터베이스 스키마
- **총 34개 테이블**: Product, Order, Chemical, Review, QnA, Quote, Cart 등
- **관계형 설계**: 다대다(Product-Chemical), 일대다(Order-OrderItem), 일대일(Order-Delivery)
- **ERD 문서**: `database_erd.md` 참조

### 🔌 API 명세서
- **총 76개 API 엔드포인트** 구현
- **REST API**: JSON 응답 지원
- **API 문서**: `PPE_Facility_API_Specification.csv` 참조

## 📊 현재 구현 상태

### ✅ 완료된 기능 (90%)
- **메인 페이지**: 랜딩 페이지, 네비게이션, 서비스 소개
- **구매자 기능**: 제품 검색/필터링, 장바구니, 주문, 리뷰, Q&A, 견적, 검교정
- **판매자 기능**: 제품 등록/수정/관리, 주문 관리, 대시보드
- **관리자 기능**: 통계 대시보드, 상품/주문/포인트 관리, 페이징
- **데이터베이스**: 34개 테이블, 관계형 설계, ERD 문서화
- **API**: 76개 엔드포인트, REST API 지원

### 🔄 부분 구현 (10%)
- **포인트 시스템**: 기본 포인트 조회/사용, 상세 내역 관리 필요
- **배송 관리**: 기본 주문 상태 관리, 실제 배송 추적 시스템 필요
- **사용자 인증**: 세션 기반, 실제 로그인 시스템 필요

### 📈 프로젝트 통계
- **총 파일 수**: 100+ 개
- **Java 클래스**: 50+ 개
- **HTML 템플릿**: 30+ 개
- **CSS 파일**: 15개
- **JavaScript 파일**: 12개
- **API 엔드포인트**: 76개
- **데이터베이스 테이블**: 34개

## 📦 설치 및 실행

### 필수 요구사항
- Java 17 이상
- Maven 3.6 이상
- IDE (IntelliJ IDEA, Eclipse, VS Code 등)

### 1. 프로젝트 클론
```bash
git clone [repository-url]
cd ppe_facility/ppe
```

### 2. 의존성 설치 및 빌드
```bash
# 의존성 설치 및 빌드
mvn clean install

# 애플리케이션 실행
mvn spring-boot:run
```

### 3. 접속 정보
- **메인 페이지**: http://localhost:9000
- **관리자 대시보드**: http://localhost:9000/admin
- **H2 콘솔**: http://localhost:9000/h2-console

### 4. 주요 페이지 접속
- **🏠 메인 페이지**: http://localhost:9000
- **🏠 회사 소개**: http://localhost:9000/about
- **🏠 서비스 안내**: http://localhost:9000/services
- **🏠 연락처**: http://localhost:9000/contact
- **구매자 페이지**: http://localhost:9000/user-buyer/products
- **판매자 페이지**: http://localhost:9000/user-seller/products
- **장바구니**: http://localhost:9000/user-buyer/cart
- **주문 관리**: http://localhost:9000/order/my-orders
- **관리자 대시보드**: http://localhost:9000/admin
- **관리자 상품 관리**: http://localhost:9000/admin/products
- **관리자 주문 관리**: http://localhost:9000/admin/orders
- **관리자 포인트 관리**: http://localhost:9000/admin/user-points

## 🏗️ 프로젝트 구조

```
ppe/
├── src/main/java/com/ppe/facility/
│   ├── Ppe1Application.java        # 메인 애플리케이션 클래스
│   ├── controller/                 # REST API 컨트롤러
│   │   ├── ProductController.java
│   │   ├── CartController.java
│   │   ├── OrderController.java
│   │   ├── SellerOrderController.java
│   │   ├── SellerProductController.java
│   │   ├── QnaController.java
│   │   ├── ReviewController.java
│   │   ├── QuoteController.java
│   │   ├── CalibrationController.java
│   │   ├── ChemicalController.java
│   │   └── AdminController.java    # 관리자 기능 컨트롤러
│   ├── service/                    # 비즈니스 로직
│   │   ├── ProductService.java
│   │   ├── CartService.java
│   │   ├── OrderService.java
│   │   ├── UserPointsService.java
│   │   ├── QnaService.java
│   │   ├── ReviewService.java
│   │   ├── QuoteRequestService.java
│   │   └── CalibrationService.java
│   ├── repository/                 # 데이터 접근 계층
│   │   ├── ProductRepository.java
│   │   ├── CartRepository.java
│   │   ├── OrderRepository.java
│   │   ├── OrderItemRepository.java
│   │   ├── UserPointsRepository.java
│   │   ├── QnaRepository.java
│   │   ├── ReviewRepository.java
│   │   ├── QuoteRequestRepository.java
│   │   └── CalibrationRequestRepository.java
│   ├── entity/                     # 도메인 모델
│   │   ├── Product.java
│   │   ├── Chemical.java
│   │   ├── Cart.java
│   │   ├── CartItem.java
│   │   ├── Order.java
│   │   ├── OrderItem.java
│   │   ├── UserPoints.java
│   │   ├── PaymentMethod.java
│   │   ├── OrderStatus.java
│   │   ├── Qna.java
│   │   ├── Review.java
│   │   ├── QuoteRequest.java
│   │   ├── QuoteStatus.java
│   │   ├── CalibrationRequest.java
│   │   ├── CalibrationStatus.java
│   │   ├── Delivery.java
│   │   ├── DeliveryStatus.java
│   │   ├── ShippingCompany.java
│   │   ├── ProductType.java
│   │   ├── ChemicalState.java
│   │   ├── UsageType.java
│   │   ├── MeasureType.java
│   │   └── SingleOrMulti.java
│   └── util/                       # 유틸리티
│       └── PointConverter.java
├── src/main/resources/
│   ├── templates/                  # Thymeleaf 템플릿
│   │   ├── main.html           # 메인 랜딩 페이지
│   │   ├── about.html          # 회사 소개 페이지
│   │   ├── services.html       # 서비스 안내 페이지
│   │   ├── contact.html        # 연락처 페이지
│   │   ├── user_buyer/            # 구매자 페이지
│   │   │   ├── cart.html
│   │   │   ├── order_form.html
│   │   │   ├── order_detail.html
│   │   │   ├── order_complete.html
│   │   │   ├── my_orders.html
│   │   │   ├── product_list.html
│   │   │   ├── product_detail.html
│   │   │   ├── review_write_form.html
│   │   │   ├── review_edit_form.html
│   │   │   ├── my_reviews.html
│   │   │   ├── qna_write_form.html
│   │   │   ├── my_qnas.html
│   │   │   ├── quote_request_form.html
│   │   │   ├── multiple_quote_request_form.html
│   │   │   ├── selected_quote_request_form.html
│   │   │   ├── my_quote_requests.html
│   │   │   ├── calibration_request_form.html
│   │   │   ├── my_calibration_requests.html
│   │   │   └── login.html
│   │   ├── user_seller/           # 판매자 페이지
│   │   │   ├── product_list.html
│   │   │   ├── product_detail.html
│   │   │   ├── product_register_form.html
│   │   │   ├── product_edit_form.html
│   │   │   ├── order_list.html
│   │   │   └── order_detail.html
│   │   └── admin/              # 관리자 페이지
│   │       ├── dashboard.html     # 관리자 대시보드
│   │       ├── product_list.html  # 상품 관리 목록
│   │       ├── product_detail.html # 상품 상세 정보
│   │       ├── product_edit_form.html # 상품 수정 폼
│   │       ├── order_list.html    # 주문 관리 목록
│   │       ├── order_detail.html  # 주문 상세 정보
│   │       └── user_points_list.html # 사용자 포인트 관리
│   ├── static/                    # 정적 리소스
│   │   ├── css/                  # 스타일시트
│   │   │   ├── buyer.css
│   │   │   ├── seller.css
│   │   │   ├── cart.css
│   │   │   ├── order.css
│   │   │   └── admin.css      # 관리자 페이지 스타일
│   │   └── js/                   # JavaScript
│   │       ├── cart.js
│   │       ├── product.js
│   │       ├── order.js
│   │       └── admin.js       # 관리자 페이지 스크립트
│   ├── application.yml            # 설정 파일
│   ├── product_schema.sql         # 제품 스키마
│   ├── product_schema_new.sql     # 새로운 제품 스키마
│   ├── product_chemical_example.sql # 제품-화학물질 예제 데이터
│   ├── chemical_migration.sql     # 화학물질 마이그레이션
│   └── add_final_amount_column.sql # 최종 금액 컬럼 추가
└── docs/                          # 프로젝트 문서
    ├── portfolio-guide.md
    ├── detailed-portfolio-guide.md
    └── product-category-guide.md
```

## 🎯 핵심 기능 상세 설명

### 1. 화학물질 관리 시스템

#### 특징
- **동적 카테고리 분류**: 화학물질 상태(기체/액체/고체)에 따른 자동 UI 변경
- **실시간 API 연동**: 서버에서 화학물질 데이터 실시간 로드
- **상태 기반 제품 분류**: 화학물질 상태에 따른 제품 타입 자동 설정

#### 화학물질 선택 방식
1. **알파벳 순**: A-Z 알파벳별로 화학물질 그룹화
2. **자주 사용**: 업계에서 자주 사용되는 화학물질 우선 표시
3. **상태 선택**: 기체/액체/고체 상태별 필터링

#### 제품 분류 로직
- **기체 제품**: 가스 측정기/분석기, DETECTOR/ANALYZER 타입
- **액체/고체 제품**: 실험실용(LAB)/현장분석용(FIELD) 용도

### 2. 화학물질 기반 제품 분류 시스템
화학물질과 제품의 정확한 매칭을 위한 고급 분류 시스템입니다.

#### 핵심 SQL 쿼리
```sql
-- 화학물질 기반 제품 검색의 핵심 쿼리
SELECT p.* FROM product p 
JOIN product_chemical pc ON p.seq = pc.product_seq 
JOIN chemical c ON pc.chemical_id = c.id 
WHERE (:productType IS NULL OR p.product_type = :productType) 
  AND c.name IN (:chemicalNames) 
  AND (:states IS NULL OR c.state IN (:states))
GROUP BY p.seq 
HAVING COUNT(DISTINCT c.name) = :chemicalCount
```

#### 지원하는 필터링 옵션
- **화학물질명**: 다중 선택 가능한 화학물질 기반 검색
- **화학물질 상태**: 기체, 액체/고체 상태별 필터링
- **제품 유형**: 측정기, 분석기 등 제품 카테고리
- **용도**: 산업용, 실험실용 등 사용 목적
- **측정 방식**: 단일/다중 측정 방식
- **키워드 검색**: 제품명, 모델명 등 텍스트 검색

### 2. 스마트 장바구니 시스템
세션 기반의 장바구니 관리 시스템으로 수량 조정, 상품 선택/삭제 기능을 제공합니다.

#### 주요 기능
- **세션 기반 관리**: 로그인 없이도 세션으로 장바구니 유지
- **실시간 수량 조정**: AJAX를 통한 비동기 수량 변경
- **개별 상품 삭제**: 선택한 상품만 장바구니에서 제거
- **전체 상품 관리**: 전체 선택/해제 기능

#### AJAX 기반 실시간 업데이트
```java
@PostMapping("/update-quantity")
@ResponseBody
public ResponseEntity<Map<String, Object>> updateQuantity(
    @RequestParam Long cartItemId,
    @RequestParam Integer quantity,
    HttpSession session) {
    try {
        cartService.updateCartItemQuantity(cartItemId, quantity);
        int totalPrice = cartService.calculateTotalPrice(session.getId());
        
        Map<String, Object> response = new HashMap<>();
        response.put("success", true);
        response.put("totalPrice", totalPrice);
        response.put("message", "수량이 업데이트되었습니다.");
        
        return ResponseEntity.ok(response);
    } catch (Exception e) {
        return ResponseEntity.badRequest()
            .body(Map.of("success", false, "message", e.getMessage()));
    }
}
```

### 3. 이중 결제 시스템 (현금 + 포인트)
현금과 포인트를 모두 지원하는 완전한 결제 시스템을 구현했습니다.

#### 포인트 변환 시스템
```java
@Component
public class PointConverter {
    private static final double POINT_TO_WON_RATIO = 1000.0; // 1포인트 = 1,000원
    
    public static int pointsToWon(int points) {
        return (int) (points * POINT_TO_WON_RATIO);
    }
    
    public static int wonToPoints(int won) {
        return (int) Math.ceil(won / POINT_TO_WON_RATIO);
    }
    
    // 포인트 할인율 계산
    public static int calculateDiscountPoints(int totalAmount) {
        if (totalAmount >= 200000) {
            return 230; // 200,000원 이상 시 230포인트 할인
        } else if (totalAmount >= 100000) {
            return 100; // 100,000원 이상 시 100포인트 할인
        }
        return 0;
    }
}
```

#### 결제 처리 로직
```java
// 현금 결제 처리
@PostMapping("/cash")
public String processCashOrder(@RequestParam String buyerName,
                             @RequestParam String buyerEmail,
                             @RequestParam String buyerPhone,
                             @RequestParam String shippingAddress,
                             HttpSession session) {
    String sessionId = session.getId();
    
    // 1. 장바구니 유효성 검증
    List<CartItem> cartItems = cartService.getCartItems(sessionId);
    if (cartItems.isEmpty()) {
        throw new IllegalStateException("장바구니가 비어있습니다.");
    }
    
    // 2. 주문 생성
    Order order = orderService.createCashOrder(sessionId, buyerName, 
                                             buyerEmail, buyerPhone, shippingAddress);
    
    // 3. 장바구니 비우기
    cartService.clearCart(sessionId);
    
    // 4. 주문 완료 페이지로 리다이렉트
    return "redirect:/order/complete/" + order.getOrderNumber();
}
```

### 4. 완전한 주문 관리 시스템
주문 생성부터 배송까지 전체 주문 생명주기를 관리합니다.

#### 주문 생성 및 관리
```java
@Service
@Transactional
public class OrderService {
    
    public Order createCashOrder(String sessionId, String buyerName, 
                               String buyerEmail, String buyerPhone, String shippingAddress) {
        // 1. 장바구니 아이템 조회
        List<CartItem> cartItems = cartRepository.findBySessionId(sessionId);
        if (cartItems.isEmpty()) {
            throw new IllegalStateException("장바구니가 비어있습니다.");
        }
        
        // 2. 주문번호 생성 (고유성 보장)
        String orderNumber = generateUniqueOrderNumber();
        
        // 3. 주문 엔티티 생성
        Order order = Order.builder()
            .orderNumber(orderNumber)
            .sessionId(sessionId)
            .buyerName(buyerName)
            .buyerEmail(buyerEmail)
            .buyerPhone(buyerPhone)
            .shippingAddress(shippingAddress)
            .totalAmount(calculateTotalAmount(cartItems))
            .paymentMethod(PaymentMethod.CASH)
            .orderStatus(OrderStatus.PENDING)
            .build();
        
        // 4. 주문 아이템 생성
        List<OrderItem> orderItems = cartItems.stream()
            .map(cartItem -> createOrderItem(order, cartItem))
            .collect(Collectors.toList());
        
        order.setOrderItems(orderItems);
        
        // 5. 주문 저장
        Order savedOrder = orderRepository.save(order);
        
        return savedOrder;
    }
    
    private String generateUniqueOrderNumber() {
        String timestamp = LocalDateTime.now().format(DateTimeFormatter.ofPattern("yyyyMMddHHmmss"));
        String randomSuffix = String.format("%04d", new Random().nextInt(10000));
        return "PPE" + timestamp + randomSuffix;
    }
}
```

#### 주문 상태 관리 시스템
- **PENDING**: 주문 접수
- **CONFIRMED**: 주문 확인
- **PROCESSING**: 처리 중
- **SHIPPED**: 배송 중
- **DELIVERED**: 배송 완료
- **CANCELLED**: 주문 취소
- **REFUNDED**: 환불 완료

### 5. 관리자 시스템
전체 쇼핑몰을 관리하는 종합 관리자 시스템으로, 상품, 주문, 사용자 포인트를 체계적으로 관리합니다.

#### 관리자 대시보드 시스템
```java
@Controller
@RequestMapping("/admin")
public class AdminController {
    
    @GetMapping // Admin Dashboard
    public String dashboard(Model model) {
        // 전체 통계 정보 조회
        long totalProducts = productService.getTotalProductCount();
        long totalOrders = orderService.getTotalOrderCount();
        long totalUserPoints = userPointsService.getTotalUserPointsCount();
        
        // 최근 등록된 상품 (최근 5개)
        List<Product> recentProducts = productService.getRecentProducts(5);
        
        // 최근 주문 (최근 5개)
        List<Order> recentOrders = orderService.getRecentOrders(5);
        
        model.addAttribute("totalProducts", totalProducts);
        model.addAttribute("totalOrders", totalOrders);
        model.addAttribute("totalUserPoints", totalUserPoints);
        model.addAttribute("recentProducts", recentProducts);
        model.addAttribute("recentOrders", recentOrders);
        
        return "admin/dashboard";
    }
}
```

#### 상품 관리 시스템
```java
// 상품 관리 기능
@GetMapping("/products")
public String productList(Model model,
                        @RequestParam(defaultValue = "1") int page,
                        @RequestParam(defaultValue = "20") int size,
                        @RequestParam(required = false) String search,
                        @RequestParam(required = false) String category) {
    
    var productPage = productService.getAllProductsWithPaging(page - 1, size, search, category);
    
    model.addAttribute("products", productPage.getContent());
    model.addAttribute("currentPage", page);
    model.addAttribute("totalPages", productPage.getTotalPages());
    model.addAttribute("totalElements", productPage.getTotalElements());
    model.addAttribute("search", search);
    model.addAttribute("category", category);
    
    return "admin/product_list";
}

// 상품 수정 기능
@PostMapping("/products/{productSeq}/edit")
public String productEdit(@PathVariable Integer productSeq,
                        @ModelAttribute Product product,
                        RedirectAttributes redirectAttributes) {
    try {
        productService.updateProduct(productSeq, product);
        redirectAttributes.addFlashAttribute("success", "상품이 성공적으로 수정되었습니다.");
    } catch (Exception e) {
        redirectAttributes.addFlashAttribute("error", "상품 수정 중 오류가 발생했습니다: " + e.getMessage());
    }
    return "redirect:/admin/products/" + productSeq + "/edit";
}
```

#### 관리자 시스템 특징
- **통합 대시보드**: 전체 시스템 현황을 한눈에 파악
- **상품 생명주기 관리**: 등록부터 삭제까지 전체 상품 관리
- **주문 현황 모니터링**: 실시간 주문 상태 및 진행상황 추적
- **포인트 시스템 관리**: 사용자별 포인트 잔액 및 사용 내역 관리
- **검색 및 필터링**: 효율적인 데이터 검색 및 분류
- **페이징 시스템**: 대량 데이터의 효율적인 페이지 처리
- **권한 관리**: 관리자 전용 기능으로 시스템 보안 강화

## 📊 데이터베이스 스키마

### 핵심 테이블 구조

#### 1. 제품 관련 테이블
- **product**: 제품 기본 정보 (카테고리, 유형, 가격, 이미지 등)
- **chemical**: 화학물질 정보 (이름, 알파벳, 상태, 분자식 등)
- **product_chemical**: 제품-화학물질 관계 테이블 (다대다 관계)

#### 2. 거래 관련 테이블
- **cart**: 장바구니 정보 (세션별 관리)
- **cart_item**: 장바구니 아이템 (제품, 수량, 가격)
- **orders**: 주문 정보 (주문번호, 구매자 정보, 결제 방법)
- **order_items**: 주문 아이템 (제품, 수량, 단가, 총액)
- **user_points**: 사용자 포인트 정보 (세션별 포인트 관리)

#### 3. 커뮬니케이션 테이블
- **qna**: 제품 문의 (질문, 답변, 상태)
- **review**: 제품 리뷰 (평점, 제목, 내용, 이미지)
- **quote_request**: 견적 요청 (회사 정보, 수량, 메시지)
- **calibration_request**: 검교정 요청 (장비 정보, 요청 내용)

### 주문 관련 테이블 구조
```sql
-- 주문 테이블
CREATE TABLE orders (
    id BIGINT PRIMARY KEY AUTO_INCREMENT,
    order_number VARCHAR(50) UNIQUE NOT NULL,
    session_id VARCHAR(255) NOT NULL,
    buyer_name VARCHAR(100) NOT NULL,
    buyer_email VARCHAR(200) NOT NULL,
    buyer_phone VARCHAR(20) NOT NULL,
    shipping_address TEXT NOT NULL,
    total_amount INT NOT NULL,
    payment_method ENUM('CASH', 'POINTS') NOT NULL,
    points_used INT,
    order_status ENUM('PENDING', 'CONFIRMED', 'PROCESSING', 'SHIPPED', 'DELIVERED', 'CANCELLED', 'REFUNDED') NOT NULL,
    is_deleted BOOLEAN DEFAULT FALSE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);

-- 사용자 포인트 테이블
CREATE TABLE user_points (
    id BIGINT PRIMARY KEY AUTO_INCREMENT,
    session_id VARCHAR(255) UNIQUE NOT NULL,
    total_points INT DEFAULT 0,
    used_points INT DEFAULT 0,
    available_points INT DEFAULT 0,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
```

## 📝 주요 API 엔드포인트

### 화학물질 관련 API
- `GET /api/chemicals/frequent` - 자주 사용하는 화학물질 목록 조회
- `GET /api/chemicals/alphabet/{alphabet}` - 알파벳별 화학물질 목록 조회

### 구매자 API
- `GET /user-buyer/products` - 제품 목록 (필터링 지원)
- `GET /user-buyer/products/{seq}` - 제품 상세
- `POST /user-buyer/cart/add` - 장바구니 추가
- `GET /user-buyer/cart` - 장바구니 조회
- `POST /order/cash` - 현금 주문 처리
- `POST /order/points` - 포인트 주문 처리
- `GET /order/my-orders` - 내 주문 목록
- `GET /order/complete/{orderNumber}` - 주문 완료 페이지
- `GET /user-buyer/qna/product/{seq}` - 제품별 Q&A
- `POST /user-buyer/reviews` - 리뷰 작성
- `POST /user-buyer/quote/request` - 견적 요청
- `POST /user-buyer/calibration/request` - 검교정 요청

### 판매자 API
- `GET /user-seller/products` - 판매자 제품 목록
- `POST /user-seller/products` - 제품 등록
- `PUT /user-seller/products/{seq}` - 제품 수정
- `GET /user-seller/orders` - 판매자 주문 목록
- `GET /user-seller/orders/{id}` - 판매자 주문 상세

### 관리자 API
- `GET /admin` - 관리자 대시보드
- `GET /admin/products` - 전체 상품 목록 (페이징, 검색, 필터링)
- `GET /admin/products/{productSeq}` - 상품 상세 정보
- `GET /admin/products/{productSeq}/edit` - 상품 수정 폼
- `POST /admin/products/{productSeq}/edit` - 상품 수정 처리
- `POST /admin/products/{productSeq}/delete` - 상품 삭제
- `GET /admin/orders` - 전체 주문 목록 (페이징, 검색)
- `GET /admin/orders/{orderNumber}` - 주문 상세 정보
- `GET /admin/user-points` - 사용자 포인트 목록 (페이징)
- `POST /admin/user-points/{sessionId}/update` - 사용자 포인트 수동 업데이트

## 🎮 사용자 플로우

### 구매자 플로우
1. **제품 검색**: 화학물질 기반 필터링으로 원하는 제품 검색
2. **장바구니 추가**: 제품을 장바구니에 추가
3. **장바구니 관리**: 수량 조정, 상품 선택/삭제
4. **구매 진행**: 현금 또는 포인트로 결제
5. **주문 완료**: 주문번호 발급 및 주문 내역 확인
6. **주문 관리**: 주문 목록 조회, 주문 취소

### 포인트 시스템
- **포인트 적립**: 관리자에 의해 포인트 적립
- **포인트 사용**: 구매 시 포인트로 결제
- **포인트 환율**: 100포인트 = 100,000원, 230포인트 = 200,000원

## 🔧 문제 해결 가이드

### 일반적인 문제들
1. **빈 페이지 표시**: 브라우저 캐시 삭제 후 새로고침
2. **API 오류**: 서버 로그 확인 및 데이터베이스 연결 상태 점검
3. **화학물질 로딩 실패**: 네트워크 연결 및 API 엔드포인트 상태 확인

### 디버깅 팁
- 브라우저 개발자 도구의 Console 탭에서 JavaScript 오류 확인
- Network 탭에서 API 요청/응답 상태 모니터링
- Spring Boot 애플리케이션 로그에서 서버 사이드 오류 추적

## 🔮 향후 개발 계획

### 1단계 (현재 진행 중)
- [x] 기본 구매 시스템 구현
- [x] 포인트 시스템 구현
- [x] 주문 생성 및 완료
- [x] 주문 목록 조회
- [x] 주문 상세보기
- [x] 주문 취소 기능
- [x] 관리자 시스템 구현
  - [x] 관리자 대시보드
  - [x] 전체 상품 관리 (조회/수정/삭제)
  - [x] 전체 주문 관리
  - [x] 사용자 포인트 관리
  - [x] 검색 및 필터링 시스템
  - [x] 페이징 시스템

### 2단계 (다음 단계)
- [x] 판매자 주문 관리 기능
- [ ] 배송 관리 시스템
- [ ] 재고 관리 시스템
- [ ] 포인트 적립/내역 관리
- [ ] 배송 주소 관리
- [ ] 관리자 시스템 고도화
  - [ ] 사용자 권한 관리
  - [ ] 시스템 로그 및 감사
  - [ ] 백업 및 복구 시스템
  - [ ] 성능 모니터링

### 3단계 (고도화)
- [ ] 실제 결제 시스템 연동
- [ ] 구매 인증 리뷰 시스템
- [ ] 알림 시스템
- [ ] 매출 통계 및 대시보드
- [ ] 모바일 최적화
- [ ] 관리자 시스템 확장
  - [ ] 다국어 지원
  - [ ] API 문서 자동화
  - [ ] 마이크로서비스 아키텍처 전환
  - [ ] 클라우드 배포 지원

## 🤝 기여하기

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다.

## 📞 문의

프로젝트에 대한 문의사항이 있으시면 이슈를 생성해 주세요.

---

**PPE Facility Management System** - 가스 측정기/분석기 전문 전자상거래 플랫폼

