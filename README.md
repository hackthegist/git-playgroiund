# Git Branch

## 용도

1. 코드 관리
2. 원격 저장소
3. 협업 도구
4. 이력서 대용

## 기초 커맨드 정리

- git init
- git add
- git commit
- git log : 16진수 6자 만으로도 충돌되지 않는다 아직! (리눅스 75만개 커밋 마저도), 형 branch에서 끝까지 찾아가는 과정!

## 원격저장소

- git remote : 저장소 리스트
- git remote -v : --verbose, 이름과 주소
- git remote add [저징소 이름] [저장소 주소]


> commit 메시지 형식 
>
> 동사 + 목적어, 현재형으로 
>
>ex) `git commit -m "resolve merge conflict"`

### 시간대 이동

- HEAD가 가리키는 commit이 변경한다  
  - git checkout [commit]
  - git checkout master

## branch

**branch는 일회용품**

- git branch
- git branch [이름]

- git chekout [branch name]
- git chekout -b [branch name] : 생성과 이동 (이번 버전)

- git switch [branch name] (>= v2.23) : git checkout으로 하던 일에 새 명령어를 부여핰
- git switch -c [branch name] (>= v2.23) : 생성과 이동 (최신)

- git branch -d [branch name] : Branch 삭제

## Merge

- git merge [branch name] : **현재 branch**에서 특정 branch를 병합, 
  - fast-forward merge : 그냥 선형에서 앞으로 가는 느낌

### Merge secnarios

1. fast-forward merge
2. auto merge (without conflict)
3. merge read conflict

## Conflict 해결 방법

### Conflict 발생 조건

1. 동일 파일 건드리기 
   - '특히 동일 라인의 내용이 다를 경우


git diff 
