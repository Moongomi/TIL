# 2020/11/01
- [x] October TIL 정리
- [x] 백준 문제 풀이
- [x] atcoder 참여
- [x] 코세라 파이썬 자동화 강의 신청
---

<https://www.acmicpc.net/problem/8901>

# 2020/11/02
- [x] 코세라 파이썬 자동화 강의

---

딱 자동화 파트만 듣고 싶었는데 5개 코스를 전부 수강하도록 되어 있었음

어차피 영어 강의니까 감회가 새로워서 지겹지는 않겠다 판단하여 수강함

일단 강의가 2~5분 단위로 굉장히 짧아서 좋았음

또한 굉장히 하이 텐션으로 강의해주셔서 왠지 모르게 나도 재밌게 느껴짐

강좌명이 Crash Course on Python 이었는데.. 이 하나의 강좌에도 4주차 이상임..

일단 1주차 강의 완강

어제 저녁에 수강 신청했으니 오늘이 벌써 2일차.. 후우후우 갈길이 멀다!!

엌.. 강의 다 듣고 있었는데 시험만 통과하면 굳이 아는 부분은 안들어도 되는 거였어..

딕셔너리 update라는거 처음 써봄

호다닥 달려서 Crash Course on Python 끝까지 수강함..

사실 final project를 정해진 환경에 적응이 안되서 검색하다가 답을 봐버렸음...

어찌어찌 지우고 스스로 다시 써봐도 대충 그 흐름이 기억이 나서 허허허

# 2020/11/03

- [x] 코세라 Using Python to Interact with the Operating System 강의 수강

---

아직 수강하기 전 : 데드락 방지를 위해 Lock을 다루는 내용이 있었으면 함. 프로젝트 진행하다가 막혀서 보면 항상 이쪽에서 문제를 일으켜서.. 한 번쯤 제대로 정리하고 넘어가고 싶었음

OS = 컴퓨터에서 우리가 하는 모든 것을 관리하는 소프트웨어

파일 관리, 프로세스 관리, 메모리 할당, 네트워크 전송 등등

운영체제에는 커널과 User space로 나뉨(이 이야기는 처음 들음.. 커널이 핵심이다만 알고 있었는데 신기하구먼)

하드웨어(CPU,Memory,I/O)와 통신하고 시스템 리소스를 관리함

User space는 커널 외부의 모든 것이라고 보면 된다고 함

UI같은게 이쪽 영역

파이썬은 Cross platform language라서 동일한 파이썬 코드로 다른 OS에서도 적용이 가능하다고 합니다.

```python3
import shutil
import psutil

du = shutil.disk_usage("/")#하드디스크 사용량
print(du)
print(psutil.cpu_percent(0.1))#CPU 사용량
```



```python3
import shutil
import psutil

def check_disk_usage(disk):
    du = shutil.disk_usage(disk)
    free = du.free/du.total*100
    return free>20

def check_cpu_usage():
    usage = psutil.cpu_percent(1)
    return usage<75

if not check_disk_usage("/") or not check_cpu_usage():
    print("error")
else:
    print("It's Okay")
```

Qwiklabs 는 온라인 VM인데 그냥 클라우드랑 뭐가 다른거지


```
#!/usr/bin/env python3
```
uses the operating system env command, which locates and executes Python by searching the PATH environment variable. Unlike Windows, the Python interpreter is usually already in the $PATH variable on linux, so you don't have to add it.

We got a permission denied error.

sudo chmod +x health_checks.py

권한을 주어서 해결

sudo apt install python3-requests

Create a file named network.py. 

```python3
#!/usr/bin/env python3
import requests
import socket

localhost = socket.gethostbyname('localhost')
request = requests.get("http://www.google.com")
```
저 status_code가 200일때 True해야한다는 내용을 놓쳐서 많이 낑낑거림

file open을 하면 close해주라

open되어있는 동안 다른데서 사용하지 못함

with block에서 파일을 열면 파이썬이 자동으로 close해줌

2주차까지 수강 완료

찾아보니까 전체 8개월짜리 강좌인데 7일만에 하려는게 어이없어짐 허허허

# 2020/11/04

오늘도 코세라 강의

정규식 다루는 중


```python3

#!/usr/bin/env python3

import re
import csv


def contains_domain(address, domain):
  """Returns True if the email address contains the given,domain,in the domain position, false if not."""
  domain = r'[\w\.-]+@'+domain+'$'
  if re.match(domain,address):
    return True
  return False


def replace_domain(address, old_domain, new_domain):
  """Replaces the old domain with the new domain in the received address."""
  old_domain_pattern = r'' + old_domain + '$'
  address = re.sub(old_domain_pattern, new_domain, address)
  return address

def main():
  """Processes the list of emails, replacing any instances of the old domain with the new domain."""
  old_domain, new_domain = 'abc.edu', 'xyz.edu'
  csv_file_location = '<csv_file_location>'
  report_file = '<path_to_home_directory>' + '/updated_user_emails.csv'
  user_email_list = []
  old_domain_email_list = []
  new_domain_email_list = []

  with open(csv_file_location, 'r') as f:
    user_data_list = list(csv.reader(f))
    user_email_list = [data[1].strip() for data in user_data_list[1:]]

    for email_address in user_email_list:
      if contains_domain(email_address, old_domain):
        old_domain_email_list.append(email_address)
        replaced_email = replace_domain(email_address,old_domain,new_domain)
        new_domain_email_list.append(replaced_email)

    email_key = ' ' + 'Email Address'
    email_index = user_data_list[0].index(email_key)

    for user in user_data_list[1:]:
      for old_domain, new_domain in zip(old_domain_email_list, new_domain_email_list):
        if user[email_index] == ' ' + old_domain:
          user[email_index] = ' ' + new_domain
  f.close()

  with open(report_file, 'w+') as output_file:
    writer = csv.writer(output_file)
    writer.writerows(user_data_list)
    output_file.close()

main()
```

# 2020/11/05

오늘도 코세라

subprocess.run()할때 명령의 출력을 처리 할 수 ​​있도록 capture_output이라는 매개 변수를 true로 설정합니다. 리턴코드,stdout,stderr확인 가능

unittest라는 모듈이 있음

unittest.TestCase

assertEqual로 input과 output이 잘이뤄지는지 체크가능

# 2020/11/06

Python OS 강의 Final project 제출함

정말 말 그대로 과제만 딱 했는데 자꾸 덜했다고 돌려보내서 이게 무슨 일인가 했더니

과제 하기 전에 있는 튜토리얼 같은 부분도 필수로 해야함..

이걸 몰라서 시간을 버렸네~

