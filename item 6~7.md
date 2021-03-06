# 2장 타입스크립트의 타입 시스템

## item 6 편집기를 사용하여 타입 시스템 탐색

타입스크립트를 설치하면 다음 두 가지를 실행 할 수 있다.

- 타입스크립트 컴파일러(tsc)
- 단독으로 실행할 수 있는 타입스크립트 서버(tsserver)

타입스크립트 서버 -> 언어 서비스 제공 : 코드 자동완성, 명세(사양, specification) 검사, 검색, 리팩터링

- 조건문의 분기에서 값의 타입이 어떻게 변하는지 살펴보는 것은 타입 시스템을 연마하는 매우 좋은 방법이다.
- 객체에서는 개별 속성을 살펴봄으로써 타입스크립트가 어떻게 각자의 속성을 추론하는지 살펴 볼 수 있다.

p. 35 연산자체인? 제너릭 타입? 추론 정보?

- p.37 lib.d.ts : Typescript를 설치하면 해당 특수한 선언파일이 함께 따라온다. 이 파일은 javascript 런타임 및 DOM에 존재하는 다양한 일반적인 JavaScript constructs에 대한 ambient 선언을 담고 있다.

* lib.d.ts는 typescript 프로젝트의 컴파ㅏ일 context에서 자동으로 추가된다.
* lib.d.ts는 타입체크가 보장된 JavaScript 코드를 손쉽게 작성할 수 있도록 돕는 역할을 한다.

타입 선언은 타입스크립트가 무엇을 하는지 어떻게 라이브러리가 모델링되었는지, 어떻게 오류를 찾아낼지 살펴볼 수 있는 훌륭한 수단이라는 것을 알 수 있다.

## item 7 타입이 값들의 집합이라고 생각하기

가장 작은 집합은 아무 값도 포함하지 않는 공집합, 타입스크립트에서는 never타입  
 그 다음 작은 집합은 한 가지 값만 포함하는 타입, 타입스크립트에서 unit타입(literal)타입.  
 두 개 혹은 세 개로 묶으려면 union 타입을 사용.

p. 40 잉여속성체크(excess property checking) : 특정 상황에서 추가 속성을 허용하지 않는...

    잉여속성체크는 타입에 선언된 속성 외의 속성이 있는지 체크
    객체 리터럴에서만 잉여 속성 체크가 동작, 그래서 엄격한 객체 리터럴 체크라고 불린다.
    일반적인 구조적 할당 기능성 체크와는 역할이다르다.

![표 2-1](./img/%ED%91%9C%202-1.JPG)

요약.  
타입을 값의 집합으로 생각하면 이해하기 편함.  
타입스크립트 타입은 엄격한 상속관계가 아니라 겹쳐지는 집합(벤 다이어그램)으로 표현  
한 객체의 추가적인 속성이 타입 선언에 언급되지 않더라도 그 타입에 속할 수 있다.  
타입 연산은 집합의 범위에 적용된다.
