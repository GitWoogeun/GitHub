# GitHub에 올리기 (협업의 시작)



### …or push an existing repository from the command line

뜻 : 현존하는 repository에 올리겠습니다



#### git remote add origin https://github.com/GitWoogeun/gitpractice.git

```javascript
이 repository에 origin이란 이름의 원격 저장소로 설정하겠다는 의미
origin은 기본값으로 사용(default)

출처:github repository에 있음
```



#### git remote add origin (해당 Repository URL) == git이랑 github연결 

```javascript
git remote add https://github.com/GitWoogeun/Spring.git
```

![git remote add URL](C:\gitproject\GIt사용법\이미지 파일\git remote add URL.PNG)



#### git remote -v (Git이랑 원격저장소인 GitHub와의 연결확인)

```javascript
git remote -v 연결 확인

git init한 폴더에서 git remote -v로 연결 확인을 하면된다.
밑에 문장처럼 
origin https://github.com/GitWoogeun/Spring.git(fetch)
origin https://github.com/GitWoogeun/Spring.git(push)
이런식으로 뜬다면 연결 성공!
```

![git remote](C:\gitproject\GIt사용법\이미지 파일\git remote.PNG)

![git -remote 연결성공](C:\gitproject\GIt사용법\이미지 파일\git -remote 연결성공.PNG)



#### git remote remoe origin = 현재 연결된 repository를 삭제

```javascript
git remote remove origin
순서
1). 현재 연결된 github의 repository확인
2). 현재 연결된 github의 repository 삭제
3). 잘 삭제 되었는지 확인

지우는 이유 : 다른 repository에 새로 연결해서 파일을 업로드 하기위해서
```

![git -remote 연결성공](C:\gitproject\GIt사용법\이미지 파일\git -remote 연결성공.PNG)

![git remote remove](C:\gitproject\GIt사용법\이미지 파일\git remote remove.png)

![git remote](C:\gitproject\GIt사용법\이미지 파일\git remote.PNG)



#### push 명령어

```javascript
git push -u origin master

현 브랜치에 컷된 내용들을 이 이름의 원격, 즉 이 레파지토리의 이 이름의 브랜치에 올리겠다 거에요~
```



#### 컴퓨터가 처음으로 git-hub에 파일을 업로드 할때는 user.name과 github ID를 물어볼껀데 입력하면된다. 

#### 그런 다음에 다시 명령어를 입력해주면된다.

```javascript
git remote add origin https://github.com/GitWoogeun/gitTest.git
git branch -M main
git push -u origin main
```



#### 입력하고 난뒤 이런 메세지가 뜨면 업로드 성공!

![업로드 성공 메세지](C:\gitproject\GIt사용법\이미지 파일\업로드 성공 메세지.PNG)



#### 위에 처음 컴퓨터가 push를 하고 난뒤는 부터는 위에 처럼 설정하면서 올리는것이 아닌 이제 기본 push명령어로 올릴수있음



#### 기본 push 명령어

```javascript
git push origin master

master부분이 main으로 되어있다면 branch main이 main으로 되어있기때문에
master로 바뀌어 주어야한다.

git branch -M master  (브랜치의 메인이 master라고 선언하는 명령어)
```

![git push 오리지널](C:\gitproject\GIt사용법\이미지 파일\git push 오리지널.PNG)



##### .gitignore = Git에 올리지않을 파일들

```javascript
제일먼저 .gitignore파일을 하나 만든다

echo 올리지않을파일>.gitignore

그 다음 올리지 않을 파일을 .gitignore파일에 집어 넣는다. (ex: 올리지않을파일.txt)

echo 올리지않을파일.txt>>.gitignore

이렇게하면 올리지않을파일.txt파일은 .gitignore로 들어가기 때문에 git에서 사라지고 commit을 할수없게 된다.
```

#### .gitignore파일생성

![gitignore](C:\gitproject\GIt사용법\이미지 파일\gitignore.PNG)

![gitignore파일 생성](C:\gitproject\GIt사용법\이미지 파일\gitignore파일 생성.PNG)



 #### 올리지않을 파일 생성

![올리지않을파일 생성](C:\gitproject\GIt사용법\이미지 파일\올리지않을파일 생성.PNG)

#### .gitignore에 올리지않을파일 집어넣기

![올리지않을파일을 gitignore파일로 집어넣기](C:\gitproject\GIt사용법\이미지 파일\올리지않을파일을 gitignore파일로 집어넣기.PNG)





#### git clone url(repository) = 해당 폴더와 똑같은 파일들을 복사

```javascript
먼저 repository의 (복사)클론파일 저장할 폴더를 하나 만들고

그 폴더로 들어가서 git clone repository(주소)하게 되면 해당 repository를 복사해서 가져올수있음
```

#### 먼저 clone할 폴더 생성 (폴더 이름 : clone으로 지정했음)

![clone할 파일생성](C:\gitproject\GIt사용법\이미지 파일\clone할 파일생성.PNG)

#### clone폴더로 들어가기

![git clone폴더로 들어가기](C:\gitproject\GIt사용법\이미지 파일\git clone폴더로 들어가기.PNG)

#### clone폴더에 들어가서 clone작업하기

![clone작업](C:\gitproject\GIt사용법\이미지 파일\clone작업.PNG)

#### clone폴더 안에 repository가져오기 성공!!

![해당 repository를 가져옴](C:\gitproject\GIt사용법\이미지 파일\해당 repository를 가져옴.PNG)



#### 내 repository에 누군가 파일을 올렸다!! (받을파일.txt파일 누군가 올렸다.)  (협업의 시작)

![누군가 내 repository에 파일을 올렸다](C:\gitproject\GIt사용법\이미지 파일\누군가 내 repository에 파일을 올렸다.PNG)

#### git fetch : github(내 repository)에 새로운 파일이 올라왔는지 확인! 

![git fetch](C:\gitproject\GIt사용법\이미지 파일\git fetch.PNG)

#### 그 다음 git status로 확인 하면된다.

```javascript
git status

Your branch is behind 'origin/master' by1 commit, add can be fast-forwarded. 라고 뜰것이다.
이 브랜치가 원격 origin의 마스터에 커밋 하나가 뒤쳐져 있다고 말해주는 것이다.
GitHub에서 다운 받아야 할 사항이 있다는 얘기에요
```



#### git pull origin master (다른쪽에서 내 repository에 올린 파일을 내 pc에 저장)

```javascript
git pull (원격명) (브랜치명)을 입력합니다.
그럼 뒤쳐진 커밋파일을 새로 다운받아진다. (내 ropository에 다른사람이 올린파일)
```

![git pull로 상대방에서 올린 파일 내 컴퓨터에도 저장](C:\gitproject\GIt사용법\이미지 파일\git pull로 상대방에서 올린 파일 내 컴퓨터에도 저장.PNG)

#### 그럼 이렇게 내 컴퓨터에 받을파일.txt 이 저장이 될것이다.

![내 컴퓨터에 새로올라간 파일 저장](C:\gitproject\GIt사용법\이미지 파일\내 컴퓨터에 새로올라간 파일 저장.PNG)

# 브랜치 주고 받기 (엄청 심화버전)



#### git checkout -b 브랜치명

```javascript
git checkout -b developking
이렇게하면 바로 developking 브랜치가 만들어져서 체크아웃까지 됩니다.
```

![한번에 브랜치 만들고 checkout까지 하기](C:\gitproject\GIt사용법\이미지 파일\한번에 브랜치 만들고 checkout까지 하기.PNG)



#### developking이라는 브랜치에서 clone폴더 저장 

![developking이라는 브랜치에서 clone폴더 저장](C:\gitproject\GIt사용법\이미지 파일\developking이라는 브랜치에서 clone폴더 저장.PNG)



#### banch = developking을 github에 만들어서 파일을 올리겠다.

![banch = developking을 github에 만들어서 파일을 올리겠다.](C:\gitproject\GIt사용법\이미지 파일\banch = developking을 github에 만들어서 파일을 올리겠다..PNG)



#### developking으로 파일 올라감

![developking branch로 파일 저장됨](C:\gitproject\GIt사용법\이미지 파일\developking branch로 파일 저장됨.PNG)

#### git branch 와 git branch -a의 차이

```javascript
git branch = 로컬저장소에있는 branch만 볼수 있지만
git branch -a = 로컬저장소와 원격저장소에 저장된 branch를 볼수 있습니다
```



#### git branch -a = 원격저장소(github)에 저장된 branch 보기

```javascript
git branch -a
```

![모든 banch 보기](C:\gitproject\GIt사용법\이미지 파일\모든 banch 보기.PNG)



#### 다른쪽에서 저장된 git branch로 이동하기

![git checkout 다른 branch로 이동](C:\gitproject\GIt사용법\이미지 파일\git checkout 다른 branch로 이동.PNG)



# 충동 해결하기 (이건 나중에 센터에서 해보기로 컴퓨터 하나로는 힘듬..)