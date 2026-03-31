# System Seoul 82 Project (D2C Platform)

## 1. Project Vision & WHY
* **목표:** 한국 언더그라운드 디지코어 크루 '시스템 서울 82'의 독자적인 D2C(Direct to Consumer) 웹 플랫폼 구축.
* **배경:** 대형 플랫폼(유튜브, 멜론 등)의 알고리즘과 제재에서 벗어나, 아티스트가 직접 팬덤 데이터를 소유하고(Owned Audience) 소통하기 위함.
* **디자인 무드:** [2hollis.life](https://www.2hollis.life/) 레퍼런스 참고. 다크하고 미니멀한 언더그라운드 감성. (단, 현재는 디자인보다 **백엔드/기능의 MVP(최소 기능 제품) 빠른 구현**이 클라이언트의 최우선 요구사항임).

## 2. Core Business Logic (WHAT)
이 프로젝트는 아래의 핵심 비즈니스 모듈이 완벽하게 동작해야 합니다.
1. **Auth:** 팬들의 회원가입 및 로그인 (초기 MVP는 이메일/비밀번호 우선, 추후 소셜 로그인 확장 고려). 유저(팬)와 어드민(아티스트) 권한 분리.
2. **Social Hub:** 사운드클라우드, 애플뮤직, 유튜브 등 외부 소셜/음원 링크 통합 라우팅.
3. **Store (Drop):** 한정판 MD 상품 등록 및 드랍(오픈 일자 스케줄링) 기능. 카운트다운 후 판매 전환 기믹.
4. **Video:** 자체 서버 호스팅 대신 유튜브 임베드(Iframe) 방식으로 비디오 아카이브 제공.
5. **Tour:** 공연 일정 안내 및 외부 예매처(Yes24 등) 아웃링크 연결.
6. **Admin Dashboard:** 클라이언트(아티스트)가 위 모든 콘텐츠(배경화면 교체 포함)를 직접 관리(CRUD)할 수 있는 백오피스.

## 3. Tech Stack & Rules (HOW)
* **Backend:** Java, Spring Boot, Spring Security, JPA/Hibernate.
* **Database:** RDBMS (MySQL 또는 PostgreSQL 사용).
* **Authentication:** 세션 대신 무상태(Stateless) JWT 기반 인증 사용.
* **Code Style:** - 코드는 명확하고 간결하게 작성하며, Controller/Service/Repository 레이어를 엄격히 분리할 것.
  - 모든 API는 RESTful 원칙을 따르며 JSON 형태로 응답할 것.
