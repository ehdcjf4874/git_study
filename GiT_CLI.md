 GIT CLI
================

 1.GIT CLI - 버전관리
---------------------

### 1.1. 파일 저장 단계
```
1. Woring tree - 수정한 파일들
2. Staging Area - 버전을 만들려고 하는 파일들
3. Repository - 만들어진 버전

```

### 1.2. 파일 저장하는 방법
```
1. 파일을 만든다. ex> nano git.txt , vim git.txt 

- Woring tree 단계

2. git add [파일명] ex> git add git.txt 

- Staging Area 단계

3. git commit -m '[설명]' ex> git commit -m 'git.txt 저장'

- Repository 단계
```

### 1.3. checkout, reset, revert 

#### 1.3.1. checkcout
```
특정버전으로 working tree를 변경시키는 방법
사용법: git checkout [git log의commit id]
```

#### 1.3.2. reset
```
원하는 버전으로 돌아가고 싶을 때 사용하는 방법
사용법: git reset [git log의 commit id]
```

#### 1.3.3. revert
```
이전버전을 삭제하지 않고 특정버전으로 되돌릴 때 사용하는 방법
사용법: git revert [git log의 coomit id]
**git revert를 할 때 특정 버전으로 돌아가고 싶다고 revert을 하면 comflict가 일어나기 때문에 이전 버전부터 역순으로 revert를 해주어야 한다.

