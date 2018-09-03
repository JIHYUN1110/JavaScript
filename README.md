# Promises

Promise는 비동기 조작의 최종 완료나 실패를 표현해주는 객체이다. 비동기 동작이 종료된 이후의 결과값이나 실패 이유를 처리하기 위한 처리기(handler)를 연결할 수 있도록 합니다. 프로미스는 비동기 메서드가 동기 메서드처럼 값을 반환한다. 
최종값 대신, 비동기 메서드는 미래 어느 시점에 값을 갖는 프로미스를 반환한다.

다음 중 하나의 상태를 가진다.
대기(pending): 이행되거나 거부되지 않은 초기 상태.
이행(fulfilled): 연산이 성공적으로 완료됨.
거부(rejected): 연산이 실패함.

Promise 오브젝트는 new 키워드와 생성자를 통해 만든다. 이 생성자는 인수로 executor 함수를 사용한다. 
이 함수는 매개 변수로 두 가지 함수를 가져야 하고 비동기 작업이 성공적으로 완료되고 결과를 값으로 반환하면 첫 번째 함수가 호출된다. 두 번째는 작업이 실패 할 때 호출되며 보통 오류 객체를 반환한다.

# Let / Const

let은 변수가 선언된 블록, 구문 또는 표현식 내에서만 유효한 변수를 선언하며 var이 블록 범위를 무시하고 전역 변수나 함수 지역 변수로 선언되는 것과 다른 점이다.
let 으로 선언된 변수는 변수가 선언된 블록 내에서만 유효하고 당연하지만 하위 블록에서도 유효하다.

const 선언은 값에 읽기 전용 참조를 생성한다. 담긴 값이 불변임을 뜻하는 것이 아니라 단지 그 변수 식별자는 재할당될 수 없다는 것이다.

# Arrow Functions

화살표 함수는 무명 함수를 생성하는 방법 중 하나로 기본 형태는 (파라메터1, 파라메터2,...) => { 함수내용 }이다.
- 함수 내용이 한줄인 경우 함수내용을 감싸는 {}를 사용하지 않아도 된다.
- {}가 없는 경우 해당 함수의 실행결과를 자동으로 보낸다.
- 함수 내용이 한줄 이상인 경우 return을 사용해서 결과를 리턴한다. 
- 파라메터가 한개인 경우 감싸는 ()를 생략할 수 있다.
(참조 https://blog.naver.com/azure0777/221111424759)

# Array Methods

- map():  배열 내의 모든 원소에 대하여 제공된 함수를 호출하고 결과를 모아 새로운 배열을 리턴하는 메소드
- reduce(): 배열의 원소마다 누적 계산값과 함께 함수를 적용해 하나의 값으로 리턴하는 메소드 (왼쪽부터)
- filter(): 배열의 원소 중 제공된 함수를 통과하는 원소를 반환하는 메소드
- slice(): 배열의 주어진 start부터 end까지 배열 객체로 변환하는 메소드
- splice(): 배열의 원소를 삭제하거나 새 원소를 추가하는 메소드

# Spread Operator

Spread operator는 2개 이상의 인수(함수 호출 용)나 2개 이상의 요소(배열 리터럴 용) 또는 2개 이상의 변수(비구조화 할당 용)가 예상되는 곳에 확장될 수 있도록 한다.
- 함수 호출 용: myFunction(...iterableObj);
- 배열 리터럴 용: [...iterableObj, 4, 5, 6]
- 비구조화destructuring 용: [a, b, ...iterableObj] = [1, 2, 3, 4, 5];

# Export / Import

Export 문은 지정된 파일(또는 모듈)에서 함수 또는 오브젝트, 원시 타입들을 export 하는데 사용된다. Named exports와 Default exports 두가지 방법이 있다.
Named exports는 여러값을 export 하는데 유용하고 Default exports 로 객체, 함수 클래스 등이 될 수 있으며 가장 간단하게 export 할 수 있다.
딱 한개만 default export를 할 수 있기 때문에, 가장 메인이라고 할 수 있는 것을 default export 하는 것이 좋다.

Import 문은 외부 모듈이나 다른 스크립트 등으로부터 export 된 기능을 가져오는데 사용된다.
- name: 가져온 값을 받을 객체 이름
- member, memberN: export 된 모듈에서 멤버의 이름
- defaultMember: export 된 모듈의 default 이름
- alias, aliasN: export된 멤버의 이름을 지정한 이름
- module-name: 가져올 모듈 이름 (파일명)

(참조: http://beomy.tistory.com/22)


(참조: https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference)


