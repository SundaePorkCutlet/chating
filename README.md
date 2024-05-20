안써본기술
websocket redis kafka mongoDB 공부를 위해 하는 작은 프로젝트

---

Kafka: 실시간 메시지 스트리밍을 위해 사용됩니다. 채팅 메시지를 Kafka 토픽으로 전송하여 소비자들이 이를 처리할 수 있도록 합니다.

Redis: 실시간 메시지 저장 및 빠른 조회를 위해 사용됩니다. Redis Pub/Sub 기능을 이용하여 실시간 채팅을 구현할 수 있습니다.

MongoDB: 영구적인 메시지 저장을 위해 사용됩니다. 채팅 히스토리나 사용자 정보를 저장하는데 사용됩니다.

Golang: 서버 로직을 구현하기 위해 사용됩니다. 고성능을 유지하면서 동시에 많은 연결을 처리할 수 있습니다.

**프론트단은 chatGpt형님이 모두 만들어주십니다**


---
**구성 요소**

사용자 인증 서비스

채팅 메시지 브로커 (Kafka)

실시간 메시지 처리기 (Redis)

메시지 저장 및 검색기 (MongoDB)

채팅 서버 (Golang)

---
**데이터 흐름**

사용자가 채팅 서버에 연결합니다.

채팅 서버는 Redis를 통해 연결된 사용자들에게 실시간 메시지를 전달합니다.

채팅 메시지는 Kafka로 전송되어 분산 처리됩니다.

메시지는 MongoDB에 저장되어 나중에 검색할 수 있습니다.

---
**version 0.1 (websocket)**

웹소켓으로 readMessage와 writeMessage 구현 , redis에 refresh token 저장
<img width="959" alt="image" src="https://github.com/SundaePorkCutlet/chating/assets/87690981/c77748c8-13ae-4cc2-aa64-8fcc51157cf6">
<img width="720" alt="image" src="https://github.com/SundaePorkCutlet/chating/assets/87690981/3002240c-39bd-4955-916f-4204106d1565">

1. 채팅방 선택
2. 채팅 단순히 화면에 띄우기

회원가입 , 방만들기, 채팅 히스토리 등등 없음...

