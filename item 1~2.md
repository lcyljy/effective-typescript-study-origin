22.05.02 월 pm 10:00 ~ 12:00

# 아이템 1 타입스크립트와 자바스크립트의 관계 이해하기

1.  타입스크립트는 문법적으로 자바스크립트의 상위 집합
2.  타입스크립트는 자바스크립트 런타임 동작을 모델링한다.(타입 체커를 통과하면서도 런타임 오류를 발생시킬 수 있으니 주의!)
3.  문법의 엄격함은 온전히 취향의 차이이며 우열을 가릴 수 없는 문제다.
4.  타입스크립트가 이해하는 값의 타입과 실제 값의 차이가 있다.

# 아이템 2 타입스크립트 설정 이해하기

1. 타입스크립트 설정은 커맨드 라인을 이용하기보다는 `tsconfig.json`을 사용하는 것이 좋다.
2. 자바스크립트 프로젝트를 타입스크립트로 전환하는게 아니라면 `noImpllicitAny`를 설정하는 것이 좋다.
3. 런타임 오류를 방지하기 위해 `strictNullChecks`를 설정하는 것이 좋다.
4. 타입스크립트에서 엄격한 체크를 하고 싶다면 `strict`설정을 고려해야 한다.

## 정리

1. 타입스크립트가 자바스크립트로부터 파생되어 나온거로 알고있었어서 당연히 타입스크립트가 자바스크립트의 부분집합일줄 알았는데 반대여서 놀라웠다...
2. `tsconfig.json`에 대해서 처음 알았다. << 해당 파일에 타입스크립트 설정을 할 수 있다.
