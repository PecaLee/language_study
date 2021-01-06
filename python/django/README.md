# Django

## web frame work

Django is a massive fram work.

### pipenv

- pipenv 환경 작성

  ```
  > pipenv --three
  ```

  - python 3.x 버젼의 pipenv 환경 작성

  ```
  > pipenv shell
  ```

  - 환경 실행

  ```
  pipenv install Django==<버전정보>
  ```

  - 장고 설치
  - VScode에서 인터프리터 선택

  ```
  > pipenv install <라이브러리 명> --dev --pre
  ```

  - 개발자 라이브러리 설치(밑의 린터와 포맷터 등)

### Linter

- 린터
  - flake8

### formatter

- 포맷터
  - black

### Django

#### creating a project

```
> django-admin startproject config
```

- config 폴더 정리(폴더 안 파일들을 밖으로 빼줌)

#### setting.py

- 장고의 전체적 세팅을 관리하는 파일
- 세팅 파일에서 모르면 주석달려있는 주소에서 도큐먼테이션 확인하는 습관을 만들자.

#### django documentation

- 장고 도큐먼테이션 사이트에서 언제라도 검색해서 찾아 볼 수 있다.

#### 서버 실행

```
> python manage.py runserver
```

#### 마이그레이션

```
> python manage.py makemigrations
> python manage.py migrate
```

- 데이터 베이스를 만들고 장고와 데이터베이스를 연결

#### 슈퍼유저

```
> python manage.py createsuperuser
```

#### Django config

- 모든 애플리케이션을 통합해서 웹 사이트를 구성

#### Django Applications

- 장고 프로젝트는 여러 애플리케이션을 포함하고 있다.
- function의 집합
- CRUD를 기준으로 생각하기
- 어플리케이션은 한문장으로 설명할 수 있어야 한다
- 1개의 어플리케이션은 가능하한 작게
- divide and conquer

```
> django-admin startapp <app name>
```

- 어플리케이션 작성
- 어플리케이션 이름은 복수형으로
- 장고 기본 어플리케이션과 겹치는 이름은 다른 이름으로 작성

#### 장고에 어플리케이션을 등록

- config에서 등록
-
