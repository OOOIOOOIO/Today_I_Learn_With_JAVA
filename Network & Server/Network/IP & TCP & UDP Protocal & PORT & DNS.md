# IP(Internet Protocol)

- IP는 osi 7계층 중 3계층인 네트워크 계층에서 사용하는 프로토콜이다.
- iP는 서로 다른 운영체제 등을 쓰는 다양한 컴퓨터들이 서로 통신할 때 사용하는 약속된 데이터 이동 간의 규약이다.
- 인터넷에서 이메일을 확인하거나, 파일을 전송하는 등 모든 행위를 할 때 컴퓨터(서버) 간에 데이터 전송이 이루어지게 되는데, 이러한 데이터 통신에 대한 규약을 IP(인터넷 프로토콜)이라고 한다.

<br>

![IP 패킷 정보](https://user-images.githubusercontent.com/74396651/178098016-16428707-6438-43d4-8189-e251ff73362a.png)

<br>

# IP 주소
- 각 컴퓨터는 고유 주소를 가지고 있다. 컴퓨터를 식별하여 데이터를 보내거나 받을 수 있는데, 이 때 컴퓨터의 고유 주소인 IP주소를 사용한다.
- 데이터를 전달할 때 패킷이라는 통신 단위를 통해 전달하는데, IP 패킷에는 출발지 IP, 목적지 IP, 전송하는 데이터 등이 포함되어 있다.

<br>

# IP의 한계
- ### 비연결성
   - 패킷을 받을 대상이 없거나 서비스 불능 상태여도 패킷을 전송한다.

- ### 비신뢰성
   - 에러제어와 흐름제어를 하지 않는다.
   - 중간에 패킷이 소실 되거나 패킷 전달 순서에 문제가 발생할 때 조절해주는 작업을 하지 않는다.

- ### 프로그램 구분
   - 같은 IP를 사용하는 서버에서 통신하는 애플리케이션이 여러개일 때 문제가 발생한다.

<br>
<hr>
<br>

# TCP(Transmission Control Protocol)
- osi 7계층 중 4계층인 전송 계층에서 사용하는 프로토콜이다.
- TCP는 네트워크 망에 연결된 컴퓨터 프로그램 간 데이터를 순서대로, 에러 없이 교환할 수 있게 도와주는 역할을 한다.

<br>

# TCP의 특징
- 연결지향
   - 3 way handshake(가상 연결)
   - 물리적으로 전용회선이 연결되어 있는 것처럼 논리적인 연결을 통해 데이터를 주고받음
   - 4 way handshake를 통해 연결 해제
- 순서 보장
   - 순서가 잘못되어 도착한 경우 수신 호스트가 송신 호스트에게 잘못된 지점부터 다시 전송해달라고 요청
- 데이터 전달 보증
   - 메세지가 중간에 누락되면 알 수 있다.
   - 접속 요청을 하고 이에 대해 요청을 수락하며 데이터를 잘 받았다고 응답한다.
- 흐름제어 및 혼잡제어
- TCP 세그먼트 안에 전송제어 정보, 순서 정보, 검증 정보들이 포함되어 있기 때문에 신뢰할 수 있는 프로토콜이며 대부분 TCP를 사용한다.

<br>

![TCP/IP 패킷 정보](https://user-images.githubusercontent.com/74396651/178098876-4e8816b7-2f3f-4ce2-a71b-d920b8e934cf.png)

<br>

![3 way handshake](https://user-images.githubusercontent.com/74396651/178098510-1b695f5b-8edb-4123-a7ef-4a9b398c4b1f.png)

<br>
<hr>
<br>

# UDP(User Datagram Protocol)
- osi 7계층 중 4계층인 전송 계층에서 사용하는 프로토콜이다. 사용자 데이터그램 프로토콜이다.

<br>

# UDP의 특징
- 데이터 제어에 관한 기능이 거의 없다.
   - 오직 전송 계층에서 애플리케이션에 데이터를 분배하는 역할만 한다.
- 연결지향 X
- 순서 보장 X
- 데이터 전달 보증 X
- 단순하고 빠름
- 애플리케이션에서 추가 작업이 필요하다.
- IP와 거의 같다. PORT 번호와 체크섬 정도만 추가된 정도이다.
- 신뢰성이 없기 때문에 데이터 전송을 보장하지 못하지만 실시간 서비스(Streaming) 등과 같이 신뢰성보다는 연속성, 성능이 중요한 서비스에 자주 사용된다.

<br>

![image](https://user-images.githubusercontent.com/74396651/178098744-8d7abfd0-b4ae-4ebb-87d0-63f8e0a58eed.png)

<br>
<hr>
<br>

# PORT

<br>

![PORT](https://user-images.githubusercontent.com/74396651/178098861-0b0317c5-ff6d-4131-842d-ef1933fba349.png)

<br>

- 포트는 "접속 장소"라고 할 수 있다. 특시 TCP/IP 프로토콜을 사용할 때 클라이언트가 네트워크 상의 특정 서버 프로그램을 지정하는 방법으로 사용된다.
- <code>IP</code>는 출발지 서버와 목적지 서버라면, <code>PORT</code>는 그 서버 안에서 돌아가는 애플리케이션을 구분하는 것이라고 할 수 있다.
- <code>IP</code> : 아파트
- <code>PORT</code> : 몇 동 몇 호
- 라고 생각하면 쉽게 이해할 수 있다.

<br>

### 자주 사용하느 포트번호
- 0 ~ 65535 할당 가능
- 0 ~ 1023 : 잘 알려진 포트, 사용하지 않는 것이 좋다.
   - FTP : 20, 21
   - TELNET : 23
   - HTTP : 80
   - HTTPS : 443

<br>
<hr>
<br>

# DNS(Domain Name System)
- IP는 기억하기 어렵고(192.000.000.7), 변경될 수 있기 때문에 <code>www.naver.com</code>과 같은 호스트 네임을 쓴다.
- 하지만 컴퓨터는 호스트 네임을 알아듣지 못한다. 
- 따라서 호스트 네임을 IP주소로 변환해주는 서비스가 필요한데 이것이 바로 DNS이다.
- DNS는 계층 구조를 가지는 분산데이터베이스 구조이다.

<br>

## DNS 기본 동작 과정

![image](https://user-images.githubusercontent.com/74396651/178099066-c50c6ef9-9111-48b5-9a83-b394c5700ad1.png)

<br>

1. PC 브라우저를 통해 <code>www.naver.com</code>이라는 호스트 네임에 접근 요청한다.
2. Local DNS에 해당 IP 주소가 있는 경우 바로 IP 주소를 PC에 보내준다.  만약 없는 경우 Root DNS 서버에 해당 도메인에 대한 IP 주소를 알려달라고 요청한다.
3. Root DNS는 해당 정보가 없기 때문에, "com 도메인"을 관리하는 DNS 서버의 주소를 전달해준다
4. Local DNS는 com DNS 서버에게 해당 도메인에 대한 IP 주소를 알려달라고 요청한다
5. com DNS 또한 해당 정보가 없기 때문에, "naver.com 도메인"을 관리하는 DNS 서버의 주소를 전달해준다
6. Local DNS는 naver.com DNS 서버에게 해당 도메인에 대한 IP 주소를 알려달라고 요청한다
7. naver.com DNS 서버에는 요청한 호스트네임 <code>www.naver.com</code>에 대한 IP 주소가 존재하므로 Local DNS에게 IP 주소를 넘겨주며 응답한다.
8. 이를 수신한 Local DNS는 <code>www.naver.com</code>에 대한 IP 주소를 캐싱하고 그 IP 주소 정보를 단말(PC)에 전달한다

-> Local DNS 서버가 여러 DNS 서버를 차례대로 물어봐서, 그 답을 찾아가는 과정을 Recursive Query(재귀적 질의) 라고 한다.




<br>
<br>
<br>

참조 : 인프런 김영한님 강의


