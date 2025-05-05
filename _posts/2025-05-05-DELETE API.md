
## DELETE API

#### @PathVariable 과 @RequestParam을 활용한 DELETE 메서드 구현
```java
//http://127.0.0.1:8080/api/v2/delete-api/{String 값}  
@DeleteMapping(value = "/{variable}")  
public String DeleteVariable(  
        @PathVariable String variable  
){  
    return variable;  
}
```

#### @RequestParam을 호라용한 DELETE 메서드 구현 ??
```java
//http://127.0.0.1:8080/api/v2/delete-api/request1?email=value  
@DeleteMapping(value = "/request1")  
public String getRequestParam1(  
        @RequestParam String email  
) {  
    return "e-mail : " + email;  
}
```