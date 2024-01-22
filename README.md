-----------------------------------------------------------------------------------


# 정보처리기사 필기


-----------------------------------------------------------------------------------

## 데이터 입출입


### 모듈(Module)

모듈이란 프로그램을 구성하는 시스템을 기능 단위로 독립적인 부분으로 분리한 것이다. 단순히 규모가 큰 것을 작게 여러 개로 나눈 조각이 아니라, 하나 이상의 논리적인 기능을 수행하기 위한 명령어들의 집합이라 할 수도 있다. 모듈은 독립적인 프로그램 그 자체일 수도 있고 함수나 메서드일 수도 있다. 모듈이 되려면 다른 것들과 구분될 수 있는 독립적인 기능을 가져야 하고 유일한 이름을 사용해야 한다. 그리고 다른 프로그램이나 또 다른 모듈에서 호출하여 사용할 수도 있어야 한다. 또, 모듈 자체로서 재사용될 수 있고 독립적으로 컴파일이 가능해야 한다는 중요한 특징을 포함해야 한다. 따라서 모듈은 다양한 형태로 존재할 수 있는데 용도가 비슷한 함수나 추상화된 자료, 객체(Object), 메서드(Method)등이 이에 해당한다.

### 컴포넌트

컴포넌트(Component)란 프로그래밍에 있어 재사용이 가능한 각각의 독립된 모듈을 뜻한다.

그림에서 확인 할 수 있듯이 컴포넌트 기반 프로그래밍을 하면 마치 레고 블록처럼 이미 만들어진 컴포넌들을 조합하여 화면을 구성할 수 있다.

-----------------------------------------------------------------------------------

### 소프트웨어 생명 주기

#### 폭포수 모형
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
* 연산자의 기호는 그리스 문자 시그마를 사용

##### Project
: 주어진 릴레이션 속성 리스트에 제시된 속성 값만을 추출하여 새로운 릴레이션을 만드는 연산
* 연산자의 기호는 그리스 문자 파이를 사용
* 결과에 중복이 발생할 시 중복제거

##### Join
: 공통 속성을 중심으로 두 개의 릴레이션을 하나로 합쳐서 새로운 릴레이션을 만드는 연산
* 연산자의 기호는 ⋈을 사용
