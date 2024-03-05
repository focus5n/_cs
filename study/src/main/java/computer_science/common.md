# 공통 지식

## 객체지향 프로그래밍

### 단일책임

    1. 클래스 혹은 모듈이 변경되는 이유는 단 하나여야만 한다.
    2. ex) 자동차 클래스는 자동차의 요소 및 동작에 대한 정보만 지닌다.
    3. ex) 연료소모량 기록, 운전자에게 정보표현 등 기능은 다른 곳에서 구현한다.

### 개방폐쇄

    1. 기존 코드를 수정하지 않고 새로운 기능을 추가할 수 있어야 한다.
    2. 추상화 (상속, 추상 클래스, 인터페이스) (빈, DI)
    3. 다형성

### 메서드 오버로딩

    1. 같은 이름의 메서드를 여러 개 정의
    2. 매개변수 타입, 개수를 다르게 함으로써 구현

### 메서드 오버라이딩

    1. 상속받고
    2. 상위 클래스의 메서드를 하위 클래스에서 새로운 내용으로 재정의

### 리스코프 치환

    1. 상속된 구현체가 있을 경우,
    2. 부모 클래스를 의존하다가 자식 클래스를 의존하더라도
    3. 어떠한 수정도 거치지 않더라도
    4. 작동에는 아무런 문제가 없어야 한다.

### 인터페이스 분리

    1. 인터페이스에는 관련된 최소한의 구현체를 연결한다.
    2. 사용자는 그리함으로써 불필요한 구현체를 의존하지 않는다.

### 의존역전

    1. 구현체가 아니라 인터페이스에 의존해야 한다.

## OSI, Open Systems Interconnection

    *. 7 계층
    1. 물리 (Physical)
        1-1. 데이터전송을 위한 물리적 매개체를 다룸.
        1-2. 전기신호
        1-3. 광섬유
        1-4. 무선
        1.5. 프로토콜 없음.
        1-6. 하드웨어 표준을 따름.
    2. 데이터링크 (Data Link)
        2-1. 물리적인 매개체를 통해 신뢰성 있는 데이터 전송을 보장.
        2-2. 프레임 전송
        2-3. 오류 검출
        2-4. 오류 수정
        2-5. Ethernet
        2.6. IEEE 802.11 (Wi-Fi)
        2.7. PPP (Point-to-Point Protocol)
        2.8. HDLC (High-Level Data Link Control)
        2.9. ATM (Asynchronous Transfer Mode)
    3. 네트워크 (Network)
        3-1. 다양한 네트워크 간 경로 선택
        3-2. 패킷 전송
        3-3. 라우팅
        3-4. 패킷 전달
        3-5. IP 주소 할당
        3-6. IP (Internet Protocol)
        3-7. ICMP (Internet Control Message Protocol)
        3-8. ARP (Address Resolution Protocol)
        3-9. RARP (Reverse Address Resolution Protocol)
        3-0. OSPF (Open Shortest Path First)
        3-1. BGP (Border Gateway Protocol)
    4. 전송 (Transport)
        4-1. 데이터를 종단 간의 신뢰성 있게 전송 (7 계층 내부 전송)
        4-2. 연결 설정
        4-3. 흐름 제어
        4-4. 오류 복구
        4-5. TCP (Transmission Control Protocol)
        4-6. UDP (User Datagram Protocol)
        4-7. SCTP (Stream Control Transmission Protocol)
    5. 세션 (Session)
        5-1. 통신 세션을 설정하고 관리한다.
        5-2. 세션 생성
        5-3. 세션 유지
        5-4. 세션 종료
        5-5. ISO 8327 / CCITT X.225 / RFC 1001, 1002
        5-6. RPC (Remote Procedure Call)
        5-7. NetBIOS (Network Basic Input/Output System)
    6. 표현 (Presentation)
        6-1. 데이터 표현을 담당한다.
        6-2. 서로 다른 데이터 형식 간의 변환을 수행한다.
        6-3. 암호화
        6-4. 압축
        6-5. 인코딩
        6-6. SSL (Secure Sockets Layer) / TLS (Transport Layer Security)
        6-7. JPEG (Joint Photographic Experts Group)
        6-8. MPEG (Moving Picture Experts Group)
        6-9. ASCII (American Standard Code for Information Interchange)
        6-0. Unicode
    7. 응용 (Application)
        7-1. 사용자와 직접 상호작용하는 프로그램에 서비스를 제공한다.
        7-2. 다양한 프로토콜 사용 (HTTP, FTP, SMTP)
        7-3. HTTP (Hypertext Transfer Protocol)
        7-4. FTP (File Transfer Protocol)
        7-5. SMTP (Simple Mail Transfer Protocol)
        7-6. POP3 (Post Office Protocol Version 3)
        7-7. IMAP (Internet Message Access Protocol)
        7-8. DNS (Domain Name System)
        7-9. DHCP (Dynamic Host Configuration Protocol)

## TCP, Transmission Control Protocol

    1. 신뢰성
        1-1. 패킷의 순서를 보장
        1-2. 재전송 및 오류제어 기능 제공
    2. 연결지향
        2-1. 연결 설정 후 유지한 후 데이터 전송
        2-2. 3-Way Handshake / 4-Way Handshake 방식으로 연결 및 해제
    3. 흐름제어
        3-1. 수신자가 처리할 수 있는 속도에 따라서 데이터의 전송속도 조절가능
    4. 혼잡제어
        4-1. 네트워크 혼잡상태를 감지
        4-2. 혼잡상태에서 데이터 전송 속도 조절
        4-3. 데이터 손실 및 지연 최소화

## IP

    *. OSI 모델 네트워크 계층

    1. 데이터 전송용 프로토콜
    2. 인터넷 상에서 데이터 패킷을 주고받는 데 사용
    3. 각 패킷은 출발지 및 목적지 IP 주소를 포함
    4. 주소 지정
        4-1. 네트워크 상 각 호스트(컴퓨터)에게 고유한 주소를 할당.
        4-2. 고유한 주소를 바탕으로 출발지 및 목적지 식별.
        4-3. IPv4: 32bit 주소
        4-4. IPv6: 128bit 주소
    5. 라우팅
        5-1. 데이터 패킷을 목적지까지 안전하게 전달하기 위함.
        5-2. 다양한 경로 중 목적지까지 최적경로를 선택.
    6. 패킷 전달
        6-1. 패킷을 분할하여 전달할 수 있는 기능 제공.
        6-2. 큰 데이터를 작은 패킷을 분할하여 전송 가능.
        6-3. 수신 측에서 재조립하여 데이터 복원 가능.
    7. 상태없음
        7-1. 각 패킷은 독립적으로 처리.
        7-2. 이전 패킷과 연결이나 상태 정보를 기억하지 않음.
        7-3. 네트워크 확장성 향상 및 오류 복구에 도움.

## HTTP

    1. 요청
    2. 응답
    3. 웹 리소스
    4. Stateless
    5. Connectionless
    6. Text Protocol
        6-1. TCP/IP 프로토콜 위에서 동작
        6-2. HTTP/1.1 : 기본적으로 지속적인 연결이 지원
        6-3. HTTP/2.0 : 멀티플렉싱 및 헤더압축 제공
    7. HTTP Method

## Rest

    1. HTTP 프로토콜 기반
    2. Resource, 자원
        2-1. 모든 것을 자원으로 표현한다.
        2-2. 자원은 고유한 식별자를 가진다. (URI)
    3. Verb, 행위
        3-1. HTTP 메서드를 활용하여 자원에 대한 행위를 정의한다. (GET, POST, PUT, DELETE)
    4. Representation, 표현
        4-1. 자원의 상태를 특정 양식으로 전달. (XML, JSON ...)
    5. Stateless, 상태
        5-1. 요청에 대한 응답이 전해지면 상태를 유지하지 않는다.

## Restful API

    1. Resource-Oriented, 자원지향
    2. HTTP Method
    3. Representational State
    4. Stateless
    5. Cachable
        5-1. 클라이언트는 서버에서 받은 응답을 캐싱할 수 있어야 한다.