# CS_study_13회

## 1. [네트워크] 로드 밸런싱

> 로드 밸런싱에 대해 간단히 설명해주세요.

## 2. [웹] UI/UX

> UI/UX의 개념을 간단히 설명하고, 진행했던 프로젝트에서 UI/UX를 향상하기 위해 노력했던 경험을 말씀해주세요.

## 3. [언어] 호이스팅

> 자바스크립트의 호이스팅(Hoisting)이란 무엇인가요?

호이스팅 현상이란 변수 선언 이전에 참조되는 현상을 의미합니다. 자바스크립트 변수 타입 중 let과 const는 변수 선언 단계와 초기화 단계가 나누어서 이루어지기 때문에 참조는 되지만 Reference error가 발생합니다. var는 변수 선언 단계와 초기화 단계가 동시에 이뤄지고, 초기화 값이 없으면 자동으로 'undefined'로 할당해버리기 때문에 오류가 발생하지 않습니다.

```javascript
console.log(hello) // undefined
var hello = 'world!'
console.log(hello) // 'world!'
```

해당 예제에서는 첫번째 줄에서 호이스팅이 발생하여 선언하지 않았지만 참조되어 undefined를 출력하게 됩니다. 따라서 다음 코드와 동일하게 동작하게 됩니다.

```javascript
var hello
console.log(hello)
var hello = 'world!'
console.log(hello)
```



## 4. [알고리즘] Stable sorting

> Sorting Algorithm에서 stable 하다는 것은 무엇을 의미하나요?