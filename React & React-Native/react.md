```
 "error": "could not prepare statement
 [Schema \"SYSTEM\" not found; SQL statement:\nselect next value for system.uuid [90079-224]]
 [select next value for system.uuid]; SQL [select next value for system.uuid]",
 "data": null
```
system.uuid 가 정의되어 있지 않아 null 나온거 같다.
- system.uuid -> system-uuid 수정(오타 주의하기)
#
#### http://localhost:9090 서버에러
코드에 문제가 없는거 같은데 서버가 안열린다.
```
http://localhost:9090/test//testRequestBody  <- / 두번 사용해서 오류(오타 주의해라)
```
#
#### event.preventDefault();
- event.preventDefault();를 사용하지 않으면  
  submit 됨과 동시에 창이 다시 실행되어 초기 화면으로 돌아오게 된다
#
#### 404 Not Found (요청경로가 잘못됨)
- call("요청경로") -> 요청경로가 없거나 오타
#
#### ssh에러 https로 접속 시도해서 에러 발생
```
react에서 axios.get('https://localhost:9090/api/books' 부분
axios.get('http://localhost:9090/api/books' 수정
```
#

### pathname Error
![pathNameError](https://github.com/user-attachments/assets/10f81d5e-313f-49b3-a142-2b389ba1fedb)
```
import { BrowserRouter as Route, Routes, Router } from "react-router-dom"; //error reason 

return (
      <Router> 
        <Routes>
          <Route path='' element={< />} />
          <Route path='' element={< />} />
          <Route path='' element={< />} />
        </Routes>
      </Router>
  )
```
- Routes 와 Route는 BrowserRouter또는 Router로 반드시 감싸야 한다.
- import에서 "BrowserRouter as Route" BrowserRouter를 Route로 정의하고 사용했기 때문에 에러발생
```
import { BrowserRouter as Router, Routes, Route } from "react-router-dom"; //수정 후
```
#

