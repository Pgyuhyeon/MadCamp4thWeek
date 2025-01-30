## Team & Stacks

**박규현 (한양대학교 컴퓨터소프웨어학부 22, BE)**

![KakaoTalk_Image_2025-01-23-18-37-46_001.png](attachment:22908d40-5623-445f-8a22-ea36228439aa:291e626e-77f1-4096-a5f3-5b9a954c08ad.png)

- Node.js + express
- MongoDB
- Github, `kakaotalk`, Notion

**진예환 (KAIST 전기 및 전자공학부 21, FE)**

![KakaoTalk_Image_2025-01-23-18-37-46_002.png](attachment:a1f91e8c-f2bd-4a62-9a12-db92678f4047:KakaoTalk_Image_2025-01-23-18-37-46_002.png)

- React
- Figma
- Github, `kakaotalk`, Notion

## outline

---

![201106161403401001_1.jpg](attachment:39fe22af-98d4-4274-9914-9c8b1fc68077:201106161403401001_1.jpg)

### 28박 29일동안 열심히 달려오느라 모두 고생 많았습니다….👏🏻👏🏻👏🏻👏🏻

### *여러분들의, 여러분들에 의한, 여러분들을 위한* 게임을 만들어보았습니다….

### 게임 시작하겠습니다…………🎮

![images.jpeg](attachment:aee340f1-37f5-4f01-b3d4-cd24b4571e44:images.jpeg)

## APIs

### Socket

---

URL:  `http://192.249.29.181:3000`

| **이벤트 이름**  | **방향** | **설명** | **데이터 형식** |
| --- | --- | --- | --- |
| `getParticipants` | Server → Client | 특정 방의 참여자 목록을 전송합니다. | `{ "participants": ["User1", "User2", "User3"] }` |
| `getHost` | Server → Client | 특정 방의 방장 정보를 전송합니다. | `{ "host": "User1" }` |
| `startGame` | Client → Server | 게임 시작을 요청합니다. | `{ "room": "room1", "category": "영화" }` |
| `joinRoom` | Client → Server | 특정 방에 입장합니다. | `{ "room": "room1", "nickname": "User1" }` |
| `gameStarted` | Server → Client | 게임이 시작되었음을 알립니다. | `{ "category": "영화" }` |
| `chatMessage` | Client → Server | 특정 방에 채팅 메시지를 전송합니다. | `{ "room": "room1", "message": "안녕하세요!" }` |
| `disconnect` | Server → Client | 사용자의 연결이 해제되었음을 알립니다. | `{ "message": "User1 님이 연결을 해제했습니다." }` |
| `chatMessage` | Server → Client | 방의 모든 사용자에게 메시지를 전송합니다. | `정답일 경우: { "nickname": "User1", "message": "정답!" } 일반 메시지: { "nickname": "User1", "message": "채팅 내용" }` |
| `error` | Server → Client | 에러 메시지를 전송합니다. | `{ "message": "게임 시작에 실패했습니다." }` |
| `roomJoined` | Server → Client | 방 참가 성공을 클라이언트에게 알립니다. | `{ "roomId": "room1" }` |
| `hostMessage` | Server → Client | 방의 호스트(방장)에게 메시지를 전송합니다. | `{ "message": "이 메시지는 호스트만 볼 수 있습니다." }` |
| `clientMessage` | Server → Client | 방의 호스트를 제외한 모든 사용자에게 메시지를 전송합니다. | `{ "message": "이 메시지는 일반 참가자에게만 보입니다." }` |
| `endGame` | Client → Server | 게임 종료 요청을 서버로 전송합니다. | `{ "room": "room1" }` |
| `gameEnded` | Server → Client | 게임 종료를 클라이언트에 알립니다. | `{ "message": "게임이 종료되었습니다!" }` |

### API

---

`Base URL: http://192.249.29.181:3000`

| Method | URL | Description | Request | Response |
| --- | --- | --- | --- | --- |
| POST | `/keyword` | 랜덤 키워드 생성 | Body: `{"category: "영화" }` | 성공: `{ "keyword": "메이즈러너" }` 에러: `{ "error": "Category is required" }` |
| POST | `/generate-image` | 텍스트로 그림 생성 | Body: `{"prompt": "빌딩에서 깡패한테 둘러싸여서 혼자 쇼파에 앉아 담배피는중","n": 1,"size": "1024x1024"}` | 성공: `{  “imageUrls: [ “http://djslkdjsldjslds”] }`에러: `{"error": "Prompt is required" }` |

## 웹사이트 소개

## **1. 홈 화면**

![image.png](attachment:7467ca7d-a007-4593-b8d9-f697b705eabd:image.png)

기본 화면

![image.png](attachment:a27eea3e-edac-4693-bd07-355a86fcd0df:image.png)

로그인 기능& 플레이 방법

![image.png](attachment:236c7f80-c0d7-4c43-8a8e-47704e2623f4:image.png)

게임 목록

## **2. 게임 시작 화면**

![image.png](attachment:ac1f47ff-4e72-42c2-a17d-6124c266794c:image.png)

방장: 게임 시작 버튼
게임 나가기 버튼, 채팅기능

## **3. 게임 카테고리 선택 화면**

![image.png](attachment:e2d0084a-ffaf-4994-810e-fd4f4d718d63:image.png)

방장은 게임을 고를 수 있음

## 느낀점

**박규현 (한양대학교 컴퓨터소프웨어학부 22, BE)**

**진예환 (KAIST 전기 및 전자공학부 21, FE)**

- 디자인은 너무 어려운 것 같습니다. gptㅠㅠ
- gpt가 맛이 갔네요…
