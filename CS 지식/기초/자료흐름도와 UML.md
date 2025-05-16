#### **자료 흐름도(DFD)**

 : 요구사항 분석에서 자료의 흐름, 변환 과정,기능을 도형 중심으로 기술하는 방법

- 자료 흐름 그래프, 버블 차트라고도 함

- **네가지 기본 기호** : 프로세스(Process) 자료 흐름(Flow), 자료 저장소(Data Store), 단말(Terminator)

**- 프로세스(Process)**

   ㄴ 자료를 변환시키는 시스템의 한 부분(처리과정)을 나타냄

   ㄴ 처리, 기능, 변환, 버블이라고도 함

   ㄴ 원이나 둥근 사각형으로 표시하며 그 안에 프로세스 이름 기입

![](https://blog.kakaocdn.net/dn/dIZFRp/btscRJL5Jcv/sbJDw2tfpuKacgDQjUB0NK/img.png)

**- 자료 흐름(Data Flow)**

  ㄴ 자료의 이동(흐름)이나 연관 관계를 나타냄

  ㄴ 화살표 위에 자료의 이름을 기입

   **<표기법>**

![](https://blog.kakaocdn.net/dn/3lJjz/btscTjlOROo/myD6yuB7XzbpP5uSx9DKt0/img.png)

**- 자료 저장소(Data Store)**

  ㄴ시스템에서의 자료저장소(파일,데이터베이스)를 나타냄

  ㄴ 도형 안에 자료 저장소 이름을 작성

![](https://blog.kakaocdn.net/dn/dI7CPl/btscQPeZXO1/V59dZSBo36whUbPWaSK4u0/img.png)

![](https://blog.kakaocdn.net/dn/wQ6ls/btscXWjsCYc/kK8T2ikWSLzY3279zK4yOk/img.png)

**- 단말(Terminator)**

  ㄴ 시스템과 교신하는  외부 개체로, 입력 데이터가 만들어지고 출력 데이터를 받음(정보의 생산자와 소비자)

  ㄴ 도형 안에 이름을 작성

![](https://blog.kakaocdn.net/dn/bVvS7I/btscSnvnoXG/3npI0O6Sx60OGkak4rZv21/img.png)

![](https://blog.kakaocdn.net/dn/dsfPR7/btscR0Halxu/1bPkoRE5R4jBx9s3mJWIOK/img.png)

#### **자료 사전(Data Dictionary)**

 : 자료 흐름도에 있는 자료를 더 자세히 정의하고 기록한 것

 - 데이터를 설명하는 데이터 (메타 데이터 Meta Data)

|   |   |
|---|---|
|**기호**|**의미**|
|**=**|자료의 정의 : ~로 구성되어 있다(is composed of)|
|**+**|자료의 연결 : 그리고(and)|
|**(  )**|자료의 생략 : 생략 가능한 자료(Optional)|
|**[ \| ]**|자료의 선택 : 또는(or)|
|**{  }**|자료의 반복 : iteration of  <br>{ }n :n번 이상 반복  <br>{ }n (n 위에 씀) : 최대 n번 반복  <br>{ }nm : m이상 n이하로 반복|
|***  ***|자료의 설명 : 주석(Comment)|

#### **요구사항 분석을 위한 CASE (자동화 도구)**

 : 요구사항을 자동으로 분석, 요구사항 명세서를 기술하도록 개발된 도구

**<종류>**

 **SADT**(Structured Analysis and Degin Techniquw)

  - 시스템의 정의, 소프트웨어 요구사항 분석, 시스템/소프트웨어 설계를 위해 널리 이용된 구조적 분석 및 설계 도구

**SREM**(Software Requirements Engineering Methodology) =RSL/REVS

 - 실시간 처리 소프트웨어 시스템에서 요구사항을 명확히 기술하도록 개발

 - RSL과 REVS를 사용하는 자동화 도구

 - RSL(Requirement Statement Language) : 요소, 속성, 관계, 구조들을 기술하는 요구사항 기술 언어

 - REVS(Requirement Engineering and Validation System) : RSL로 기술된 요구사항들을 자동으로 분 석하여 요구사항 분석 명세서를 출력하는 요구사항 분석기

#### **HIPO** (Hierarchy Input Process Output)

 : 시스템의 분석, 설계, 문서화할 때 사용되는 기법

 - 시스템 실행 과정인 입력, 처리, 출력의 기능을  나타냄

 - 기본 시스템 모델은 입력, 처리, 출력으로 구성

 - 하향식 소프트웨어 개발을 위한 문서화 도구

 - 체계적인 문서 관리 가능

 - 기호, 도표 등을 사용하여 보기 쉽고 이해하기 쉬움

 - 기능과 자료의 의존 관계를 동시에 표현 가능

 - 변경, 유지보수 용이

 **HIPO Chart**

  : 시스템의 기능을 여러 개의 고유 모듈들로 분할하여 이들 간의 인터페이스를 계층 구조로 표현한 것

**<종류>**

 - 가시적 도표(도식 목차)

    : 시스템의 전체적인 기능과 흐름을 보여주는 계층(Tree) 구조도

 - 총체적 도표(총괄도표, 개요도표) 

    : 입력, 처리, 출력에 대한 전반적인 정보를 제공하는 도표 (프로그램을 구성하는 기능을 기술한 것)

- 세부적 도표(상세 도표)

    : 총체적 도표에 표시된 긴ㅇ을 구성하는 기본 요소들을 상세히 기술하는 도표

#### **UML(Unified Modeling Language)**

 : 시스템 분석, 설계, 구현 등 시스템 개발 과정에서 시스템 개발자와 고객 , 개발자 상호간의 의사소통이 원활하게 이루어지도록 표준화한 대표적인 객체 지향 모델링 언어

- 객체 기술에 관한 국제표준화기구(OMG)에서 표준으로 지정

-  Rumbaugh(OMT), Booch, Jacobson 등의 객체지향 방법론의 장점을 통합함

- UML의 구성 요소에는 사물(Things), 관계(Relationships), 다이어그램(Diagram) 등이 있음

- 시스템의 구조를 표현하는 6개의 구조 다이어그램과 시스템의 동작을 표현하는 7개의 행위다이어그램 작성 가능

- 각각의 다이어그램은 사물과 사물 간의 관계를 용도에 맞게 표현

#### **관계(Relationships)**

 : 사물과 사물 사이의 연관성을 표현하는 것

 **- 연관 관계 (Association)**

    : 2개 이상의 사물이 서로 관련되어 있음을 표현

 **- 집합 관계(Aggregation)**

    : 하나의 사물이 다른 사물에 포함되어 있는 관계

 **- 포함 관계(Composition)**

   : 집합 관계의 특수한 형태, 포함하는 사물의 변화가 포함되는 사물에게 영향을 미치는 관계

 **- 일반화 관계(Generalization)**

   : 하나의 사물이 다른 사물에 비해 더 일반적인지 구체적인지를 표현

 **- 의존 관계 (Dependency)**

    : 서로 연관은 있으나 필요에 의해 서로에게 영향을 주는 짧은 시간 동안만 연관을 유지하는 관계

      ( 일반적으로 한 클래스가 다른 클래스를 오퍼레이션의 매개 변수로 사용하는 경우에 나타남 )

 **- 실체화 관계(Realization)**

     : 사물이 할 수 있거나 해야 하는 기능(행위, 인터페이스)으로 서로를 그룹화 할 수 있는 관계