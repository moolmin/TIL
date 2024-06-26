스프링 프레임워크에서 MVC(Model-View-Controller)는 웹 애플리케이션을 개발하기 위한 **디자인 패턴**이다. 
사용자의 인터페이스로부터 비즈니스 로직을 분리하여 서로 영향 없이 쉽게 고칠 수 있는 설계가 가능하다.

### 구성 요소
- **모델(Model)**
	- 데이터를 처리하는 영역
	- 데이터베이스와의 상호작용, 데이터 검증, 비즈니스 규칙 등을 담당한다.
- **뷰(View)**
	- 데이터를 보여주는 화면 자체의 영역
	- 사용자에게 데이터를 표시하고, 입력을 받는다.
- **컨트롤러(Controller)**
	- 모델과 뷰 사이에서 중재자(브릿지) 역할
	- 사용자의 요청은 모두 컨트롤러를 통해 진행되어야 한다.
	- 컨트롤러로 들어온 요청은 어떻게 처리할지 결정하여 모델로 요청을 전달함
- **예시**
	- 쇼핑몰에서 상품을 검색하면 그 키워드를 컨트롤러가 받아 모델과 뷰에 적절하게 입력을 처리하여 전달함
	- 검색을 위한 키워드가 넘어오면 데이터베이스에서 관련된 상품의 데이터를 받아 뷰에 전달함
	- 검색 결과를 보여주기 위해 모델에서 결과 상품 리스트 데이터를 받음

### 스프링 MVC 패턴 적용 과정
1. **스프링 프로젝트 설정**
	- 스프링 부트를 사용한다면, 시작하기 위해 Spring Initializr([https://start.spring.io/)를](https://start.spring.io/) 사용하여 프로젝트를 생성하고, 필요한 의존성(예: spring-boot-starter-web)을 추가한다.
2. **컨트롤러 작성**
	- @Controller [[Annotation]]을 클래스에 추가하여 스프링에게 이 클래스가 컨트롤러임을 알린다.
	- 요청을 처리할 메소드를 작성하고, `@RequestMapping` 또는 `@GetMapping`, `@PostMapping` 등의 [[Annotation]]을 사용하여 요청 경로를 지정한다.
3. **모델 작성**
	- 비즈니스 로직과 데이터를 처리할 모델 클래스를 작성한다.
4. **뷰 생성**
	- 컨트롤러에서 뷰로 데이터를 전달하기 위해, 모델 객체를 사용하거나, ModelAndView 객체를 반환할 수 있다.

### 디자인 패턴의 장단점
#### 장점
- 개발자 간의 원활한 협업 가능
- 소프트웨어 구조를 파악하기 용이함
- 재사용을 통해 개발 시간 단축
- 설계 변경이 있을 경우 비교적 원활하게 조치 가능
#### 단점
- 객체지향적 설계를 고려하여 진행해야 함
- 초기 투자 비용이 많이 들어감 (돈, 시간 등)