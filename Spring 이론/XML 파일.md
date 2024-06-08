스프링 프레임워크에서 XML 파일은 애플리케이션의 **설정 정보를 정의**하는 데 사용된다. 초기의 스프링 프로게임워크는 주로 XML 기반의 설정 파일을 사용하여 애플리케이션 컴포넌트([[Bean]])의 생성, 구성 및 [[Dependency Injection]] 등을 설정했다. 이러한 방식을 통해 개발자는 애플리케이션의 구조를 쉽게 변경하고 관리할 수 있다.
### XML 파일의 역할
1. **[[Bean]]의 정의**
	- 애플리케이션에서 사용할 객체([[Bean]])들을 정의하고, 그 객체들의 생명주기와 의존성 관계를 설정한다.
2. **[[Dependency Injection]]**
	- 객체 간의 의존성을 외부에서 주입하는 방식으로, XML 파일에서는 빈들 사이의 의존성을 설정하여 스프링 컨테이너가 자동으로 의존성을 주입하도록 한다.
3. **애플리케이션 설정**
	- 데이터베이스 연결 정보, 트랜잭션 관리, [[AOP]] 설정 등 애플리케이션 전반에 걸친 설정 정보를 포함할 수 있다.

### XML 파일 예시
```xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!-- Bean 정의 -->
    <bean id="exampleBean" class="com.example.ExampleBean">
        <!-- 의존성 주입 -->
        <property name="dependency" ref="anotherBean"/>
    </bean>

    <bean id="anotherBean" class="com.example.AnotherBean"/>
</beans>
```
위 예시에서 `exampleBean`과 `anotherBean`이라는 두 개의 빈을 정의하고 있다. `exampleBean`은 `anotherBean`에 대한 의존성을 가지고 있으며, 이 의존성은 `<property>` 태그를 통해 주입된다.