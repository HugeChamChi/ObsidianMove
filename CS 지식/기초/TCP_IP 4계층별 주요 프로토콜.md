## 1. 응용 계층 (Application Layer)

- **역할**: 사용자와 가장 가까운 계층. 실제 응용 프로그램(웹, 메일, 파일전송 등)이 사용하는 데이터 형식과 통신을 담당함.
    
- **주요 프로토콜**:
    
    - **TELNET**: 원격 로그인
        
    - **FTP**: 파일 전송
        
    - **SMTP**: 이메일 전송
        
    - **SNMP**: 네트워크 관리
        
    - **E-Mail**: 이메일 서비스
        
    - **HTTP, HTTPS, DNS, SSH** 등도 포함됨.
        
- **예시**: 웹브라우저, 메일 클라이언트, 파일전송 프로그램 등
    

## 2. 전송 계층 (Transport Layer)

- **역할**: 데이터의 신뢰성 있는 전송, 흐름 제어, 오류 제어, 포트번호를 통한 응용프로그램 구분
    
- **주요 프로토콜**:
    
    - **TCP**(Transmission Control Protocol): 연결지향, 신뢰성 보장, 데이터 순서 보장, 재전송 지원
        
    - **UDP**(User Datagram Protocol): 비연결지향, 빠른 전송, 신뢰성 보장 안함
        
- **예시**: 웹(HTTP)과 메일(SMTP)은 TCP, 실시간 스트리밍은 UDP 사용
    

## 3. 인터넷 계층 (Internet Layer)

- **역할**: 네트워크 간 데이터 전송, 논리적 주소(IP 주소) 지정 및 라우팅(경로 설정)
    
- **주요 프로토콜**:
    
    - **IP**(Internet Protocol): 패킷의 주소 지정과 전달
        
    - **ICMP**(Internet Control Message Protocol): 네트워크 진단, 오류 메시지(예: ping)
        
    - **IGMP**(Internet Group Management Protocol): 멀티캐스트 그룹 관리
        
    - **ARP**(Address Resolution Protocol): IP ↔ MAC 주소 변환
        
    - **RARP**(Reverse ARP): MAC → IP 주소 변환
        
- **예시**: 인터넷 통신, 네트워크 진단(ping), 주소 변환 등
    

## 4. 네트워크 액세스 계층 (Network Access Layer)

- **역할**: 실제 물리적 네트워크에서 데이터 전송, 프레임화, 에러 검출, MAC 주소 사용
    
- **주요 프로토콜**:
    
    - **Ethernet**: 유선 LAN 표준
        
    - **IEEE 802**: 다양한 LAN 표준(802.3=Ethernet, 802.11=Wi-Fi 등)
        
    - **HDLC, X.25, RS-232C**: WAN, 시리얼 통신 등 다양한 하드웨어/링크 프로토콜
        
- **예시**: 스위치, 브릿지, 허브 등 장비에서 실제 데이터 전송
    

## 요약 표

|계층|주요 프로토콜 예시|주요 역할|
|---|---|---|
|응용 계층|TELNET, FTP, SMTP, SNMP, HTTP, DNS, E-Mail 등|사용자 서비스, 응용프로그램 통신|
|전송 계층|TCP, UDP|신뢰성, 데이터 전송, 포트 관리|
|인터넷 계층|IP, ICMP, IGMP, ARP, RARP|주소 지정, 라우팅, 오류 메시지|
|네트워크 액세스 계층|Ethernet, IEEE 802, HDLC, X.25, RS-232C 등|실제 데이터 전송, 프레임화|


![[Pasted image 20250513173300.png]]

