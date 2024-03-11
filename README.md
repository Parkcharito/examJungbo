-----------------------------------------------------------------------------------

# 정보처리기사 필기

-----------------------------------------------------------------------------------

## 데이터 입출


### 모듈(Module)

모듈이란 프로그램을 구성하는 시스템을 기능 단위로 독립적인 부분으로 분리한 것이다. 단순히 규모가 큰 것을 작게 여러 개로 나눈 조각이 아니라, 하나 이상의 논리적인 기능을 수행하기 위한 명령어들의 집합이라 할 수도 있다. 모듈은 독립적인 프로그램 그 자체일 수도 있고 함수나 메서드일 수도 있다. 모듈이 되려면 다른 것들과 구분될 수 있는 독립적인 기능을 가져야 하고 유일한 이름을 사용해야 한다. 그리고 다른 프로그램이나 또 다른 모듈에서 호출하여 사용할 수도 있어야 한다. 또, 모듈 자체로서 재사용될 수 있고 독립적으로 컴파일이 가능해야 한다는 중요한 특징을 포함해야 한다. 따라서 모듈은 다양한 형태로 존재할 수 있는데 용도가 비슷한 함수나 추상화된 자료, 객체(Object), 메서드(Method)등이 이에 해당한다.

### 컴포넌트

컴포넌트(Component)란 프로그래밍에 있어 재사용이 가능한 각각의 독립된 모듈을 뜻한다.

그림에서 확인 할 수 있듯이 컴포넌트 기반 프로그래밍을 하면 마치 레고 블록처럼 이미 만들어진 컴포넌들을 조합하여 화면을 구성할 수 있다.

-----------------------------------------------------------------------------------

### 소프트웨어 생명 주기

#### 폭포수 모형
: S/W 개발 생명주기에 기반하고 있는 소프트웨어 개발 기법중 하나
한 번 떨어지면 다시 거슬러 올라갈 수 없는 폭포수처럼, 각 개발 단계를 확실히 매듭 짓고 다음 단계로 넘어간다는 의미
#### 프로토타입 모형
#### 나선형 모형

-----------------------------------------------------------------------------------

### 애자일 모형
### 스크럼


-----------------------------------------------------------------------------------
### 관계대수 / 관계해석

#### 관계대수
: 관계형 데이터베이스에서 원하는 정보와 그 정보를 검색하기 위해 어떻게 유도하는가를 기술하는 절차적인 언어
* Select, Project, Join, Division등이 있음

##### Select
: 릴레이션에 존재하는 튜플 중 선택 조건을 만족하는 튜플의 부분집합을 구하여 새로운 릴레이션을 만드는 연산
* 연산자의 기호는 그리스 문자 σ시그마를 사용

##### Project
: 주어진 릴레이션 속성 리스트에 제시된 속성 값만을 추출하여 새로운 릴레이션을 만드는 연산
* 연산자의 기호는 그리스 문자 π 파이를 사용
* 결과에 중복이 발생할 시 중복제거

##### Join
: 공통 속성을 중심으로 두 개의 릴레이션을 하나로 합쳐서 새로운 릴레이션을 만드는 연산
* 연산자의 기호는 ⋈을 사용
* Join 조건이 '='인 경우 동일한 속성이 있으면 두 번 나타나게 된다

##### Division
: X ⊃ Y 인 두개의 릴레이션 R(X)와 S(Y)가 있을 때, R의 속성이 S의 속성 값을 가진 튜플에서 S가 가진 속성을 제외한 속성만을 구하는 연산
* 연산자의 기호는 ÷을 사용
* 표기 형식은 R[속성r ÷ 속성s]S 이다
* 속성 r은 릴레이션 R에 속하는 속성, 속성 s는 릴레이션 S에 속하는 속성 값을 가지는 속성이어야함


### 정리
* SELECT σ시그마
* PROJECT π파이
* JOIN ▷◁ 나비넥타이
* DIVISION ÷나누기


-----------------------------------------------------------------------------------

#### 가상기억장치
: 보조기억장치의 일부를 주기억 장치처럼 사용하는 것
* 용량이 작은 주기억장치를 마치 큰 용량을 가진 것처럼 사용할 수 있음
* 프로그램을 여러 작은 블록 단위로 나누어서 가상기억장치에 불연속적으로 할당하여 처리
* 주기억장치의 이용률과 다중 프로그래밍의 효율 상승
* 가상기억장치에 저장된 프로그램을 실행하려면 가상기억장티의 주소를 주기억장치의 주소로 바꾸는 주소 변환 작업이 필요
* 연속 할당 방식에서 발생할 수 있는 단편화를 해결할 수 있음

#### 페이징 기법
: 가상기억장치에 보관되어 있는 프로그램과 주기억장치의 영역을 동일한 크기로 나눈 후 나눠진 프로그램을 동일하게 나눠진 주기억장치의 영역에 적재시켜 실행하는 기법
* 프로그램을 일정한 크기로 나눈 크기를 페이지라 하고 페이지 크기로 일정하게 나누어진 주기억장치의 단위를 페이지 프레임이라고 함
* 외부 단편화는 발생하지 않으나 내부 단편화는 발생할 수 있음
* 매핑작업을 위해서 페이지 맵 테이블이 필요함
* 페이지 맵 테이블 사용으로 비용이 증가되고 처리 속도가 감소됨

#### 세그먼트 기법
: 가상기억장치에 보관되어 있는 프로그램을 다양한 크기의 논리적인 단위로 나눈 후 주기억장치에 적재시켜 실행시키는 방법
* 프로그램을 논리적인 크기로 나눈 단위를 세그먼트라고 함
* 내부 단편화는 발생하지 않으나 외부 단편화는 발생할 수 있음
* 매핑작업을 위해서 세그먼트 맵 테이블이 필요함

 
-----------------------------------------------------------------------------------

### 프로토콜
: 서로 다은 기기들간의 데이터 교환을 원할하게 수행할 수 있도록 표준화시켜 놓은 통신 규약

#### 프로토콜의 기본 요소

##### 구문 
: 전송하고자 하는 데이터의 형식, 부호화, 신호 레벨 등을 규정

##### 의미
: 두 기기 간의 효율적이고 정확한 정보 전송을 위한 협조 사항과 오류 관리를 위한 제어 정보를 규정

##### 시간
: 두 기기 간의 통신 속도, 메시지의 순서 제어 등을 규정

#### 프로토콜의 기능

##### 단편화와 재결합
: 송신 측에서 전송할 데이터를 전송에 알맞은 작은 크기의 블록으로 자르는 작업

##### 재결합
: 수신 측에서 수신한 단편화된 데이터를 다시 모으는 작업

##### 캡슐화
: 단편화 된 데이터에 주소, 오류 검출 코드, 프로토콜 제어 정보를 부가하는 것

##### 흐름제어
: 수신 측에서 송신 측의 데이터 전송 속도나 전송량을 제어할 수 있는 기능
: 정지-대기 방식이나 슬라이딩 윈도우 방식을 이용

##### 오류제어
: 전송 중에 발생하는 오류를 검출하고 정정하여 데이터나 제어 정보의 파손에 대비하는 기능

##### 동기화
: 송수신 측이 같은 상태를 유지하도록 타이밍을 맞추는 기능

##### 순서 제어
: 전송되는 데이터 블록에 전송 순서를 부여하여 연결 위주의 데이터 전송 방식에 사용
: 흐름 제어 및 오류 제어를 용이하게 함

##### 주소 지정
: 데이터가 목적지까지 정확하게 전송될 수 있도록 목적지 이름, 주소, 경로를 부여하는 기능

##### 다중화
: 한 개의 통신 회선을 여러 가입자들이 동시에 사용하도록 하는 기능

##### 경로 제어
: 송수신 측간의 송신 경로 중에서 최적의 패킷 교환 경로를 설정하는 기능

##### 전송 서비스
: 전송하려는 데이터가 사용하도록 하는 별도의 부가 서비스

-----------------------------------------------------------------------------------

## 병행제어
: 다중 프로그램의 이점을 활용하여 동시에 여러 개의 트랜잭션을 병행 수행할 때, 동시에 실행되는 트랜잭션들이 데이터베이스의 일관성을 파괴하지 않도록 트랜잭션 간의 상호 작용을 제어하는 것

### 병행제어의 목적

* 데이터베이스의 공유 최대화
* 시스템 활용도 최대화
* 데이터베이스 일관성 유지
* 사용자에 대한 응답 시간 최소화

### 병행제어 기법의 종류

#### 로킹
: 주요 데이터의 액세스를 상호 베타적으로 하는 것

* 트랜잭션들이 어떤 로킹 단위를 액세스하기 전에 Lock을 요청해서 Lock이 허락되어야만 그 로킹 단위를 액세스할 수 있도록 하는 기법
* 로킹의 대상이 되는 객체의 크기를 로킹 단위라고함
* 데이터베이스도 로킹 단위 가능
* 로킹 단위가 커지면 로크 수가 작아 로킹 오버헤드 감소

#### 타임 스탬프 순서
: 트랜잭션과 트랜잭션이 읽거나 갱신한 데이터에 대해 트랜잭션이 실행을 시작하기 전에 시간표를 부여하여 부여된 시간에 따라 트랜잭션 작업을 수행하는 기법

* 교착상태가 발생하지 않음
* 직렬성 순서를 결정하기 위해 트랜잭션 간의 처리 순서를 미리 선택하는 기법들 중 가장 보편적인 방법

#### 최적 병행수행
: 병행 수행하고자 하는 대부분의 트랜잭션이 판독 전용 트랜잭션일 경우, 트랜잭션 간의 충동률이 매우 낮아서 병행제어 기법을 사용하지 않고 실행되어도 이중의 많은 트랜잭션은 시스템의 상태를 일관성 있게 유지한다는 점을 이용한 기법

#### 다중 버전 기법
: 타임 스탬프의 개념을 이용하는 기법으로 다중 버전 타임스탬프 기법이라고도 함

* 갱신될 때마다 버전을 부여하여 관리

#### 로킹 단위
: 병행제어에서 한꺼번에 로킹할 수 있는 객체의 크기를 의미

* 데이터베이스, 파일, 레코드, 필드 등이 로킹 단위가 될 수 있음
* 로킹 단위가 크면 로크 수가 작아 관리하기 쉽지만 병행성 수준이 낮아지고, 로킹 단위가 작으면 로크 수가 많아 관리하기 복잡해 오버헤드가 증가하지만 병행성 수준이 높아짐

-----------------------------------------------------------------------------------
#### Critical Path Method(CPM, 임계 경로법)
: 네트워크를 중심의 논리적 구성, 시간과 비용 문제를 취급.
프로젝트를 일정 기일 내에 완성시키고 해당 계획이 원가의 최소값에 의해 보증되는 등의 최적 스케줄을 구하는 관리 방법

#### Work Breakdown Structure(업무 분업 구조)
: 성과 목표 완전 달성을 위한 프로그램.
산업 관리 간접 부문의 기술 혁신형 업무-목표를 설정하여 소정 기간, 자원 내에서 달성하는 형태의 업무를 효과적으로 수행하기 위한 수법

#### Risk Analysis
프로젝트에 내재된 요소를 인식하고 그 영향을 분석하여 이를 관리하는 활동으로서,
프로젝트를 성공시키기 위하여 위험요소를 사전에 예측, 대비하는 모든 기술과 활동을 포함하는 것


-----------------------------------------------------------------------------------

 ### 정규화 정리
 
 #### 1정규형
 : 도메인이 원자값으로 구성되어 있다
 
 #### 2정규형
 : 부분 함수 종속 제거(완전 함수적 종속 관계)
 
 #### 3정규형
 : 이행 함수 종속 제거
 
 #### 보이스/코드(BCNF)정규형
 : 결정자가 후보 키가 아닌 함수 종속 제거 
 
 #### 4정규형
 : 다치(다중 값) 종속성 제거
 
 #### 5정규형
 : 조인 종속성 제거



-----------------------------------------------------------------------------------

#### 화이트박스 테스트 기법
문장검증 : 프로그램의 모든 문장이 적어도 한번씩 수행되는 검증
기준선택검증 : 선택하는 부분만 검증
경로검증 : 수행 가능한 모든 경로 검사
조건검증 : 문장 내 조건식을 조사하는 기준


#### 블랙박스 테스트 
: 작동 원리를 모르는 상태에서 '동작을 검사'하는 방식 (사용자 관점의 테스트)
화이트박스 테스트: '내부 소스코드'를 테스트 하는 기법 (개발자 관점의 단위 테스트)

-----------------------------------------------------------------------------------

#### 분산 데이터베이스의 목표
* Location Transparency (위치 투명성)
: 데이터베이스의 실제 위치를 알 필요 없이 단지 데이터베이스의 논리적 명칭만으로 액세스할 수 있음

* Replication Transparency (중복 투명성; 복제 투명성)
: 동일 데이터가 여러 곳에 중복되어 있더라도 사용자는 마치 하나의 데이터만 존재하는 것처럼 사용하고, 시스템은 자동으로 여러 자료에 대한 작업을 수행

* Failure Transparency (장애 투명성)
: 장애가 발생해도 트랜잭션을 정확하게 처리하고 데이터 무결성을 보장함

* Concurrency Transparency (병행 투명성)
: 다수의 트랜잭션들이 동시에 실현되더라도 그 트랜잭션의 결과는 영향을 받지 않음

* Division Transparency (분할 투명성)
: 하나의 논리적 릴레이션이 여러 단편으로 분할되어 각 단편의 사본이 여러 시스템에 저장되어 있음을 인식할 필요가 없음

-----------------------------------------------------------------------------------

* 1계층 - 물리계층(Physical Layer) : Coax, Fiber, Wireless
* 2계층 - 데이터 링크계층(DataLink Layer) : Ethernet, SLIP, PPP, FDDI, HDLC
* 3계층 - 네트워크 계층(Network Layer) : IP, IPSec, ICMP, IGMP
* 4계층 - 전송 계층(Transport Layer) : TCP, UDP, ECN, SCTP, DCCP
* 5계층 - 세션 계층(Session Layer) : VARIOUS API;S, SOCKETS
* 6계층 - 표현 계층(Presentation Layer) : SSL, FTP, IMAP, SSH
* 7계층 - 응용 계층(Application Layer) : HTTP, FTP, IRC, SSH, DNS
* 
-----------------------------------------------------------------------------------



# 정보처리기사 실기




-----------------------------------------------------------------------------------

프로그래밍 활용
-----------------------------------------------------------------------------------

컴파일 (Compile)
컴파일 = 번역
사용자가 작성한 소스코드 파일(.java)을 컴퓨터가 이해할 수 있는 기계어로 번역한다. (.class)
.java를 .class로 변환하는 것
컴파일을 해주는 프로그램을 컴파일러라고 한다.

💡 빌드 (Build)
사용자가 작성한 소스코드 파일(.java)을 컴파일해서 컴파일된 코드(.class)가 되면, 이것을 컴퓨터가 실행할 수 있는 상태로 변환하는 것을 빌드라고 한다.
컴퓨터가 실행할 수 있는 상태란, resource를 .class에서 참조할 수 있는 적절한 위치로 옮기는 등등의 작업을 하는 것이다.
즉, 컴파일된 코드를 실제 실행할 수 있는 상태로 만드는 것이다.
컴파일을 포함하여 war, jar 등의 실행파일을 만드는 과정 또한 빌드라고 부른다.

💡 배포 (Deploy)
실행 가능한 파일을 사용자가 접근할 수 있는 환경에 배치하는 것을 배포라고 한다.
실서버에 반영하는 것이다.


## 기본연산자의 우선순위


1. (),[] : 괄호 / 대괄호
2. !, ~, ++, -- : 부정 / 증감 연산자
3. +, /, % : 곱셈 / 나눗셈 연산자
4. +, - : 덧셈 / 뺄셈 연산자
5. <<, >>, >>> 비트단위의 쉬프트 연산자
6. <, <=, >, >= : 관계 연산자
7. ==, !=
8. & : 비트단위의 논리 연산자
9. ^
10. |
11. && : 논리곱 연산자
12. || : 논리합 연산자
13. ?: : 조건 연산자
14. =, +=, -=, *=, /=, <<=, >>=, &=, ^=, ~= : 대입 / 할당 연산자


