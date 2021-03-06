# REST

### REST는 웹의 아키텍처 스타일이다.

REST는 웹의 아키텍처 스타일이다. 먼저 아키텍쳐 스타일에 대해 알아보자.

- 아키텍쳐 스타일은 '아키텍쳐 패턴'이라고도 하며, 
- 복수의 아키텍쳐의 공통된 성질, 양식, 규정 혹은 독특한 방식을 가리키는 말이다.
- **제약 조건의 집합**이라고 볼 수 있으며 아키텍쳐 스타일에 속한 제약조건을 모두 지켜야 아키텍쳐 스타일을 따른다고 볼 수 있음.

아키텍쳐와 아키텍쳐 스타일은 별개이다.

- 실제 시스템은 구체적인 아키텍쳐를 가지고 있지만
- 그 아키텍처를 설계할 때, 설계 지침, 규정, 방식 즉, 아키텍처 스타일을 적용한다.
- 시스템의 아키텍처를 결정할 때 나침반이 되는 것이 아키텍처 스타일이다.



REST는 **네트워크 시스템의 아키텍처 스타일**이다.

- 네트워크 시스템의 아키텍처 스타일로서 가장 유명한 것은 클라이언트/서버(Client-Server)이다.
- 웹의 아키텍처 스타일은 REST이기도 하지만, 클라이언트/서버이기도 하다.
  - REST는 클라이언트 서버 구조에서 파생되었기 때문
  - 순수한 클라이언트/서버 아키텍처 스타일에 몇 가지 제약을 더한 것이 REST 아키텍처 스타일이다.
- REST는 웹 전체의 아키텍처 스타일이기도 하며, 개별 웹 서비스와 웹 API의 아키텍처 스타일이기도 하다.
  - 웹 서비스와 웹 API에서도 REST의 규약을 지키는 것은 중요
  - 개별 웹 서비스가 전체의 조화를 무너뜨리면, 전체가 통일된 아키텍처 스타일을 지킬 수 없기 때문



### REST에 있어서 중요한 개념의 하나로 리소스(Resource)가 있다.

리소스(Resource)란?

- 웹 상에 존재하는 이름을 가진 모든 정보
- 리소스가 이름을 가진다는 것?
  - 어떤 리소스를 다른 리소스와 구별하기 위한 것



리소스 명칭으로서의 URI

- 리소스의 이름이란 URI를 말한다.
- 리소스는 URI로 식별할 수 있다.
  - ex) 서울의 일기 예보 - http://weather.naver.com/rgn/cityWetrWarea.nhn?cityRgnCd=CT001000

- URI를 이용함으로써, 프로그램은 리소스가 표현하는 정보에 접근할 수 있다.



리소스의 어드레스 가능성(Addressability)

- URI가 지니고 있는 리소스를 간단히 가리킬 수 있는 성질
- URI가 없었던 시절에는 특정 파일에 접근하는 방법을 일일이 설명했어야 했다.
  - 해당 파일을 ftp.example.com에 두었고, 디렉터리는 /public/data이고, 파일명은 sample_file.gz이고, ...
- URI가 있는 현재는 URI 한 줄로 적어 액세스하는 것이 가능하다.
  - ftp://example.com/public/data/sample_file.gz



복수의 URI를 가진 리소스

- 1개의 리소스는 복수의 URI를 가질 수 있다.
  - 오늘이 2021년 1월 1일이라면
    - http://weather.example.com/seoul/today
    - http://weather.example.com/seoul/2021-01-01
- 하나의 리소스에 URI를 여러 개 붙여 두면, 클라이언트가 리소스에 접근하기 쉬워짐.
- 반면, 어느 것이 정식 URI인지 알기 힘들다.



리소스의 표현과 상태

- 리소스는 ''웹상에 존재하는 정보''라는 추상적인 개념
- 서버-클라이언트 간에 실제로 리소스를 주고 받을 때는 구체적인 데이터를 송신하는데 이 데이터를 '**Resource Representation**'이라고 부른다.
- 또한 리소스에는 '**상태**'라는 것이 있음.
- 시간의 경과에 따라 리소스의 상태가 변하면 그 표현도 변함



### 그래서 다시, REST란?

Representational State Transfer 약자로, 다음과 같이 구성되어 있음.

- 자원(resource): URI
- 행위(verb): HTTP Method
- 표현(representations)

즉, **REST는 URI를 통해 자원을 표시하고, HTTP Method를 이용하여 해당 자원의 행위를 규정하여 그 결과를 받는 것**



### 왜 REST인가?

- REST는 HTTP/1.1 스펙과 동시에 만들어졌음 
- HTTP 프로토콜을 정확히 의도에 맞게 활용하여 디자인하게 유도하기 때문에 디자인 기준 명확
- REST의 기본 원칙을 성실히 지킨 서비스 디자인은 "RESTful 하다"라고 표현함
- 이렇게 잘 디자인된 API는 서비스가 여러 플랫폼을 지원해야 할 때 설명을 간결하게 해주며 여러 가지 상황을 쉽게 해결할 수 있게 해줌.



### REST를 구성하는 스타일

REST 아키텍처 스타일이 과연 어떻게 구성되어 있는지 살펴보자.

#### 클라이언트/서버(Client-Server)

- 웹은 **HTTP라는 프로토콜을 이용해 클라이언트와 서버가 서로 통신하는 아키텍처 스타일**을 채용하고 있음
- 요청(Request)을 보내면 응답(Response)하는 구조
- 장점: 단일 컴퓨터 상에서 모든 것을 처리하는 것이 아니라, 클라이언트와 서버로 분리해서 처리할 수 있다.
  - 클라이언트를 멀티 플랫폼으로 구성할 수 있다. (웹에 PC, 휴대전화, 게임기를 통해서도 접속)
  - UI는 클라이언트 담당. 서버는 데이터 스토리지로서의 기능만 제공해도 됨
  - 복수의 서버를 조합해 확장함으로써 가용성 올릴 수 있음

#### 무상태성(Statless)

- stateless - **클라이언트의 애플리케이션 상태를 서버에서 관리하지 않는다**
- 장점: 서버가 애플리케이션 상태를 가지지 않으면, 서버 측의 구현을 간략화 할 수 있다.
- Cookie-Session을 이용하여 HTTP를 스테이트풀하게 만드는데 이는 REST 관점에서는 HTTP의 잘못된 확장임.

#### 캐시(Cache)

- 캐시란 한번 가져온 리소스를 클라이언트 쪽에서 돌려쓰는 방식
- 장점: 서버와 클라이언트 사이의 통신량을 줄여 네트워크 대역 이용과 처리시간 축소 가능
- 단점: 오래된 캐시를 이용하면 정보의 신뢰성이 떨어질 수 있음

#### 유니폼 인터페이스(Uniform Interface)

- 유니폼 인터페이스는 **URI로 지정한 리소스에 대한 조작을 통일되고 한정적인 인터페이스로 수행하는 아키텍처 스타일**을 말한다.
- REST를 가장 특징짓는 아키텍처 스타일이다
  - 다른 스타일의 경우, HTTP만 잘 따라도 지켜지는 스타일이기 때문(HTTP의 특성과 동일)
- Uniform Interface의 제약조건
  - identification of resources - 리소스가 uri로 식별되야 한다.
  - manipulation of resources through representations - representation 전송을 통해서 리소스를 조작해야 한다. 리소스를 만들거나 업데이트하거나 삭제할 때 http message에 표현을 담아 전송을 해야한다.
  - **Self-descriptive messages - 메시지는 스스로를 설명해야 한다. 메시지의 내용으로 온전히 해석이 가능해야한다.**
  - **hypermedia as the engine of application state(HATEOAS) - 애플리케이션의 상태는 Hyperlink를 이용해 전이되어야한다.**
  - (REST API라고 알려진 거의 모든 것들이 3,4번째 제약 조건이 지켜지지 않고 있다고 한다. -그런 REST API로 괜찮은 가 중-)[https://www.youtube.com/watch?v=RP_f5dMoHFc]

#### 계층화 시스템(Layered System)

- 시스템을 몇 개의 계층으로 분리하는 아키텍처 스타일
- 웹 서비스에서 서버와 클라이언트 간의 로드 밸런서를 설치해 부하를 분산시키거나, 프록시를 설치해 액세스를 제어함.
- 클라이언트 측에서 보면, 서버나 프록시 모두 동일한 인터페이스로 접속할 수 있기 때문에 접속할 곳이 바뀐 것을 신경 쓸 필요가 없어짐.
- 서버와 프록시 등 각 컴포넌트 간의 인터페이스를 HTTP로 통일하고 있기에 실현 가능

#### 코드 온 디맨드(Code-On-Demand) - Optional

- 프로그램 코드를 서버에서 다운 받아 클라이언트에서 실행하는 아키텍처 스타일
- Javascript, Flash, Java 애플릿 등
- 장점: 클라이언트의 차후 확장성
- 단점: 프로토콜 가시성이 저하됨



REST는 아키텍처 스타일이므로 실제 시스템을 설계할 때는 그 시스템의 아키텍처를 만들어야만 한다.

- REST에 기초한 아키텍처를 구축할 경우라도 REST를 구성하는 스타일 중 몇 가지를 제외하더라도 상관없음
  - ex) Cookie-Session을 사용하여 스테이트풀 하지만, URI 형식 등은 REST 제약에 따르는 아키텍처
  - (''그런 REST API로 괜찮은가'에 따르면') REST의 창시자 로이 필딩은 "REST 스타일 규칙을 따르던가 다른 이름으로 부르던가 둘 중 하나만 해달라"라고 말함.

- 소프트웨어와 시스템의 설계에서는 아키텍처 스타일의 이상과 타협해야하는 부분도 있음
- 이상을 염두에 두면서 실제로 동작하고 가치를 제공할 수 있는 시스템을 만드는 것이 중요함.





#### [참고]

- 유튜브, "그런 REST API로 괜찮은가"
- 웹을 지탱하는 기술