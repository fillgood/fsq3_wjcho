-네트워크

- 컴퓨터네트워크 타입    LAN / MAN / WAN
- 네트웍크구조               Client/Server / Peer to Peer
- 네트워크의 구성           Star / Ring / Bus형(병렬형,주로사용)
- 네트워크통신구성         Intranet / Ethernet / Internet

- LAN (Local Area Network) - 근거리통신망
- MAN(Mertopolitan Area Network) 도시권 통신망
- WAN(Wide Area Network) 광역통신망

인터넷(Internet)

- -컴퓨터로 연결하여 TCP/IP 프로토콜을 이용해 정보를 주고받는 디바이스의 네트워크
- -Inter Network
- -네트워크의 네트워크

TCP/IP 프로토콜

- TCP (Transmission Control Protocol)
- IP (Internet Protocol)
- 인터넷을 통하여 정보를 주고받을때 사용하는 서로간의 약속

WWW

- World Wide Web
- 웹문서들이 있는 정보의 저장소
- 분산과 연결

URL
Uniform Resource Locator
[Protocol]://[Host]:[Port]/[Path]
http://www.daum.net:80/map
해석:다음에 접속해서 웹문서의 정보를 보여달라
ftp://id:pw@192.168.1.10:777/mydir
file://localhost/movie/test.avi

Protocol

- 프로토콜
- 통신규약
- 장비 사이에서 메시지를 주고 받는 양식과 규칙의 체계 즉 동신(네트워킹) 할때 정해진 메세지 규칙
- http.https,ftp,sftp,ssh,ssl,smtp

- HTTP(Hyper Text Transfer Protocol)

Http Method 메소드

ㅇ GET     :
     - URL(URI) 형식으로 웹서버측 데이터를 요청
          부가정보가 주소창에 담겨서 보내짐으로서 정보누출의 위험이 있다
     * Conditional GET (웹브라우저의 캐싱 가능성이 있다 )
        . 최초 리소스를 요청할 때는 요청만 하고, 이후 요청 때는 첫 요청의 응답에 함께 온
          HTTP 헤더 정보를 참고하여, 변경사항이 있는지 물어보는 GET
        . 캐싱에 중요한 HTTP 헤더 정보 : Last-Modified, eTag 등

ㅇ POST    : 내용 전송 (파일 전송 가능)
     - 클라이언트에서 서버로 어떤 정보를 제출함
        . 요청 데이터를 HTTP 바디에 담아 웹서버로 전송함
          웹브라우저의 캐싱하지 않음
        . 만일, 새로이 작성된 리소스이면, 서버측은 HTTP 헤더 항목 중 `Location:`에
          URI 주소 정보를 포함시켜 응답하게 됨

ㅇ PUT     : 내용 갱신 위주 (파일 전송 가능)
     - POST 처럼 정보를 서버로 제출하는 것으로 형식은 동일하나, 갱신 위주 임
        . 이에 의해 갱신 또는 작성된 내용에 대한 주소 정보를
          서버측 응답메세지의 HTTP 헤더 항목 중 `Location:`을 보내지 않아도 됨
        . 즉, 서버측은 클라이언트 측이 제시한 URI를 그대로 사용하는 것으로 간주함
        . 이는 클라이언트측이 서버측 구현에 관여하게되는 것이므로, 통상 POST를 더 많이 씀

ㅇ DELETE  : 파일 삭제
     - 웹 리소스를 제거

ㅇ HEAD    : 메세지 헤더(문서 정보) 취득
     - GET과 비슷하나, 실제 문서를 요청하는 것이 아니라, 문서 정보를 요청
        . 이에따라 응답 메세지에 본문(Body)이 없이 헤더 만을 보냄

ㅇ OPTIONS : 웹서버측 제공 메소드에 대한 질의
     - 가능한 메소드 옵션에 대한 질의
        . 이 경우 응답메세지에 HTTP 헤더 항목 중 `Allow: GET,POST,HEAD` 처럼 보내게 됨

ㅇ TRACE   : (거의 사용 안함)
     - 요청 리소스가 수신되는 경로를 보여줌

ㅇ CONNECT : (거의 사용 안함)
     - 프락시 서버와 같은 중간 서버 경유

FTP(File Transfer Protocol)

TELNET
Terminal NETwork
-원격 로그인을 위한 프로토콜(암호와 되지 않음)

SSH
Secure Shell
네트워크 상의 다름 컴퓨터에 로그인하거나 원격시스템에서 명령을 실행하고 다른 시스템으로 파일을 복사할 수 있도록 해주는
응용프로그램 또는 프로토콜
텔넷의 대용목적(암호와 되어서 움직임)

SSL
Secure Soket Layer
웹서버와 브라우저 사이의 보안을 위한 프로토콜
Htttp 와 https 사용시 기존보다 부하가 많이 생김 ,기존보다 3~4배
시스템교체시 자금소요가 많이 됨

SMTP
Simple Mail Transfer Protocol
전자메일 발송 프로토콜

IP Address
Internet protocol adress
컴퓨터 네트워크에서 장치들이 서로를 인식하고 통신을 하기 위해서 사용하는 번호

Domain Adress
네크워크상에서 컴퓨터를 식별하는 호스트이름

DNS
Domain Name System
호스트의 도메인 이름을 호스트의 네트워크 주소로 바꾸거나 그 반대의 변환을 수행
전화번호부의 역활과 비교함 쉽다..

Port (0~1024 포트까지 사용)
가상의 논리적 통신 연결단
번호로 구분

OSI((Open Systems Interconnection Reference Model) 7 계층이해
URI 개념확인

-암호화

- 대칭키 방식
암호화와 복호화에 같은 암호키를 쓰는 알고리즘
DES,AES,SEED(초기인증서방식) 등
암호키 분실시 정보누출위험

- 공개키방식(비대칭키)
공개키로 암호화된 데이터를 비밀키를 사용하여 복호화 할 수 있는 암호화 알고리즘(암호화키와 복호화키가 다름)
복호화키를 분실시 정보누출위험
RSA(공인인증서의경우) 등

- 해시
임의의 데이터(암호 등)를 고정된 길이의 데이터로 매핑하여 원래의 입력값과의 관계를 찾기 어렵게 만든 것
SHA,MD5등