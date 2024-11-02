### package import 오류
- 패키지나 import 할 파일 압축 풀 때 파일 안에 같은 이름의 파일이 있어서 오류  
ex) product/product/...
- 압축 풀 때 "여기에 풀기" 하기
#
### http://localhost:9090 서버가 안열린다.
- 실행은 메인(OOApplication)에서 해야한다.
#
### Repository import 안됨
- 만들 때 class로 만들지 않게 주의 interface로 만들기
#
### 404 Not Found (요청경로가 잘못됨)
```java
@ReController
@RequestMapping("리소스") //리소스가 없거나 오타
Controller{
	@GetMapping("리소스")
	}
```
#
