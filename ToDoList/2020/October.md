# 2020/10/05
- [x] 백준 그리디 잃어버린 괄호
---------------------------------------
문제 자체의 아이디어는 어렵지 않았으나, 수식을 어떻게 자를지에 시간을 더 소모함<br/>
----------------------------------------
- [x] ebs 인공지능 -- 이미지 처리까지 봄

# 2020/10/06
- [x] 백준 수학 문제
- [x] ebs 인공지능 -- 소리처리 중간
---------------------------------------------------
<br/>
삼각함수 설명부터 막혀버렸다<br/>
관련 강의나 글을 읽어봐야겠다<br/>

# 2020/10/07
- [x] 백준 문제
- [x] ebs 인공지능 -- 소리처리 중간
---------------------------------------------------
어제까지 이론만 본 내용에 실습을 추가함<br/>
그냥 따라 타이핑만 하면 의미가 없을듯하여 버튼 액션 추가<br/>


# 2020/10/08

- [x]  백준 문제 풀이(부분수열의 합, 2진수 8진수,중복 빼고 정렬하기,N과 M(1),차이를 최대

---

### 부분수열의 합

부분수열의 합은 기본 접근 방식으로 재귀가 있다.

처음에는 1,0으로 이루어진 배열로 풀까 생각했었는데 비트 마스킹이라는 방식이 더 어울린다는 조언을 받음.

두 방식으로 다 해봤으나.. 비트 마스킹을 내가 계속 기억하고 써먹을 수 있을까..?

### 2진수 8진수

정석 풀이가 아닌 파이썬만의 장점으로 해결

그리고 이것을 몇시간 뒤에 후회하게 되는데...

### 중복 빼고 정렬하기

set쓰고 정렬하면 간단하게 해결 가능

### N과 M(1), 차이를 최대

앞을 풀면 응용해서 뒤를 풀 수 있는 문제

itertools를 잘 사용하면 쉽고 간편하게 풀 수 있음

---

- [x]  프로그래머스 월간 대회

---

여기의 1번 문제가 3진수와 10진수 변환 문제였다

그리고 3진수 변환은 앞의 2진수마냥 꼼수로 할 수 없었음...

미리...잘...짜놨다면..... 그냥... 숫자만 바꿔서 빨리 풀 수 있었는데.....

쒸익쒸익.......

# 2020/10/09

- [x]  mp3 to wav

---

python 에서 mp3 파일을 wav 로 바꾸는 예제를 찾아보면 전부 ffmpeg를 사용한다

그런데 그게 원래 제공하던 분이 페이지를 닫으면서 다른 사람들의 버전만 남아있다

같은 사용방법인지 비교해보려고 해도 기존을 모르니 비교 불가능

따라서 최대한 ffmpeg original 설치 파일을 찾아다녔고, 결국 구했다.

path 설정하면 끝

만약 cmd창에서는 명령어가 잘 먹히는데 파이썬 IDE에서는 인식 못하는 경우

컴퓨터 재부팅 필요

mp3를 wav 변환한 파일을 저번 소리 파형 그리고 재생하는 예제에 적용

마우스를 그대로 두면 소리가 잘 나오는데, 막 움직이면 버버버벅 거림(4분짜리 노래라서 그런가..)

어쨋든.. 작은 목표는 달성했으니, 다음 진도 나가야지


# 2020/10/10

- [x]  수학과 함께하는 AI기초 삼각함수

---

저번에 삼각함수에서 막혀서 관뒀었는데, ebs 강의를 수강하고 해결했다

현재는 이해중인데, 미래에도 그러기를..

삼각함수, 확률 파트 수강

- [x]  Atcoder

---

A,C번 풀었음

B번의 경우에는 완전 문제를 잘못 해석해서 못풀었는데..

다시 생각해도 어이없다...

# 2020/10/12

- [x]  백준 소인수분해

---

코드포스나 앳코더 앞문제들은 간단한 수식으로 풀리는 경우가 더러 있다.

그런데.. 나는 수학을 못하니까.. 수학 기본 문제들을 조금씩 풀 예정

분명 이런 문제는 n의 제곱근까지만 반복문을 돌려서 풀어도 된다고 알고 있는데 틀렸다고 함

또 어디서 실수한거냐...

- [x]  수학 AI

---

임의의 시그널 생성 + 소리 합성

예전에 TTS 만들다가 그만 뒀었는데, 소리 합성 더 배워봐야지

# 2020/10/13

- [x]  백준 제로, 팰린드롬수,랜선자르기,카드2

---

랜선자르기는 이분 탐색, 카드2는 덱으로 풀었다.

원래 파이썬에서 리스트 만으로 큐처럼 사용할 수 있어서

그것을 이용해서 풀었는데 시간 초과가 떴다.

다른 사람들 보니까 collection의 덱으로 푼다고 그래서 나도 이용

# 2020/10/14

- [x]  백준 9문제

---

음.. 여태껏 a = [1,2,3,4]가 있고 출력 값으로 1 2 3 4를 원한다면 for문을 돌려서 탐색했다.

그런데 print(*a)라고 하면 바로 저 형태로 나온다는걸 알게 되었고 매우 충격받음

# 2020/10/15 ~ 2020/10/18

- [x]  백준 문제 풀이
- [x]  Git 조금씩 공부
- [x]  Velog 정렬 포스팅

---

GIT을 그냥 TIL 용도로만 쓰고 있는데 더 다양하게 쓰고 싶어서 공부중

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
