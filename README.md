<!-- 헤더 / 인트로 -->
<div align="center">
  
## 자바/스프링 백엔드 개발자
**Java/Spring Boot Backend** · **Practical Frontend with JS**

[![Email](https://img.shields.io/badge/Email-3400jkh%40naver.com-ef4444?logo=gmail)](mailto:3400jkh@naver.com)

</div>

---

## 🔧 Tech Toolbox
<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,mysql,js,html,css,docker,git,postman,idea,vscode&perline=11" />
</p>

- **Backend:** Java, Spring Boot, JPA, Spring Security, JDBC  
- **DB:** MySQL (인덱싱·페이지네이션·쿼리 튜닝)  
- **Realtime & Search:** WebSocket/Socket.IO, 키워드/필터/랭킹 설계  
- **Ops:** Docker, REST API 설계, 간단한 프론트 제작(JS/HTML/CSS)

---

## 🚀 Highlights (대표 프로젝트)
> 클릭하면 상세 설명이 펼쳐집니다.

### AMGN(Amugeona) — 위치 편의성은 유지하고, 지역 제한은 없앤 중고거래
[![Repo](https://img.shields.io/badge/Repo-AMGN-111?logo=github)](https://github.com/torye2/AMGN)
[![Contribution](https://img.shields.io/badge/Docs-개인_기여_상세-2563eb)](https://github.com/torye2/AMGN/blob/master/docs/CONTRIBUTION_sanghyeok.md)

> **Stack:** Java · Spring Boot · JPA · MyBatis · MySQL · JS  
> **Role:** 백엔드 설계·구현, 프론트 디자인

<details>
<summary><b>구현 기능</b></summary>

- **웹소켓 채팅** (Socket.IO): 구매자/판매자 매칭 → 방 생성/이동 → 시간대 정렬 메시지
- **판매 순위(랭킹)**: 판매자별 판매건 집계, 홈 Top3 노출
- **지역/카테고리 필터링**: 대→소 분류 path 구조, 지역ID/카테고리ID 조회
- **위치 기반 검색**: Kakao REST API로 사용자 좌표 → 인근 상품 리스트
- **상품 검색/관리/상태 전이**: 공백 제거 키워드 매칭, 수정/삭제, `RESERVED`/`SOLD`
- **위시리스트 & 최근 본 상품**: 사용자ID+상품ID 저장/해제, 상세 진입 히스토리
</details>

---

### Yoyang Project — 요양 병원 검색·비교 서비스
[![Repo](https://img.shields.io/badge/Repo-yoyang--project-111?logo=github)](https://github.com/sanghyeok07/yoyang-project)
[![Contribution](https://img.shields.io/badge/Docs-개인_기여_상세-2563eb)](https://github.com/sanghyeok07/yoyang-project/blob/main/docs/CONTRIBUTION_sanghyeok.md)

> **Stack:** Spring Boot · Spring Security · JDBC · MySQL · JS  
> **Role:** 백엔드 설계·구현, 프론트 디자인

<details>
<summary><b>구현 기능</b></summary>

- **시설찾기**: 지역/프로그램 필터 + 키워드 검색
- **공지사항 & Q&A**: 글ID 조회, 페이지네이션(10개/페이지)
- **시설비교**: 선택된 병원 ID set → 비교 테이블 렌더링
- **카테고리 필터링**: 조건 일치 병원 리스트 조회(지역 + 프로그램)
</details>

---

### Groupware Collaboration Platform — 실시간 협업/근태/결재/캘린더 통합 그룹웨어
[![Repo](https://img.shields.io/badge/Repo-AMGW-111?logo=github)](https://github.com/torye2/AMGW)
[![Contribution](https://img.shields.io/badge/Docs-개인_기여_상세-2563eb)](https://github.com/torye2/AMGN/blob/master/docs/CONTRIBUTION_sanghyeok.md)


> **Stack:** Java · Spring Boot · JPA · WebSocket · WebRTC · MySQL  
> **Role:** 백엔드 전반 설계 및 구현 (도메인 모델링, 서비스 로직, 실시간 통신)

<details>
<summary><b>구현 기능</b></summary>

#### 🕒 출결 관리 (Attendance)
- 출근/퇴근 기록 & 휴가/연장근무 신청 흐름 구현
- 근무 시간 통계/요약 제공 (`AttendanceSummaryService`)

#### 📄 전자 결재 (Approval)
- 사용자-문서 읽음 상태를 복합키로 관리 (`ApprovalDoc`, `ApprovalDocPK`)
- 승인/반려/열람 이력 추적 (`ApprovalService`)

#### 🗓 조직 캘린더 (Calendar)
- 팀/개인 일정 생성/조회/공유
- 시간 범위/유저 조건 필터링 (`CalendarService`)

#### 💬 실시간 채팅 (Chat)
- 채팅방 / 참여자 / 메시지 / 읽음 상태 **도메인 분리 설계**
- WebSocket 메시지 전송 & 읽음 반영 (`ChatWsController`, `ChatService`)
- `ChatDto` 로 송수신 포맷 표준화

#### 🎥 화상 회의 (Meeting)
- WebRTC P2P 연결을 위한 Signaling Controller 구현
- Offer / Answer / ICE Candidate 교환 처리

#### ✅ Todo 업무 관리
- 개인 단위 업무 CRUD (`TodoService`)

</details>

<details>
<summary><b>설계 포인트</b></summary>

- **실시간 통신:** WebSocket 기반 메시지 푸시 + WebRTC 시그널 교환 구조 설계
- **복합키 & 관계 모델링:** 읽음 상태, 참여자 관계 등을 별도 엔티티로 정규화
- **명확한 계층 분리:** Controller → Service → Repository → Entity 구조 확립
- **유지보수성 고려:** 단일 도메인 변경 시 영향 범위 최소화
</details>
