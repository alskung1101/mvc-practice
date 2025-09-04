## 1. Rest API란 무엇인가?

REST API란 Representational State Transfer 아키텍처 스타일을 따르는 API(Application Programming Interface)를 의미한다.
간단히 말해, 클라이언트(브라우저, 앱 등)와 서버가 데이터를 주고받을 때 규칙을 정해놓은 방식이다.

HTTP 프로토콜을 기반으로 동작한다.

요청(Request)과 응답(Response) 구조로 이루어진다.

자원을 URI(Uniform Resource Identifier)로 식별한다.

CRUD(Create, Read, Update, Delete) 작업을 HTTP 메서드(GET, POST, PUT, DELETE 등)와 매핑시켜 사용한다.

예시:

GET /users/1

위 요청은 users라는 자원 중 ID가 1인 사용자의 정보를 가져오라는 의미이다.

## 2. HTTP 통신에 대하여

HTTP(HyperText Transfer Protocol)는 웹에서 데이터를 주고받기 위한 규약이다.
클라이언트와 서버는 요청과 응답을 주고받으며 동작한다.

## HTTP 통신 구조

1. 클라이언트(Client): 요청을 보내는 주체 (예: 웹 브라우저, 모바일 앱)

2. 서버(Server): 요청을 처리하고 응답을 돌려주는 주체 (예: 웹 서버, API 서버)

3. 요청(Request): 클라이언트가 서버에 원하는 작업을 전달 (예: GET / POST 요청)

4. 응답(Response): 서버가 요청을 처리한 결과를 클라이언트에 반환

예시:

### 요청 (Client → Server)
GET /products HTTP/1.1
Host: example.com

### 응답 (Server → Client)
HTTP/1.1 200 OK
Content-Type: application/json

[
  {"id":1, "name":"Keyboard"},
  {"id":2, "name":"Mouse"}
]

여기서 클라이언트는 상품 목록을 요청했고, 서버는 JSON 형식으로 데이터를 응답했다.

## 3. 브라우저에 URL 입력 시 동작 과정

브라우저 주소창에 URL을 입력하면 다음과 같은 과정이 일어난다.

### 1. URL 입력

사용자가 https://example.com과 같은 주소를 입력한다.

### 2. DNS 조회

브라우저는 URL에 포함된 도메인(example.com)을 IP 주소로 변환하기 위해 DNS 서버에 요청한다.

결과: example.com → 203.0.113.10 (IP 주소)

<img width="1280" height="802" alt="image" src="https://github.com/user-attachments/assets/2e4d70d5-9af5-4855-979c-c4987f217eff" />


### 3. 서버 연결

브라우저는 얻은 IP 주소로 서버에 연결을 시도한다.

HTTPS의 경우 TLS/SSL 핸드셰이크를 통해 보안 연결을 설정한다.

### 4. HTTP 요청 전송

브라우저는 서버로 HTTP 요청(Request)을 보낸다.

예: GET / HTTP/1.1

### 5. 서버 처리

서버는 요청을 받고, 필요한 데이터를 조회하거나 로직을 실행한다.

그 결과를 HTTP 응답(Response)으로 생성한다.

### 6.브라우저 렌더링

브라우저는 응답받은 HTML, CSS, JavaScript를 해석하여 화면에 표시한다.

추가로 필요한 리소스(이미지, 스타일, 스크립트 등)를 다시 요청하고 불러온다.

<img width="1700" height="712" alt="image" src="https://github.com/user-attachments/assets/ba80589b-7103-4e26-84e1-276a6ad5c2fb" />

