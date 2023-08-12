

![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=250&section=header&text=Weather%20App&fontSize=60&animation=fadeIn&fontAlign=26&fontAlignY=40)


---
## 목차

- [URLSession을 이용하여 HTTP 통신 수행하기](#urlsession을-이용하여-http-통신-수행하기)
- [openweather 날씨 API 사용해보기](#openweather-날씨-api-사용해보기)
- [기본 UI구성하기](#기본-ui구성하기)
- [기능 구현하기](#기능-구현하기)


<br/>

---

## URLSession을 이용하여 HTTP 통신 수행하기

<br/>

### 01. HTTP 프로토콜은 기본적으로 어떻게 구성되어 있나요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/1.png" width="400" height="200"><br/>

- HTTP 통신은 기본적으로 요청request와 응답response로 이루어져 있습니다
- 예를 들어 브라우저에 구글을 입력하면 클라이언트의 웹 브라우저를 통해 구글서버에 구글 시작 페이지를 보여달라고 요청합니다
- 구글 서버는 클라로부터 요청을 받으면 구글 시작 페이지에 해당는 html페이지를 클라이언트에게 돌려줍니다.
- 따라서 기본적으로 클라이언트와 서버는 연결되어 있지 않습니다.

#

### 02. 클라이언트와 서버가 연결되어 있지 않는다는게 어떤 뜻인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/2.png" width="400" height="200"><br/>

- 서버가 클라에게 연결을 보내면 곧바로 연결을 종료한다는 것을 의미합니다

#

### 03. HTTP 패킷이란 무엇인가요?

&nbsp;&nbsp;&nbsp;&nbsp;<img src="pic/3.png" width="400" height="200"><br/>

- HTTP 통신은 요청을 보내고 응답을 받을 때 패킷을 통해 주고 받습니다.
- 패킷은 크게 header와 body로 구성되어 있습니다.
- 패킷에는 보내는 사람의 주소, 받는 사람의 주소, 패킷의 생명시간등이 들어가 있고 body에는 통신하려는 데이터가 들어있습니다

#

### 04. HTTP 메서드 종류에 대해서 설명해주세요

- **GET**: 클라이언트가 서버에 리소스를 요청할 때 사용합니다.
- **POST**: 클라이언트가 서버의 리소스를 새로 만들때 사용합니다.
- **PUT**: 클라이언트가 서버의 리소스를 전체 수정할 때 사용합니다.
- **PATCH**: 클라이언트가 서버의 리소스를 일부 수정할 때 사용합니다.
- **DELETE**: 클라이언트가 서버의 리소스를 삭제할 때 사용합니다.
- HEAD: 클라이언트가 서버의 정상 작동 여부를 확인할 때 사용합니다.
- OPTIONS: 클라이언트가 서버에서 해당 URL이 어떤 메소드를 지원하는지 확인할 때 사용합니다.
- CONNECT: 클라이언트가 프록시를 통하여 서버와 SSL 통신을 하고자 할 때 사용합니다.
- TRACE: 클라이언트와 서버간 통신 관리 및 디버깅을 할 때 사용합니다.

  #

  ### 05. 서버가 보내주는 상태코드 종류에 대해서 설명해주세요

  - 100번대 Informational: 요청정보를 처리중 
  - **200번대** Success: 요청을 정상적으로 처리함
  - 300번대 Client Error: 요청을 완료하기 위해 추가 동작 필요
  - **400번대** Client Error: 서버가 요청을 이해하지 못함
  - 500번대 Server Error: 서버가 요청 처리 실패함




