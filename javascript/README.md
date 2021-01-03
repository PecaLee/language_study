# javascript
### 노트 및 개념정리   
## 프로그래밍이란?
- 컴퓨터한테 명령을 내리는 것
## 자바스크립트란?
- 컴퓨터에 명령을 내리는 언어의 하나  
### 주석
    ```
    //주석내용
    ```
### 자료형
- NaN, number, string, boolean, null, undefined
### 연산자
- +, -, *, **, /, %, >, <, >=, <=
- +=, -=
### 비교 연산자
- ==, !=
- ===, !==
- 엄격한 비교   
### 변수
- var
- const
- let
### 조건문
- if
    ```
    if () {

    } else if () {

    } else {

    }
    ```
- [switch](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/switch)
    ```
    switch (<condition>) {
        case <condition> :
            <code>
            break;
        case <condition> :
        case <condition> :
        case <condition> :
            <code>
            break;
        default:
            <code>
    }
    ```
### [반복문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration)
- while
    ```
    while (<condition>) {

    }
    ```
    - condition 이 true 일 때 반복
- for 
    ```
    for (<start>; <조건>; <end>){
        <code>
    }
    ```
    ex)
    ```
    for (let a = 0; a < 5; a = a + 3) {
        console.log("text");
    }
    ```
### 함수
    ```
    function <function name> () {

    }
    ```   
### 객체
- 값을 그룹화 하는 용도로 쓸 수 있다.
    ```
    const 페카 = {
        이름 : "페카",
        키 : 173,
        몸무게 : 65,
        먹다 : function eat(){
            console.log("eat!");
        },
    }
    const 슈 = {
        이름 : "슈",
        키 : 165,
        몸무게 : 43,
    }
    ```
    - 속성(프로퍼티) : 값
    - 속성(메서드) : 함수
    - 메서드는 익명함수로 사용해도 된다. 메서드명이 함수명의 역할을 함.
    ```
    페카["이름"]
    페카.이름
    페카["먹다"]
    페카.먹다
    페카.먹다()
    ```
    - 대괄호를 꼭 써야하는 경우
        - 변수를 사용하여야 하는 경우
### 배열
- 값 그룹화는 하지만 속성이름을 주고싶지 않을때
- array [ ]
    ```
    const array = [
        "사과", 
        "오렌지", 
        "포도", 
        "딸기",
    ]
    ```
    ```
    array[0]
    > "사과"
    ```
### window 객체
- window.document
- window.<...>
### document 객체와 DOM
- document object model
- html을 js로 통역해 주는 역할