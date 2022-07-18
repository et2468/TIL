# git이란
버전관리 프로그램</br>
파일버전을 변경사항과 최종버전만 남긴다

- 코드의 history를 관리
- 개발되어온 과정 파악 가능
- 이전버전과 비교, 분석가능
---
*중앙집중식 버전 관리* : 모든 버전이 한곳에 모여 관리

*분산 버전 관리* : 
여러곳에서 버전을 관리</br>
sync가 안맞게 된다</br>
서버가 날아가도 클라 컴퓨터로 

- 클라우드 처럼 git도 저장소 서비스 종류가 있음
- gitlab 개인적인 정보 올리는데 사용
- github 공개적인 정보 올리는데 사용

git은 분산버전관리프로그램 github는 git기반의 저장소 서비스

---
## github를 쓰면 뭐가 좋을까?
- 인스타그램처럼 회사가 나의 공부, 관심, 열정을 알 수 있는곳
---

**GUI** 그래픽을 통해 사용자가 컴퓨터가 상호작용</br>
**CLI** 명령어를 통해 사용자가 컴퓨터가 상호작용

- GUI 는 CLI보다 쉽지만 단계가 많고 컴퓨터의 성능을 더 많이 소모
- 수 많은 서버/개발 시스템이 CLI를 통한 조작 환경을 제공

---
## CLI 기본명령어
- ***touch*** : 파일생성명령어 (touch a.txt)//폴더는 생성할 수 없다 </br>
- ***ls*** : 현재 작업중인 디렉토리에 어떤 목록이 있는지 보여준다<br/>
- ***mkdir*** : 새 폴더를 생성하는 명령어<br>
- ***cd*** : 현재 작업중인 디렉토리를 변경하는 명령어 (cd fd -->cd/fd경로로 이동) (cd .. -->상위 폴더로 이동)<br/>
- ***start*** : 파일을 실제로 열어주는 명령어 (start a.txt -->a메모장실행<br/>
- #code a.txt vscode로 a.txt열기<br/>
- ***rm*** : 파일을 삭제하는 명령어<br/>
- ***rm -rf*** : 폴더를 삭제하는 명령어 (rm -rf fd)

---
## 절대경로와 상대경로
*절대경로* : 전체적인 경로 c:/사용자/... <br/>
*상대경로* : 현재작업 디렉토리 위치에서 상대적인 위치를 계산<br/>
- ./  현재 작업하는 폴더 의미
- ../  현재 작업 폴더의 상위폴더를 의미 
- ./c:/사용자/

---
## Markdown
- 문서의 구조와 내용을 쉽고 빠르게 작성 (html, typora)
- Markdown Cheat Sheet에서 마크다운 문법 확인가능

- github문서의 시작과 끝
- README.md 파일을 통해 오픈소스의 공식문서 작성
- 개인 프로젝트의 소개문서 작성
- 매일 학습한 내용 정리
- 마크다운을 이용한 블로그 운영
- MM, notion에서도 사용가능

---
## README.md
일반적으로 소프트웨어와 함께 분포<br/>
Github 프로젝트에서 가장 먼저 보는문서<br/>
금요일마다 관통프로젝트를 할때 1시간~1시간 반 정도 작성<br/>
시간내에 프로젝트를 마쳤지만 README쓰고 가야해서 늦을수도<br/>
작성형식은 따로 없으나 일반적으로 마크다운을 이용하여 작성<br/>
다운받은 템플릿 형식에 맞춰 장식

---
## Repository
- 특정 디렉토리를 버전관리하는 저장소
- ***git init*** 명령어로 로컬 저장소를 생성
- 로컬한경(사용중인 컴퓨터 환경)안에서 git으로 관리를 할려면 선언이 필요
<br/>이 폴더는 앞으로 git으로 버전관리할거야-->git init-->해당 폴더 안의 모든 파일을 버전관리
- ***.git*** : 디렉토리에 버전 관리에 필요한 모든 것이 들어있음


- git 선언이후<br/>
***ls -a*** 숨긴폴더까지 같이 나타남
- ./   ../   .git/   a.txt  '개발자로 성장하기.assets'/  '개발자로 성장하기.md'
명령프롬프트에 (master)가 추가됨

ctrl F1-숨김항목 체크

***rm -rf .git*** :	git파일 삭제, (master)삭제, 숨긴git파일 삭제

touch readme.md
start readme.md
---
##git 기본기
커밋은 3가지 영역으로 구분되어있다
1. working directory : 우리가 작업하고 있는 실제디렉토리 //실제 버전관리 대상에선 제외
2. staging area : 커밋으로 repository에 저장하기 전에 특정버전으로 관리하고 싶은 파일이 있는곳
3. repository : 커밋들이 저장되는곳
1에서 2로 3으로 옮김

1. untracked (new file) 이것을 명령어 git add를 통해 2로 옮김
2. staged (이름이 변경됨) 이것을 git commite을 통해 3으로 옮김
3. committed (이름이 변경됨)

1.에서 new file을 수정 시 modified로 이름이 바뀜
위의 작업을 똑같이 수행

## git 명령어
- git status : 깃의 상태를 확인한다. 1,2,3 각 단계에 어느 파일이 올라와져 있는가
- git rm --cached : 파일을 1로 내린다. / git add의 반대
- git add . : 현재 경로의 모든 파일을 2단계로 올리겠다

---
## git commit입력시
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

github 이메일을 넣자
git config --global user.email "csm66865407@gmail.com"
git config --global user.name "csm"

git config --global --list
user.email=csm66865407@gmail.com
user.name=csm

---

## 다시 git commit입력
git
vim 2가지 모드
1. command mode
2. edit mode

- 1모드에서 인설트 i클릭
- 2모드에서
- esc 연타 :wq 저장하고 나간다 
- :q! 저장하지 않고 나간다

---
## git log
- 로그에 메세지 추가 가능, 어떤 부분을 변경되었는지 작성
- i클릭 insert모드 로그에 메세지를 작성가능

- git commit -m "커밋 메세지를 입력하세요"
- 커밋메세지는 협업에서 정하기 다른사람이 알아보기 쉽게

---
## 왜 staging area를 거치는 걸까?
a,b,c라는 파일중 a,b만 개발이 완료되었을때 관리하고싶은 파일만 git add를 추가
확실히 버전을 관리하고 싶은 파일만 올리고 커밋을 하는게 합리적이라서 그렇다고 한다

***git log*** : git의 모든 히스토리를 확인할 때 사용<br/>
***git diff*** : 파일의 변경사항을 확인 할 수 있다
	
---
## repository생성
깃허브에서 remote repository생성

github repository 와  local repository연결

1. git remote add origin {주소}
2. git push origin master
3. 로컬에서 명령어로 origin(별명)주소로 연결한다
4. 로컬에 있는 커밋내역을 github repository로 올린다 (최신 업데이트
5. 로컬에서 명령어로 git remote -v로 현재 등록된 리모트에 대한 정보를 확인한다

---
## README.md를 수정하고 push하기
local repo에 github repo를 연결 (remote주소를 로컬에 등록한다)
등록을 해야지만 push/pull이 가능하다

github repository 내려받기
clone과 pull의 차이점
git clone은 복제, github repository를 로컬 pc에 복제를 한다 (.git파일도 같이 복제가 된다)
.git 파일 : git 설정이 있는 폴더, remote주소도 같이 복제가 된다. (git init을 할 필요가 없다, git remote add로 등록도 할 필요가 없다)
git pull은 remote repository에 있는 버전    과 동일한 버전으로 다운받는것, remote정보가 사전에 필요하다, 이미 git으로 관리가 되어 있어야 한다(.git폴더가 이미 있어야한다)
clone : init, remote, pull //최초 1회만 해주면 된다
이후는 push와 pull만 사용해주면 된다

github repository삭제
github- et2468/test-setting-danger zone-delet

새로운 repository만들기
TIL 파일
TIL작성법 구글링







