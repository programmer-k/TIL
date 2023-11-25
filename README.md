# TIL
TIL for back-end (YC Tech Academy)

## 1주차
* REST API
* Inversion of Control
* Dependency Injection: +flexibility for testing
* Aspect Oriented Programming: Separation between business logic and others.
* MVC architecture
* REST API 설계는 HTTP를 통해 리소스를 표현하고 접근하기 위한 인터페이스를 정의하는 과정
  * 요청의 종류에 따라 GET, POST, PUT, DELETE 등으로 분류하고, 요청하는 URI을 설정한다.
* Controller 작성은 해당 API 엔드포인트를 처리하는 로직을 개발하는 단계
  * 서비스의 로직을 실행하고 결과 값을 받아서 유저에게 보내준다.

## 2주차
* Bean Singleton vs. Prototype:
  * Bean Singleton: 스프링 컨테이너에서 기본적으로 한 번 생성된 빈 객체를 여러 곳에서 공유하여 사용함.
  * Bean Prototype: 요청마다 새로운 빈 객체를 생성하여 사용함.
* Bean @Autowired, @Qualifier, @Primary:
  * @Autowired: 의존성 주입을 자동으로 처리하는 어노테이션.
  * @Qualifier: 여러 빈 중에서 특정 빈을 선택하여 의존성 주입할 때 사용.
  * @Primary: 여러 후보 빈 중에서 기본 빈을 설정할 때 사용.
* Circular Dependency:
  * 클래스 간에 서로 참조하고 의존하는 상황을 나타냄.
  * 스프링에서는 주로 생성자 주입을 통해 해결하며, @Lazy 어노테이션을 사용하여 늦게 초기화할 수 있음.
* DI Testing:
  * DI(Dependency Injection)를 사용하여 의존성을 주입하고, 단위 테스트를 수행함.
  * 스프링 테스트 프레임워크를 활용하여 컨테이너를 생성하고 테스트하는 방법이 포함됨.

## 3주차
UNIQUE KEY, PRIMARY KEY, FOREIGN KEY:

PRIMARY KEY: 테이블에서 유일한 식별자 역할을 하는 열. 중복된 값을 가질 수 없음.
UNIQUE KEY: 중복을 허용하지 않는 열 또는 열의 조합. PRIMARY KEY와 유사하지만 여러 개의 UNIQUE KEY가 테이블에 존재할 수 있음.
FOREIGN KEY: 다른 테이블의 PRIMARY KEY를 참조하여 두 테이블 간의 관계를 정의하는 열.
INDEXING:

CREATE INDEX: 데이터베이스에서 인덱스를 생성하는 명령어. 검색 성능을 향상시키는 데 사용됨.
DROP INDEX: 데이터베이스에서 인덱스를 삭제하는 명령어.
SHOW INDEX: 데이터베이스의 테이블에 대한 인덱스 정보를 조회하는 명령어.
UNIQUE INDEX: 중복 값을 허용하지 않는 인덱스.
TRANSACTION:

데이터베이스 작업의 논리적인 단위. ACID (원자성, 일관성, 고립성, 지속성) 속성을 따라 데이터 일관성을 보장.
시작, 커밋, 롤백 등의 작업으로 구성됨.
여러 개의 SQL 명령을 하나의 트랜잭션으로 묶어 원자적으로 처리.
JPA HIBERNATE:

JPA (Java Persistence API): 자바 애플리케이션에서 객체와 데이터베이스 간의 매핑 및 관리를 위한 API. ORM(Object-Relational Mapping) 기술의 표준 인터페이스.
Hibernate: JPA를 구현한 ORM 프레임워크 중 하나. 객체와 데이터베이스 간의 매핑, 쿼리 작성, 트랜잭션 관리 등을 제공.
Hibernate는 JPA를 기반으로 하며, 더 많은 기능과 확장성을 제공하는 ORM 도구 중 하나로 널리 사용됨.

## 4주차
사용자 인증과 인가: Spring Security는 다양한 인증 방법(폼 기반, 기본 인증, OAuth 등)과 권한 부여를 제공하여 안전한 로그인 및 페이지 접근을 보장합니다.

CSRF 및 XSS 방어: 애플리케이션 보안을 강화하기 위해 Cross-Site Request Forgery(CSRF) 및 Cross-Site Scripting(XSS) 공격으로부터 보호합니다.

세션 관리: 세션 효과적으로 관리하여 세션 공격으로부터 보호합니다.

사용자 정의 필터 및 핸들러: 요청에 대한 커스텀 로직을 적용하여 보다 복잡한 시나리오에 대응할 수 있습니다.

## 5주차

Spring Boot에서 OAuth 2.0 설명:
의존성 추가: Spring Boot 애플리케이션에 OAuth 2.0을 추가하기 위해 pom.xml 파일에 필요한 의존성을 추가합니다.

GitHub 설정: GitHub에서 OAuth 애플리케이션을 등록하고, 발급받은 클라이언트 ID와 시크릿을 Spring Boot 애플리케이션의 설정 파일에 추가합니다.

컨트롤러 작성: OAuth 로그인을 처리할 컨트롤러를 작성합니다. 사용자 정보는 OAuth2User 객체를 통해 얻을 수 있습니다.

GitHub Actions 설명:
워크플로우 파일 작성: GitHub Actions를 사용하기 위해 .github/workflows 디렉토리에 워크플로우 YAML 파일을 작성합니다.

이벤트 설정: 특정 이벤트(예: 코드 푸시)가 발생했을 때 워크플로우가 실행되도록 설정합니다.

작업 정의: 워크플로우는 하나 이상의 작업으로 구성되며, 각 작업은 GitHub Actions에서 제공하는 여러 액션을 사용하여 정의됩니다.

실행 환경 설정: 작업이 실행될 환경(예: Ubuntu, Java 버전)을 설정합니다.

스크립트 실행: 각 작업은 스크립트 또는 명령어를 실행하여 빌드, 테스트, 배포 등을 수행합니다.

워크플로우 실행: 작업이 설정한 이벤트가 발생하면, GitHub에서 해당 워크플로우가 자동으로 실행되고 진행 상황을 확인할 수 있습니다.

## 6주차
Amazon EC2 (Elastic Compute Cloud):

EC2는 가상 서버를 제공하는 서비스로, 다양한 운영 체제에서 실행되는 가상 머신(인스턴스)을 쉽게 프로비저닝할 수 있습니다.
사용자는 필요에 따라 인스턴스 크기를 조절하거나, 여러 가용 영역에 분산하여 가용성을 확보할 수 있습니다.
Amazon S3 (Simple Storage Service):

S3는 객체 스토리지 서비스로, 웹상에서 언제든지 어디서든 데이터를 저장하고 검색할 수 있습니다.
정적 웹 호스팅, 백업 및 복원, 대용량 파일 전송 등 다양한 용도로 사용됩니다.
Amazon RDS (Relational Database Service):

RDS는 관계형 데이터베이스를 호스팅하기 위한 서비스로, MySQL, PostgreSQL, Oracle, SQL Server 등 다양한 데이터베이스 엔진을 지원합니다.
자동 백업, 확장성 및 관리의 용이성을 제공하여 개발자가 데이터베이스에 더 집중할 수 있도록 합니다.
기타 AWS 서비스:

Lambda: 서버리스 컴퓨팅을 제공하는 서비스로, 코드 실행을 관리하고 스케일링을 자동으로 처리합니다.
SNS (Simple Notification Service): 애플리케이션에서 이벤트를 관리하고, 이벤트에 따라 메시지를 전송하고, 푸시 알림을 제공하는 서비스입니다.
Route 53: DNS 및 도메인 등록 서비스로, 안전하고 안정적인 도메인 네임 시스템을 제공합니다.
Elastic Beanstalk: 애플리케이션을 배포하고 운영하기 쉽게 하는 PaaS(Platform as a Service) 서비스입니다.

## 7주차
Redis는 인메모리 데이터 구조 스토어로서, 데이터를 메모리에 저장하고 빠르게 검색하고 분석하는 데 사용되는 오픈 소스 데이터베이스입니다. Spring Boot 애플리케이션에서 Redis를 사용하면 데이터 캐싱, 세션 관리, 메시지 브로커 등 다양한 용도로 활용할 수 있습니다.

Redis의 주요 특징:
인메모리 데이터 스토어: 데이터를 메모리에 저장하여 빠른 읽기 및 쓰기 성능을 제공합니다.

다양한 데이터 구조 지원: 문자열, 해시맵, 리스트, 셋, 정렬된 셋 등 다양한 데이터 구조를 지원하여 유연한 데이터 모델링이 가능합니다.

지속성 및 스냅샷: 지속성을 제공하여 디스크에 데이터를 저장하고, 스냅샷 기능으로 특정 시점의 데이터 상태를 저장할 수 있습니다.

키-값 저장소: 데이터는 고유한 키에 매핑되어 저장되며, 키를 사용하여 데이터를 검색합니다.
