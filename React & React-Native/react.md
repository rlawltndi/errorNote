### pathname Error
![pathNameError](https://github.com/user-attachments/assets/10f81d5e-313f-49b3-a142-2b389ba1fedb)
```
import { BrowserRouter as Route, Routes, Router } from "react-router-dom"; //error reason 

return (
      <Router> 
        <Routes>
          <Route path=/' element={< />} />
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

