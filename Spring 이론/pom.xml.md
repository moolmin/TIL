Maven 프로젝트를 생성하면 루트 디렉토리에 생성되는 파일
Project Object Model 정보를 담고 있음

### 주요 설정 정보
#### 프로젝트 정보
-  프로젝트의 이름, 개발자 목록, 라이센스 등
#### 빌드 설정 정보
- 소스, 리소스, 라이프 사이클 등 실행할 플러그인 등
#### POM 연관 정보
- 의존 프로젝트(모듈), 상위 프로젝트, 하위 모듈 등

### 프로젝트 기본 정보
```xml
<name>Example Project</name>
<url>http://www.example.com/project</url>
<description>A simple example project </description>
    
<organization>
    <name>Example Company</name>
    <url>http://www.example.com</url>
</organization>
```
- name 태그: 프로젝트 명
- url 태그: 프로젝트 사이트 URL
- description 태그: 프로젝트에 대한 간단한 설명
- organization 태그: 프로젝트를 관리하는 단체 설명

```xml
<groupId>com.example</groupId>
<artifactId>example-project</artifactId>
<version>1.0-SNAPSHOT</version>
<packaging>jar</packaging>
```
- groupId 태그: 프로젝트의 그룹 ID 설정
- artifactId 태그: 프로젝트의 아티팩트 ID 설정
- version 태그: 프로젝트의 버전
- packaing 태그: 패키징 타입 설정
	- jar: 자바 프로젝트 압축 파일
	- war: 웹 어플리케이션을 위한 패키징 방식

### 프로젝트 의존 설정
```xml
<dependencies>
    <!-- 예시: JUnit 테스트 프레임워크 의존성 -->
    <dependency>
        <groupId>junit</groupId>
        <artifactId>junit</artifactId>
        <version>4.13.1</version>
        <scope>test</scope>
    </dependency>
    
    <!-- 추가 의존성 설정 -->
</dependencies>

```
- dependencies 태그: 라이브러리 의존성 정보를 가지고 있는 dependency 태그를 묶은 태그
- dependency 태그: 각 라이브러리의 정보를 담는 태그
- groupId 태그: 의존성 라이브러리의 group ID
- artifactId 태그: 의존정 라이브러리의 아티팩트 ID
- version 태그: 의존성 라이브러리의 버전
- scope 태그: 해당 라이브러리의 이용 범위를 지정