![[Pasted image 20250612025048.png]]

접속부터해줌 

`npm install socket.io` 를 입력하여 소켓 라이브러리 설치

![[Pasted image 20250612025121.png]]

`vi server.js` server.js 파일을 열어 socket io를 통합시킬예정

![[Pasted image 20250612025547.png]]

각종 라이브러리를 설치했던 `game-auth-server` 에 접속하기.

그리고 여길 참조하여 멀티게임 json 코드 배껴버리깃 

https://wolstar.tistory.com/12

https://github.com/itisnajim/SocketIOUnity

블로그 내용을 보면

1. Socket.IO 클라이언트 라이브러리 설치
2. socket.io 이벤트 리스너에서 받은 응답은 메인 스레드가 아닌 다른스레드에서 처리됨.
   따라서 UI 조작이나 GameObject 활성화 비활성화등 Unity API를 사용하는코드는 메인스레드에서 실행되어야함.
3. 이를 위해 using newtonsoft.Json 구문을 사용하기위해 unity packagemanager 에서 다운받아야함
4. 근데 특정 unity 버전에서는 unity registry 에서 바로보이지않고 add package by name 기능을 이용하여 다운받아야함 .

`com.unity.nuget.newtonsoft-json`

![[Pasted image 20250612031912.png]]


https://github.com/itisnajim/SocketIOUnity/releases

여기에서 다운받은 source code 를 unity 에 import 한다.

![[Pasted image 20250612035436.png]]

근데 다운받았던 socket.io 에서 이런오류가 났는데 netstandared 호환이 안되어서 그런것같으니 
.net framwork 가 범용성은 좋아서 바꾸어봤더니 오류가 사라졌다.


![[Pasted image 20250612035609.png]]


스크립트 짜는데 필요한 명령어들 

```cs
on 수신

emit 전달

join 방에 들어갑니다

leave 방에 나갑니다.
```

![[Pasted image 20250612043516.png]]

출처 : https://wolstar.tistory.com/12



