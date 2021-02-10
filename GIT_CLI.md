 GIT CLI
================

 1.GIT 문법
-----------
```
1. git mkdir : 디렉토리를 만든다.
2. nano [파일명] or vim [파일명] : 파일을 만든다.
3. git rm [파일명] : 파일을 삭제한다.
4. git -rf rm [디렉토리명] : 디렉토리를 삭제한다.
5. git mv [파일명][바꾸고자하는 파일명] : 파일 이름을 변경한다.
6. git mv [파일명][이동할 위치의 경로] : 파일을 이동한다.
7. git log : 로그를 확인한다.
* git log --all --graph --oneline : 로그를 그래프와 oneline으로 확인한다. 
8. git status : 파일 저장 단계의 상태를 확인한다.
9. git add . : 지금 디텍토리의 하위 파일들을 add한다.
10. git commit -am '[설명]': 이미 생성된 파일에 한해서 add와 commit이 동시에 가능하다.
11. git commit --amend : 최근 commit 메세지를 수정한다.
12. 커밋메시지 수정하는 방법 
    1) git rebase -i [commit id]
    2) 수정을 원하는 커밋을 pick에서 edit로 변경한다.
    3) git commit --amend
    4) commit 메시지를 수정한다.
    5) git rebase --continue
```
* * *
 2.GIT CLI - 버전관리
---------------------

### 2.1. 파일 저장 단계
```
1. Woring tree - 수정한 파일들
2. Staging Area - 버전을 만들려고 하는 파일들
3. Repository - 만들어진 버전
```

### 2.2. 파일 저장하는 방법
```
1. 파일을 만든다. ex> nano git.txt , vim git.txt 

- Woring tree 단계

2. git add [파일명] ex> git add git.txt 

- Staging Area 단계

3. git commit -m '[설명]' ex> git commit -m 'git.txt 저장'

- Repository 단계
```

### 2.3. checkout, reset, revert 

#### 2.3.1. checkcout
```
특정버전으로 working tree를 변경시키는 방법
사용법: git checkout [git log의commit id]
```

#### 2.3.2. reset
```
원하는 버전으로 돌아가고 싶을 때 사용하는 방법
사용법: git reset [git log의 commit id]
```

#### 2.3.3. revert
```
이전버전을 삭제하지 않고 특정버전으로 되돌릴 때 사용하는 방법
사용법: git revert [git log의 coomit id]
**git revert를 할 때 특정 버전으로 돌아가고 싶다고 revert을 하면 comflict가 일어나기 때문에 이전 버전부터 역순으로 revert를 해주어야 한다.**
```
* * *

 3.GIT CLI - Branch & Conflict
------------------------------
### 3.1. Branch
```
한 뿌리에서 나왔지만 서로 다른 역사를 써가는 버전들을 말한다.
```

### 3.2. merge
```
branch와 branch를 합치는 것
사용법: git merge[병합하고자 하는 branch명]

ex> maseter branch에 o2branch를 병합 할 때:
1. git checkout master - master branch로 이동
2. git merge o2 - master branch에 o2 branch를 병합
```

### 3.3. Conflict
```
두 branch가 수정됬을 때 merge를 하면 conflict가 일어난다.
이 때는 파일에 들어가 conflict가 일어난 부분을 수정해주면 해결된다.
```
* * *
 4.GIT CLI - Backup
-------------------

### 4.1.원격저장소와 연결
```
사용법: git remote add origin [원격저장소의 https 주소]
* origin은 원격저장소의 별명이다. 원하는 별명을 써도 되지만 관습적으로 origin을 사용한다.

git remote : 원격 저장소를 볼 수 있다.

git remote -v : 원격 저장소의 주소를  볼 수 있다.
```
### 4.2.push
```
push : 로컬 저장소에서 원격 저장소로 파일을 백업한다.

사용법: git push
```

### 4.3.clone
```
clone: 깃허브에서 로컬저장소로 파일을 복원하는것

git bash에서 기존저장소의 파일을 새로운 저장소에 복원한다.

사용법: git clone[기존저장소의 주소][원하는 파일명]
* 원하는 파일 명을 생략시, 기존저장소의 파일명으로 생성된다.
```

### 4.4.pull
```
pull : 원격저장소의 버전을 지역저장소로 가져오는 방법
다른 말로는 작업한 내용을 다른 컴퓨터로 동기화 시키는 작업

사용법 : git pull
```
* * *

 5.GIT CLI - 협업
-----------------

```
협업을 할 때, 
git bash를 통해 작업을 시작하기 전에 pull을 해주고 
작업이 끝나면 push를 해준다.
```

### 5.1. git pull vs fetch 그리고 원격 브랜치
```
fetch - 현재 로컬저장소의 내용을 원격저장소의 내용과 merge해서 가져오는 것이 아니라 원격저장소의 내용만을 가져오는 것

git pull = git fetch + git merge FETCH_HEAD
```

