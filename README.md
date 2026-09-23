# SpringBootMyBatis

Spring Boot 3 + MyBatis 기반 웹 애플리케이션입니다.

## 기술 스택

- Java 17
- Spring Boot 3.3.1
- MyBatis (mybatis-spring-boot-starter)
- MariaDB
- Spring WebSocket
- JSP / JSTL (View)
- Tess4j (OCR)
- Jsoup (크롤링/파싱)
- Spring Mail
- Lombok

## 주요 기능

- 회원 관리 (가입, 로그인, 아이디/비밀번호 찾기)
- 게시판 (공지사항)
- 채팅 (1:1 / 전체 채팅, WebSocket)
- 영화 순위 수집 및 조회
- OCR 이미지 텍스트 인식
- 번역 (Papago) / 언어 감지
- 날씨 조회
- 메일 발송

## 프로젝트 구조

```
src/main/java/kopo/poly
├── controller   # 요청 처리
├── service      # 비즈니스 로직 (interface + impl)
├── mapper       # MyBatis 매퍼 인터페이스
├── dto          # 데이터 전달 객체
├── chat         # WebSocket 채팅 핸들러
├── config       # 설정 (WebSocket 등)
└── util         # 공통 유틸리티

src/main/resources
├── mapper       # MyBatis XML 매퍼
└── application.properties

src/main/webapp/WEB-INF/views  # JSP 화면
sql                            # 테이블 생성 스크립트
```

## 실행 방법

1. MariaDB에 DB를 생성하고 `sql/` 디렉터리의 스크립트를 실행합니다.
2. `src/main/resources/application.properties`에 DB 접속 정보 등 환경값을 설정합니다.
3. 아래 명령으로 실행합니다.

```bash
./mvnw spring-boot:run
```

기본 포트는 `application.properties`에 설정된 값을 따릅니다.
