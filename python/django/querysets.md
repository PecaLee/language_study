# Django Query sets

### 쿼리란?

- 데이터베이스에 정보를 요청하는 것
- 웹 서버에 특정한 정보를 보여달라는 웹 클라이언트 요청

## python dir / vars

### dir

- It attempt to return a list of valid attributes for that object when passed an argument
- 내장함수, 객체의 어트리뷰트(함수, 변수 등의 이름들)을 리턴한다. 그리고 객체의 클래스 속성 및 슈퍼클래스의 속성까지 한꺼번에 표시함.

### vars

- It returns a dictionary corresponding to the object's symbol table if a module, class or class instance object as argument (or anything else that has a **dict** attribute) is passed.
- 내장함수, object 없이 쓸 경우 지역 변수의 사전을 넘김. object 가 들어가면 그 객체(모듈, 클래스, 클래스 인스터스)의 사전을 넘김.

## [Django QuerySet API](https://docs.djangoproject.com/en/3.1/ref/models/querysets/)

```
$ python manage.py shell
```

```
>>> from <app>.models import <model>
>>> dir(<model>)
>>> vars(<model>)
```

- foreign key 에서 가져올때는
  ```
  .<arg>_set
  ```
