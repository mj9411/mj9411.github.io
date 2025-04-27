
# Springframework 특징 3가지

## 제어역전 IOC
-  제어의 역전(IoC)은 **객체를 누가 만들고 관리하는가**
-  스프링이 대신 객체를 생성하고 관리해줌
-  개발자는 객체가 **필요하다는 것만** 표현하면 됨.

```java
// 옛날식
Service service = new Service();
Controller controller = new Controller(service);
```

```java
// new
@Component
public class Service {}

@Component
public class Controller {
    private final Service service;

    @Autowired
    public Controller(Service service) {
        this.service = service;
    }
}
```

## 의존성 주입 DI
  제어 역전 방법 중의 하나 
- **생성자를 통한 의존성 주입**
-  필드 객체 선언을 통한 의존성 주입
-  setter 메서드를 통한 의존성 주입

## 관점 지향 프로그래밍(AOP)
- 중복되는 코드를 줄여보자, 목적에 해당되는 중복되는 코드를 걷어내서 사용하자
1. 컴파일 과정에 삽입
2. 바이트코드를 메모리에 로드하는 과정에 삽입하는 방식
3. 프락시 패턴 이용

# SpringBoot의 4가지 특성
## 의존성 관리 
- spring-boot-starter

## 자동 설정 
- springboot는 springframewark의 기능을 사용하기 위한 자동설정(AutoConfiguration)을 지원

## 내장 WAS 
- spring-boot-starter-web 에 tomcat 내장

## 모니터링 
- 스레드, 메모리, 세션 등 요소들 관리를 spring boot actuator 라는 자체 모니터링 도구에서 지원
