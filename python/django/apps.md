# Django Applications

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

## 장고에 어플리케이션을 등록

- config에서 등록
- config/setting.py
  ```
  INSTALLED_APPS = [
    "<appname.apps.appnameConfig>"
  ]
  ```

## 장고 어플리케이션 폴더 안의 디폴트

- models.py : 데이터베이스의 내용
- apps.py
- admin.py : admin패널에서의 뷰
- views.py

## AUTH_USER_MODEL

- 유저모델을 변경
- config/setting.py
  ```
  AUTH_USER_MODEL = "<myapp.MyUser>"
  ```

## User

- AbstractUser

## models.py

### 앱의 데이터베이스의 형태를 결정

```
from django.contrib.auth.models import AbstractUser #AbstractUser 임포트
from django.db import models

# Create your models here.
class User(AbstractUser):   #AbstractUser를 상속해서 데이터베이스 생성

  """ Custom User Model """

  GENDER_MALE = "male"          #선택 데이터 필드 생성
  GENDER_FEMALE = "female"
  GENDER_OTHER = "other"

  GENDER_CHOICE = (
      (GENDER_MALE, "Male"),
      (GENDER_FEMALE, "Female"),
      (GENDER_OTHER, "Other"),
  )

  avatar = models.ImageField(null=True, blank=True)   #이미지 필드 타입
  gender = models.CharField(                          #캐릭터 필드 타입
      choices=GENDER_CHOICE, max_length=10, null=True, blank=True
  )
  bio = models.TextField(default="", blank=True)      #텍스트 필트 타입
```

- null = True : 데이터베이스에서 빈칸 허용
- default = "" : 데이터베이스 에서의 기본값
- blank = True : 필수선택이 아니게

## admin.py

### 애드민 패널에서의 형태를 결정

```
from django.contrib import admin
from django.contrib.auth.admin import UserAdmin     #장고 기본 유저 어드민 임포트
from . import models                                #데이터베이스 형태 임포트(모델)

# Register your models here.
@admin.register(models.User)         #밑의 클래스를 데이터베이스의 모델을 사용해 어드민으로서 등록
class CustomUserAdmin(UserAdmin):    #장고 기본 유저어드민을 상속해서 어드민 뷰를 작성

    """ Custom User Admin """

    fieldsets = UserAdmin.fieldsets + (       # 필드셋
        (
            "Custom profile",
            {
                "fields": (
                    "avatar",
                    "gender",
                    "bio",
                    "birthdate",
                    "language",
                    "currency",
                    "superhost",
                )
            },
        ),
    )
```
