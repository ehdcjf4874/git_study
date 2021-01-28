 GIT CLI
================

 1.GIT 문법
-----------
```
1. git mkdir : 디렉토리를 만든다.
2. nano [파일명] or vim [파읾영] : 파일을 만든다.
3. git rm [파일명] : 파일을 삭제한다.
4. git -rf rm [디렉토리명] : 디렉토리를 삭제한다.
5. git mv [파일명][바꾸고자하는 파일명] : 파일 이름을 변경한다.
6. git mv [파일명][이동할 위치의 경로] : 파일을 이동한다.
7. git log : 로그를 확인한다.
* git log --all --graph --oneline : 로그를 그래프와 oneline으로 확인한다. 
8. git status : 파일 저장 단계의 상태를 확인한다.
9. git add . : 지금 디텍토리의 하위 파일들을 add한다.
10. git commit -am '[설명]': 이미 생성된 파일에 한해서 add와 commit이 동시에 가능하다.
11. git commit --amend : commit 메세지를 수정한다.
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


