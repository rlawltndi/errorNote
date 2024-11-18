###  css input error
![화면 캡처 2024-11-05 151412](https://github.com/user-attachments/assets/9028b079-6701-4de5-9ff1-c84299061b07)

![화면 캡처 2024-11-05 151431](https://github.com/user-attachments/assets/4e355196-7afc-45ac-bb4d-54b0254cc9d4)

- container 안에 `justity-content: center `에 semicolon(;)이 없어서 생긴 오류
-  ``(backtick) 안에는 semicolon을 사용해야한다.
#
### collection error
![KakaoTalk_20241118_151150315](https://github.com/user-attachments/assets/bd8cf79d-4fb6-49ad-9819-befad06e6f72)

![화면 캡처 2024-11-18 165817](https://github.com/user-attachments/assets/5a6b1015-931e-459a-b192-cdb07371fbc2)
- collection()의 첫번째 인자는 firebase 인스턴스와 컬렉션 이름을 전달해야한다.
```
 //firebase.js에서
 const db = getFirestore(app); //export를 안하고 사용해서 에러 발생
```
```
export const db = getFirestore(app); //수정
```
