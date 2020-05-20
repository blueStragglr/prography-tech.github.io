# 	프로그라피 기술 블로그

프로그라피 기술 블로그입니다. 

https://prography-tech.github.io/

- 이 블로그는 Jekyll은 로 만들어져있습니다. 아래 사이트를 확인해 주세요
    https://jekyllrb-ko.github.io/docs/installation/
- 위 내용을 숙지 후 작업해주세요! 

## Getting Started

### 깃허브 설정 


1. https://github.com/prography-tech/prography-tech.github.io 포크 하기

2. 포크 저장소 계정(개인 계정) 선택

   ```bash
   $ git clone https://github.com/soomtopia/prography-tech.github.io.git
   $ cd prography-tech.github.io.git
   $ git remote add upstream git@github.com:prography-tech/prography-tech.github.io.git # 원격 저장소 등록
   ```

   리모트 확인

   ```bash
   $ git remote -v
   origin	https://github.com/user-name/prography-tech.github.io.git (fetch)
   origin	https://github.com/user-name/prography-tech.github.io.git (push)
   upstream	git@github.com:prography-tech/prography-tech.github.io.git (fetch)
   upstream	git@github.com:prography-tech/prography-tech.github.io.git(push)
   ```

   원격저장소와 동기화 
   
   ```
   $ git fetch upstream
   $ git checkout master
   $ git merge upstream/master
   ```

    이후 자신의 로컬에 add > commit > push 후 원격 master에 pull request 를 보내주세요! 
   
   

### 로컬에서 빌드하기

​	jekyll 관련 프로젝트를 완전히 처음 시작하는 경우, 아래의 단계를 거치면 성공적으로 로컬 환경에서 프로젝트를 빌드하고 테스	트 해 볼수 있습니다. 좀 더 자세한 매뉴얼은 https://jekyllrb-ko.github.io/docs/installation/ 를 참고하세요.

1. Ruby 설치하기 
   https://www.ruby-lang.org/en/downloads/ 를 참고하여 ruby를 설치 해 주세요. Mac OSX에는 보통 Ruby가 설치되어 있습니다. 설치 후 터미널 등에서 `$ ruby -v` 를 실행하여 Ruby가 정상적으로 설치되었는지 확인 해 주세요.
2. RubyGems 설치하기
   https://rubygems.org/pages/download 를 참고하여 RubyGems 또한 설치 해 주세요. Mac OSX에는 RubyGems 또한 설치되어 있는 경우가 많습니다. 설치 후 터미널 등에서 `$ gem -v` 를 실행하여 RubyGems가 정상적으로 설치되었는지 확인 해 주세요. 
3. Bundle 설치하기
   이제 사용하는 command line 도구(i.e. terminal)에서 프로젝트 폴더로 이동 해 주세요. 프로젝트 폴더의 최상위 경로에서 `$ bundle install` 을 실행하여 필요한 bundle들을 설치 해 줍니다. 해당 과정은 시간이 다소 소요됩니다!
4. 로컬 환경에서 실행하기
   이제 command line 도구에서 `$ jekyll serve` 를 실행하면 로컬 환경에서 빌드된 블로그를 확인할 수 있습니다. 



### 글 등록

1. _posts 폴더에 자신의 글을 이동시키기 

    - 형식은 markdown 

    - 제목 형식은  `yyyy-mm-dd-<title>.md`  (년-월-일)

2. 파일 최 상단에 레이아웃 등록하기

    sample

    ```
    # 2019-03-18-testposts.md
    ---
    layout: post #require
    title: "원하는 제목 등록"
    author: "자신의 작성 이름 등록"
    date: 2019-10-11 00:00 # 작성 날짜 등록 
    tags: [algorithm, python, djnago] # 원하는 태그 등록 
    image: 'https://github.com/jangjichang/Today-I-Learn/raw/master/Algorithm/theory/stack.jpg?raw=true' # 원하는 이미지 url 등록 
    ---
    # 이 아래에 마크다운 형식의 포스트를 작성하세요요요
    ```
    
    
        - 이미지의 경우 주소 url 을 붙히면 좋다
        - 로컬에 있는 이미지를 올리고 싶은 경우 assets/images 폴더에 넣자
        -  `assets/images/<photo-name>.jpg` 와 같이 등록한다. 
        -  마크다운 파일 안에서 상대경로로 불러오는 경우 올바르게 빌드되지 않는다! 마크다운 파일 안에도 `[image](assets/images/<photo-name>.jpg)` 와 같이 작성한다. 
        
        - __작성자와 태그가 authors , tags 에 등록되지 않았다면 등록 해주어야한다.__
    
    

### 작성자 등록하기

1. _authors 폴더에 `<user-name>.md` 이름으로 파일 등록하기

2. `<user-name>.md` 파일 최상단에 레이아웃 등록

   ```
   ---
   name: soomtopia
   title: 한수민 # 이름 또는 닉네임등록 
   image: https://avatars2.githubusercontent.com/u/50104236?s=460&v=4 # 프로필사진
   cover: # 배경사진
   intro: django # author list 에 django developer 로 명시됨
   ---
   # 자기 소개를 적으면 된다 
   ```

   ###### sample

   ```markdown
   ---
   name: bluestragglr
   title: 신성환
   image: https://avatars1.githubusercontent.com/u/44422495?s=400&v=4
   intro: vue.js developer
   
   ---
   
   안녕하세요. 저는 갓성환입니다. 요리 코딩 겅부 포켓몬 다 잘하죠 훗 
   
   ####  github
   http://github.com/blueStragglr
   
   #### 주요언어 
   vue.js / html / css / javascript
   ```

   ###### result

   <https://prography-tech.github.io/authors/bluestragglr/>



### 태그 등록하기 

자신이 달고싶은 태그가 현재 _tags 에 없다면 등록해준다. 

- _tags 폴더에 `<tag_name>.md` 형식으로 파일을 등록해준다

- 파일 최 상단에 아래와 같이 등록

  ```markdown
  ---
  name: algorithm
  title: 'algorithm'#태그에 대한 설명
  image: #태그 관련 이미지. 옵션
  ---
  ```
