# Song Taehyun | Backend Portfolio

Java/Spring 기반으로 인증·트랜잭션·데이터 정합성·실시간 통신·배포를 경험한 신입 백엔드 개발자 송태현입니다.

기능 구현에서 끝나지 않고, 실패 시 데이터가 어떤 상태로 남는지와 인증·권한 및 트랜잭션의 경계를 고민합니다.

## Quick View

| 문서 | 설명 | 바로 보기 |
| --- | --- | --- |
| Summary | 10페이지 요약본 | [Summary PDF](./docs/SongTaehyun_Backend_Portfolio_Summary.pdf) |
| Full | 세 프로젝트의 핵심 설계와 문제 해결을 담은 통합본 | [Full PDF](./docs/SongTaehyun_Backend_Portfolio_Full.pdf) |

## Project Deep Dive

### DDDang — 반려동물 통합 케어 플랫폼

회원·인증, 반려동물, 오픈채팅, 공통 백엔드 규약과 배포를 담당했습니다. Refresh Token 재사용 감지를 `REQUIRES_NEW`로 분리하고, REST 송신 + STOMP 수신, `AFTER_COMMIT` 방송, JPA `@Version` 낙관적 잠금을 적용했습니다. AWS EC2에서 2026년 8~9월 배포·운영했으며 현재 서버는 종료된 상태입니다.

[PDF](./docs/projects/SongTaehyun_Backend_Portfolio_DDDang.pdf) · [Repository](https://github.com/Taehyun-0502/pet_project)

### Haru Health — 헬스장 운영 관리 서비스

결제·매출, 정산·물품, 출석·PT, SSE 알림을 담당했습니다. 현장 결제 결과를 기록하는 구조로 외부 PG는 연동하지 않았으며, 팀원이 담당한 계약 도메인의 조회·활성화 서비스를 결제 흐름에서 호출하도록 연결했습니다. 결제 트랜잭션, PostgreSQL advisory lock, PT 조건부 `UPDATE`로 정합성과 동시성 문제를 다뤘습니다.

[PDF](./docs/projects/SongTaehyun_Backend_Portfolio_HaruHealth.pdf) · [Repository](https://github.com/Taehyun-0502/health_Project)

### Cooking Star — 레시피·요리 커뮤니티

회원·인증, 댓글·좋아요·북마크·팔로우, Kakao Local·Naver Blog 연동, 관리자·방문 집계를 담당했고 요리 기록 게시판은 공동 구현했습니다. Naver Shopping·장바구니·구매내역·Gemini 연동은 팀원이 담당했습니다.

[PDF](./docs/projects/SongTaehyun_Backend_Portfolio_CookingStar.pdf) · [Repository](https://github.com/Taehyun-0502/cooking_star)

## Tech Stack

`Java 21` · `Spring Boot 3.5` · `Spring Security` · `JPA` · `MyBatis` · `PostgreSQL` · `WebSocket/STOMP` · `SSE` · `AWS EC2` · `nginx` · `GitHub Actions`

## Contact

- GitHub: [Taehyun-0502](https://github.com/Taehyun-0502)
