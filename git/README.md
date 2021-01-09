# 깃을 사용하는 방법

## 기본 개념

- repository

  - 깃이 보고있는 폴더

- commit

  - 기록 point in time
  - history
    - title, description
    - 언제 어떻게 바뀌었는지를 기록

- area

  - working area
  - staging area
    - 디폴트값으로 변경점은 전부 추가
  - repository area
    - 커밋 후 수정사항을 스냅샷으로 보관

- branch

  - 가지치기로 나눠서 작업후 변경점을 합칠 수 있다.

- push

- 깃허브
  - fork
    - clone repository on github
  - pull request
    - 원본에 합칠때
  - fork 최신화
    - base repository 가 변경되었을때 베이스 리포지토리에 맞춰 최신화가 가능
  - issues
    - 이슈, 문제, 버그의 기록
    - 이슈번호 pull request로 해결, 피드백

## CLI에서의 git

- git log

  ```
  $ git log
  ```

  - 커밋 이력을 확인
  - 프리뷰 ❎
  - "q" 클로즈

- git push

  ```
  $ git push <repository> <branch>
  ```

  - 푸쉬 레포지토리명 브랜치명

  ```
  $ git push --set-upstream <repository> <branch>
  ```

  - 업스트림 브렌치 설정 후 푸쉬
  - 업스트림이란 원격 저장소와 바로 연결된 로컬 저장소를 말하며 push나 pull 명령등에서 원격 저장소 이름을 생략할 수 있게 한다.

- git add

  ```
  $ git add <file name>
  $ git add .
  ```

  - file name을 스테이징 에리어로

- git commit

  ```
  $ git commit -m "<message>"
  ```

  - 커밋, 메시지를 커밋함

  ```
  $ git commit -help
  ```

  - commit 옵션 확인

  ```
  $ git commit --amend --no-edit
  ```

  - commit 수정 커밋 메시지는 수정 ❎

  ```
  $ git commit --amend -m "<message>"
  ```

  - commit 수정 커밋 메시지도 수정

- git checkout

  - git의 HEAD를 옮김

  ```
  $ git checkout <commit id>
  ```

  - commit id의 시점으로 돌아감

  ```
  $ git checkout master
  ```

  - 현시점으로

- git reset

  - commit 삭제

  ```
  $ git reset --hard HEAD^
  $ git reset --hard HEAD^^
  ```

  - hard reset
    - --hard 삭제
    - HEAD^ HEAD에서 몇단계 전으로 돌아갈지

  ```
  $ git reset HEAD^
  ```

  - mixed reset
    - 삭제하지 않고 변경사항을 unstage로 이동

  ```
  $ git reset --soft HEAD^
  ```

  - soft reset
  - --soft 삭제하지 않고 변경사항을 stage로 이동

  ```
  $ git push origin master --force
  ```

  - 커밋을 삭제해서 상태가 변경되었기 때문에 repository에 강제로 푸쉬

- git remote

  ```
  $ git remote -v
  ```

  - 원격저장소 확인

  ```
  $ git remote add <name> <repository url>
  ```

  - 저장소 추가

  ```
  $ git remote remove <name>
  ```

  - 저장소 제거

- 브랜치 작성

  ```
  $ git checkout <commit id>
  $ git checkout -b <new branch>
  ```

  - 시점이동 후 새 브랜치 작성

  ```
  $ git checkout
  $ git push origin <branch name>
  ```

  - 브랜치명 확인후 브랜치 푸쉬

  ```
  $ git branch -d <branch name>
  ```

  - 브랜치 삭제

- git status

  ```
  $ git status
  ```

  - 깃의 상태표시

- .gitignore

  ```
  .gitignore
      <file name>
      /<foldername>
  ```

  - repository 공유 안하는 목록
  - .gitignore 파일 작성해 그 안에 위와 같이 작성

  ```
  $ git rm <file name> --chached
  $ git rm -f <folder name>/ --chached
  ```

  - .gitignore 작성전 add했을때 git에서 캐쉬된 파일을 제거(staged area에서 제거)

- git clone

  ```
  $ git clone <repository url>
  ```

  - 깃이름으로 폴더생성 후 그 안에 클론한다

  ```
  $ git clone <repository url> <folder name>
  ```

  - folder name의 폴더 생성후 클론

- git fetch

  ```
  $ git fetch <remote>
  ```

  - 깃 리모트 저장소의 업데이트 확인

- git pull

  ```
  $ git pull <remote>
  ```

  - 깃 리모트 저장소의 내용을 가져와 병합

- git config
  ```
  $ git config
  ```
  - git 설정등을 확인
  ```
  $ git config --global user.name "name"
  $ git config --global user.email "email"
  ```
  - 글로벌 유저네임 이메일 확인
