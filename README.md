## 자주 쓰는 깃 명령어 모음

## reset

```bash
$ git reset --soft
```

index(staging area)와 working directory의 작업을 두고 HEAD 포인터만 옮긴다.

```bash
$ git reset --mixed
```

reset의 기본값이며 index까지 리셋한다.

```bash
$ git reset --hard
```

working directory까지 리셋하는 것으로 **실제 데이터가 바뀌는 작업이니 주의해야 한다.**

## merge

* 3-way merge (recursive strategy)
  * 두 브랜치의 각 마지막 커밋과 공통 조상커밋을 기준으로 병합되는 것으로 `rebase` 를 사용하지 않고 합치는 방식이다.
* Fast-forward merge
  * 한 브랜치를 `rebase` 한다음 이전 커밋에 있는 HEAD를 빨리감기 하듯이 merge하는 방식이다.

merge 명령어는 똑같지만 방식에 있어 차이가 있다. 이해안되면 [여기](https://git-scm.com/book/ko/v2/Git-브랜치-브랜치와-Merge-의-기초#_basic_merging) 참고하자.

## branch

```bash
$ git branch
```

브랜치 목록 확인

```bash
$ git branch -m "새로운이름"
```

브랜치 이름 변경, 대문자는 강제

```bash
$ git branch -d "기존 브랜치 이름"
```

브랜치 삭제, 대문자는 강제

## rebase

브랜치의 base를 바꾸는 명령어로 보통 원격저장소의 브랜치를 rebase 할 경우에 force push가 수반된다.