---
layout: post
title:  "깃헙명령어 모음"
date:   2022-05-06 10:27:42 +0900
categories: github git
---
# 1. git 명령어 모음

  ![test](https://user-images.githubusercontent.com/101091764/167056991-f29be9bc-56d5-4cfc-acfb-c1dad4f1e596.png)

### **Git 설치 (for ubuntu)

1) 터미널 (ctrl + Alt + T)  
2)  `sudo apt install git`  입력 (=> 설치완료)  
3)  `git --version`  입력 (=> 설치 확인 및 버전 확인)

## 1-1. GIT 명령어

분류

명령어

내용 설명

<새로운 저장소 생성>

**$ git init**

.git 하위 디렉토리 생성  
(폴더를 만든 후, 그 안에서 명령 실행 => 새로운 git저장소 생성)

<저장소 복제/다운로드(clone)>

**$ git clone <https:.. URL>**

기존 소스 코드 다운로드/복제

**$ git clone**  **/로컬/저장소/경로**

로컬 저장소 복제

**$ git clone 사용자명@호스트:/원격/저장소/경로**

원격 서버 저장소 복제

<추가 및 확정(commit)>

**$ git add <파일명>**  
**$ git add ***

커밋에 단일 파일의 변경 사항을 포함  
(인덱스에 추가된 상태)

**$ git add -A**

커밋에 파일의 변경 사항을 한번에 모두 포함

**$ git commit -m "커밋 메시지"**

커밋 생성  
(실제 변경사항 확정)

**$ git status**

파일 상태 확인

<가지(branch)치기 작업>

**$ git branch**

브랜치 목록

**$ git branch <브랜치이름>**

새 브랜치 생성 (local로 만듦)

**$ git checkout -b <브랜치이름>**

브랜치 생성 & 이동

**$ git checkout master**

master branch로 되돌아 옴

**$ git branch -d <브랜치이름>**

브랜치 삭제

**$ git push origin <브랜치이름>**

만든 브랜치를 원격 서버에 전송

**$ git push -u < remote > <브랜치이름>**

새 브랜치를 원격 저장소로 push

**$ git pull < remote > <브랜치이름>**

원격에 저장된 git 프로젝트의 현재 상태를 다운받고 + 현재 위치한 브랜치로 병합

<변경 사항 발행(push)>

**$ git push origin master**

변경사항 원격 서버에 업로드

**$ git push < remote > <브랜치이름>**

커밋을 원격 서버에 업로드

**$ git push -u < remote > <브랜치이름>**

커밋을 원격 서버에 업로드

**$ git remote add origin <등록된 원격 서버 주소>**

클라우드 주소 등록 및 발행  
(git에게 새로운 원격 서버 주소 알림)

**$ git remote remove <등록된 클라우드 주소>**

클라우드 주소 삭제

<갱신 및 병합(merge)>

**$ git pull**

원격 저장소의 변경 내용이 현재 디렉토리에 가져와지고(fetch) 병합(merge)됨

**$ git merge <다른 브랜치이름>**

현재 브랜치에 다른 브랜치의 수정사항 병합

**$ git add <파일명>**

각 파일을 병합할 수 있음

**$ git diff <브랜치이름><다른 브랜치이름>**

변경 내용 merge 전에 바뀐 내용을 비교할 수 있음

<태그tag 작업>

**$ git log**

현재 위치한 브랜치 커밋 내용 확인 및 식별자 부여됨

<로컬 변경사항 return 작업>

**$ git checkout -- <파일명>**

로컬의 변경 사항을 변경 전으로 되돌림

**$ git fetch origin**

원격에 저장된 git프로젝트의 현 상태를 다운로드

  

## 1-2. CLI (Command Line Interface) 명령어

-   명령어 인터페이스는 (마우스나 각종 UI 컴포넌트 대신) 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식

분류

명령어

의미

설명

<관리자 권한으로 실행>

**$ sudo**

(super user do)

1. 관리자만 읽을 수 있는 파일 읽기  
2. 새로운 프로그램 설치 (Ubuntu Linux)  
3. Notes : 새로운 프로그램 설치시 Package Manager를 이용하는 것이 보편적

<기본적인 unix/linux 명령어>

**$ ls**

(list)

파일보기

**$ al**

(all)

파일의 세부내용 확인

< $ ls -al의 상세 내용 (권한) >  
  
1. 접근권한 (읽기/쓰기/실행 가능)여부  
2. 링크된 파일 갯수  
3. 소유자  
4. 소유 그룹  
5. 파일 크기  
6. 만든 날짜  
7. 만든 시간  
8. 파일/디렉토리 이름

**$ cd**

(change directory)

디렉토리로 이동

**$ pwd**

(print working directory)

full 디렉토리 path 확인 /  
(디렉토리 위치 변경)

<디렉토리로 이동>

**$ cd ~**

홈 디렉토리 (현재 사용자 개인 파일 디렉토리)

**$ cd /**

루트 디렉토리 (시스템 최상위 디렉토리 확인) /  
(매우 중요한 디렉토리를 의미하며 관리자 권한 요구함)

**$ cd .**

현재 디렉토리

**$ cd ..**

부모 디렉토리

**$ pwd**

현재 full 디렉토리 확인

**$ clear**

터미널의 입력 내용들을 지워줌

<자주쓰는 명령어>

**$ touch [file_name]**

빈 파일 생성 / (not 디렉토리 / literally 파일을 생성)

**$ mkdir [dir_name]**

(make directory)

디렉토리 생성

**$ cat [file_name]**

(concatenate)

텍스트 형태의 파일 확인

**$ mv [file_name or dic_name][target_dir_name]**

(move)

파일 또는 디렉토리 옮기기

**$ mv [file_name or dir_name][new_file_name]**

파일 및 디렉토리 이름 바꾸기

**$ cp [file][target_dir_name]**

(copy)

복사

**$ cp -r [folder_name]**

복사

<삭제>  
(_주의!_  휴지통을 거치지 않고 즉시 삭제)

**$ rm [file_name]**

(remove)

파일 삭제

**$ rm -r [dir_name]**

폴더 삭제

<파일 소유권 변경>

**$ chown [owner_file]:[group_file]**

(change owner)

파일 소유권 변경

**$ mkdir**

디렉토리 생성

**$ rm**

삭제

<GUI프로그램의 실행을 더 간편하게>

**$ explorer .**

현재 폴더를 windows파일 관리자에서 보기

**$ open .**

현재 폴더를 macOS finder에서 보기

**$ code .**

현재 폴더를 VS Code 에디터로 열기

<파일 이름에 따른 팁>

공백이 있는 경우

공백부분에 tab 키를 누르기 or / (역슬래시)를 입력

파일 자동완성 기능

첫글자 등을 쓰고 tab 키 누르기

## 잘 몰랐던 git ...

-   branch에 기존 작업코드 복사하고 push하기
    
    -   branch 생성 후 이동 :  `git checkout -b expressPrac`
    -   확인 :  `git status`
    -   push 하기 :  `git push origin expressPrac`
-   `husky > pre-commit hook failed (add --no-verify to bypass)`  다음과 같은 에러와 함께 error때문에 commit 이 안될 때 (안쓰는 코드를 에러 처리해서 생긴 문제였음)
    

#### sklearn.ensemble.GradientBoostingClassifier
* _class_ sklearn.ensemble.GradientBoostingClassifier(_*_,  _loss='deviance'_,  _learning_rate=0.1_,  _n_estimators=100_,  _subsample=1.0_,  _criterion='friedman_mse'_,  _min_samples_split=2_,  _min_samples_leaf=1_,  _min_weight_fraction_leaf=0.0_,  _max_depth=3_,  _min_impurity_decrease=0.0_,  _init=None_,  _random_state=None_,  _max_features=None_,  _verbose=0_,  _max_leaf_nodes=None_,  _warm_start=False_,  _validation_fraction=0.1_,  _n_iter_no_change=None_,  _tol=0.0001_,  _ccp_alpha=0.0_)

> learning_rate: 


## Rename a file

You can rename the current file by clicking the file name in the navigation bar or by clicking the **Rename** button in the file explorer.

## Delete a file

You can delete the current file by clicking the **Remove** button in the file explorer. The file will be moved into the **Trash** folder and automatically deleted after 7 days of inactivity.

## Export a file

You can export the current file by clicking **Export to disk** in the menu. You can choose to export the file as plain Markdown, as HTML using a Handlebars template or as a PDF.


# Synchronization

Synchronization is one of the biggest features of StackEdit. It enables you to synchronize any file in your workspace with other files stored in your **Google Drive**, your **Dropbox** and your **GitHub** accounts. This allows you to keep writing on other devices, collaborate with people you share the file with, integrate easily into your workflow... The synchronization mechanism takes place every minute in the background, downloading, merging, and uploading file modifications.

There are two types of synchronization and they can complement each other:

- The workspace synchronization will sync all your files, folders and settings automatically. This will allow you to fetch your workspace on any other device.
	> To start syncing your workspace, just sign in with Google in the menu.

- The file synchronization will keep one file of the workspace synced with one or multiple files in **Google Drive**, **Dropbox** or **GitHub**.
	> Before starting to sync files, you must link an account in the **Synchronize** sub-menu.

## Open a file

You can open a file from **Google Drive**, **Dropbox** or **GitHub** by opening the **Synchronize** sub-menu and clicking **Open from**. Once opened in the workspace, any modification in the file will be automatically synced.

## Save a file

You can save any file of the workspace to **Google Drive**, **Dropbox** or **GitHub** by opening the **Synchronize** sub-menu and clicking **Save on**. Even if a file in the workspace is already synced, you can save it to another location. StackEdit can sync one file with multiple locations and accounts.

## Synchronize a file

Once your file is linked to a synchronized location, StackEdit will periodically synchronize it by downloading/uploading any modification. A merge will be performed if necessary and conflicts will be resolved.

If you just have modified your file and you want to force syncing, click the **Synchronize now** button in the navigation bar.

> **Note:** The **Synchronize now** button is disabled if you have no file to synchronize.

## Manage file synchronization

Since one file can be synced with multiple locations, you can list and manage synchronized locations by clicking **File synchronization** in the **Synchronize** sub-menu. This allows you to list and remove synchronized locations that are linked to your file.


# Publication

Publishing in StackEdit makes it simple for you to publish online your files. Once you're happy with a file, you can publish it to different hosting platforms like **Blogger**, **Dropbox**, **Gist**, **GitHub**, **Google Drive**, **WordPress** and **Zendesk**. With [Handlebars templates](http://handlebarsjs.com/), you have full control over what you export.

> Before starting to publish, you must link an account in the **Publish** sub-menu.

## Publish a File

You can publish your file by opening the **Publish** sub-menu and by clicking **Publish to**. For some locations, you can choose between the following formats:

- Markdown: publish the Markdown text on a website that can interpret it (**GitHub** for instance),
- HTML: publish the file converted to HTML via a Handlebars template (on a blog for example).

## Update a publication

After publishing, StackEdit keeps your file linked to that publication which makes it easy for you to re-publish it. Once you have modified your file and you want to update your publication, click on the **Publish now** button in the navigation bar.

> **Note:** The **Publish now** button is disabled if your file has not been published yet.

## Manage file publication

Since one file can be published to multiple locations, you can list and manage publish locations by clicking **File publication** in the **Publish** sub-menu. This allows you to list and remove publication locations that are linked to your file.


# Markdown extensions

StackEdit extends the standard Markdown syntax by adding extra **Markdown extensions**, providing you with some nice features.

> **ProTip:** You can disable any **Markdown extension** in the **File properties** dialog.


## SmartyPants

SmartyPants converts ASCII punctuation characters into "smart" typographic punctuation HTML entities. For example:

|                |ASCII                          |HTML                         |
|----------------|-------------------------------|-----------------------------|
|Single backticks|`'Isn't this fun?'`            |'Isn't this fun?'            |
|Quotes          |`"Isn't this fun?"`            |"Isn't this fun?"            |
|Dashes          |`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|


## KaTeX

You can render LaTeX mathematical expressions using [KaTeX](https://khan.github.io/KaTeX/):

The *Gamma function* satisfying $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$ is via the Euler integral

$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$

> You can find more information about **LaTeX** mathematical expressions [here](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference).


## UML diagrams

You can render UML diagrams using [Mermaid](https://mermaidjs.github.io/). For example, this will produce a sequence diagram:

```mermaid
sequenceDiagram
Alice ->> Bob: Hello Bob, how are you?
Bob-->>John: How about you John?
Bob--x Alice: I am good thanks!
Bob-x John: I am good thanks!
Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.

Bob-->Alice: Checking with John...
Alice->John: Yes... John, how are you?
```

And this will produce a flow chart:

```mermaid
graph LR
A[Square Rect] -- Link text --> B((Circle))
A --> C(Round Rect)
B --> D{Rhombus}
C --> D
```
