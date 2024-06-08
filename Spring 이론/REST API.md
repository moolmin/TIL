REST 아키텍처의 조건을 준수하는 어플리케이션 프로그래밍 인터페이스를 뜻한다.
최근 많은 [[API]]가 REST API로 제공되고 있다.
일반적으로 REST 아키텍처를 구현하는 웹 서비스를 RESTful 하다고 표현한다.

### REST API 특징
- REST 기반으로 시스템을 분산하여 확장성과 재사용성을 높임
- HTTP 표준을 따르고 있어 여러 프로그래밍 언어로 구현할 수 있음

### REST API 설계 규칙
#### 웹 기반의 REST API를 설계할 경우에는 URL을 통해 자원을 표현해야 함
- https://thinkground.studio/member/589
- Resource: member
- Resource id: 589
#### 자원에 대한 조작은 HTTP Method(CRUD)를 통해 표현해야 함
- URL에 행위가 들어가면 안됨
- HEADER을 통해 CRUD를 표현하여 동작을 요청해야 함
#### 메세지를 통한 리소스 조작
- HEADER을 통해 content-type을 지정하여 데이터를 전달
- 대표적 형식으로는 HTML, XML, JSON이 있음
#### URL 규칙
- URL에는 소문자를 사용
- Resource의 이름이나 URL이 길어질 경우 하이픈(-)을 통해 가독성을 높일 수 있음
- 언더바( _ ) 는 사용하지 않음 
- 파일 확장자를 표현하지 않음
