# 2020/10/20

- [x]  git

---

요즘 git 공부를 하고 있는 중

```bash
git add .
```

여태껏 git add [1.md](http://1.md) [2.md](http://2.md) 이런 식으로 전부 나열했는데, . 하나 찍으면 전체 파일과 폴더를 모두 등록할 수 있다는 말에 놀람

 

한 번이라도 커밋한 파일을 삭제하려면

```bash
git reset HEAD 파일명
```

를 써줘야함

파일 이름 변경

```bash
git mv 현파일 변경파일
```

git에도 HEAD라는 포인터 개념이 있음

이는 최종적인 커밋 작업의 위치를 가리킴

---

VI 에디터 사용법 간단 정리

- 새로운 내용 입력 : ESC → i
- 저장 및 종료 : ESC → :wq
- 그냥 종료 : :q

---

커밋 메시지 작성 요령

1. 제목
2. 
3. 상세 내용

---

```bash
git commit -a
```

git add와 commit을 동시에 하는 효과

```bash
git log
```

커밋 목록 확인

```bash
git checkout --수정파일이름
```

마지막 내용으로 되돌리기 

→ ?? 예전에 fog computing 환경 구성할때 매번 git checkout을 해줘서 최신 버전이 있는지 확인하는 과정이구나 생각했는데 전혀 아니었음..

# 2020/10/21

- [x]  git

---

```bash
git commit --allow-empty-message
```

와.. 여태껏 TIL 업데이트 커밋 메시지를 대체 뭐로 해야하는지 고민했는데..

빈 커밋 작성이 가능하단걸 처음 알게 됨

```bash
git commit --amend
```

커밋 메시지 수정

```bash
get diff
```

워킹 디렉터리 내용과 스테이지 내용의 차이점 출력

```bash
git remote add 저장소 폴더경로
```

로컬 저장소를 서버로 이용

```bash
git pull
```

갱신된 원격 저장소의 커밋 정보를 내려받음

pull → 작업 → commit → pull → push

처럼 자주 pull과 push를 해줘야함

# 2020/10/22

```bash
git checkout branch_name
```

저번에 checkout을 잘못 사용했다고 했는데

이쪽 의미로 사용했었나보다

실제로 git checkout master 이런 명령어를 친 느낌도 있구...

HEAD를 기준으로 상대적 커밋 위치도 지정 가능

이전 5개면 HEAD^5나 HEAD~5로 가능

스태시 = 임시 저장

```bash
git clean
```

추적되지 않는 파일들을 찾아 삭제

```bash
git merge branch_name
```

브렌치 병합

# 2020/10/24

---

### 3-way 병합

3-way가 된 상태에서 git checkout master로 이동

```bash
git merge 다른브렌치이름
```

병합 커밋 메시지 생성

### git flow

= 브렌치 관리 기법

master,feature,develop,release,hotfix가 있음

불필요한 브렌치는 삭제한다

```bash
git branch -d 브렌치명
```

# 2020/10/25

reset 관련해서 배웠음

# ~ 2020/10/31

조금씩 git 공부 병행하면서 백준 문제 풀었음

주로 비트마스킹 계열..