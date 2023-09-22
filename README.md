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

# 3주차
                                            
