# Orderly

테이블 주문용 메뉴 안내 챗봇입니다. 음성으로 메뉴를 듣는 시각장애인 손님도 쓸 수 있게 만들었습니다.

## 실행 (Node.js 18 이상, 추가 설치 없음)

```bash
OPENAI_API_KEY=발급받은키 node server.js
```

브라우저에서 `http://localhost:3000/?table=3&ai=on` 을 엽니다.

- `ai=on` 을 빼면 서버의 AI 없이 브라우저 안의 규칙 엔진만으로 답합니다.
- 매장 관리 화면: `#/admin`

## 구조

- `index.html`: 손님 화면과 관리자 화면, 규칙 엔진(알레르기·담기·주문 확정·직원 호출)
- `server.js`: `index.html` 제공, `/api/chat` 으로 GPT 호출 후 답 검증

API 키는 서버에만 둡니다. 저장소에 올리지 마세요.
