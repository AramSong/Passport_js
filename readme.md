## Multi User

* 다중 사용자의 접속(사용자의 추가) : Register
* 해당 사용자가 이미 존재하는 사용자인지 아닌지 체크
* node.js는 비동기식 프로그래밍

## 암호화

* 사용자가 서비스에 비밀번호를 맡겨놓은 상태. 

* 사용자의 비밀번호가 악의적인 사용자에게 넘어갈 경우를 대비
* 사용자의 비밀번호가 유출되면 안됨.
* MD5

![1549950822246](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1549950822246.png)

 * 단방향 암호화 : 원래의 문자를 암호화된 문자로 바꿀수는 있지만 암호화된 문자를 원래의 문자로 복호화할

   수는 없음.

![1549951003217](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1549951003217.png)

* 사용자가 로그인하는 순간에 사용자가 입력한 값을 저장되어있는 비밀번호와 비교할 때, 사용자가 입력한 비밀번호도 md5로 암호화.

* 키 스트레칭?
* PBKDF2

![1549951601111](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1549951601111.png)

![1549951723793](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\1549951723793.png)

1. 첫번째 null : error가 없음

2. 두번째 pass : 비밀번호 111111,원래값

3. 세번째salt : 같은 값을 가지고 있는 데이터가 암호화된 결과를 다르게 하는 것. 어떠한 salt를 썼는지 알아야 hash값과 salt값을 이용해 password를 검사할 수 있음.

4. 네번째hash: 암호화된 해시값