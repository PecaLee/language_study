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