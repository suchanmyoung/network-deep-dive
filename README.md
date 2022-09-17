# network-deep-dive
#### 네트워크 관련 서적들의 내용을 발췌하여 정리하였으며 출처는 하단에 명시하였음.

<details>
<summary>TCP(Transfer Control Protocol)</summary>

TCP는 트랜스포트 계층에 해당하며 신뢰성 있는 바이트 스트림 서비스를 제공 한다. 바이트 스트림 서비스란 용량이 큰 데이터를 보내기 쉽게 TCP 세그먼트라고 하는 단위 패킷으로 작게 분해하여 관리하는 것을 말한다. 결국 TCP는 대용량의 데이터를 작게 분해해서 보내고, 정확하게 도착했는지 확인하는 역할을 담당한다.

</details>

<details>
<summary>3-way handshaking</summary>

TCP는 상대방에게 정확하게 데이터를 보내기 위해 3-way handshaking 방법을 사용하는데, 이 방법은 패킷을 보내고 바로 끝내는 것이 아니라 보내졌는지 여부를 'SYN', 'ACK' 이라는 TCP 플래그를 사용하여 확인한다.

SYN 패킷 전송(송신 측) > SYN/ACK 패킷 전송(수신 측) > ACK 전송(송신 측)

만약 핸드셰이킹 과정에서 도중에 통신이 끈헝지면 TCP는 같은 수순으로 패킷을 재전송한다.

</details>



출처.
* 그림으로 배우는 HTTP Network BASIC, 우에노 센