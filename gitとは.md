<ol>
    <ul>
        git init            : git 초기설정
    </ul>
</ol>

<ol>
    <ul>
    git add "파일명"    : 특정파일 stage에 올림
    </ul>
    <ul>
    git add ./          : 변경사항 전부 state에 올림
    </ul>
</ol>

<ol>
    <ul>
    git commit              : 커밋 메세지 입력 창
    </ul>
    <ul>
    git commit -m "메세지"  : 메세지 입력창 없이 바로 커밋가능
    </ul>
    <ul>
    git commit -v           : 커밋사항 출력
    </ul>
</ol>
<ol>
    <ul>
    git diff        : git add 전 파일의 변경사항 출력
    </ul>
    <ul>
    git diff --staged : git add 후 파일의 변경사항 출력
    </ul>
</ol>

<ol>
    <ul>
    git log     : 변경사항(Commit) 출력
    </ul>
    <ul>
    git log --oneline : 간략하게 출력
    </ul>
    <ul>
    git log -p "파일명" : 특정파일의 변경사항 출력
    </ul>
    <ul>
    git log -n 커밋수   : 출력할 커밋의수 제한(최근 커밋부터)
    </ul>
</ol>

<ol>
    <ul>
    git rm "파일명"
    </ul>
    <ul>
    git rm -r "디렉터리명"
    </ul>
    <ul>
    git rm --cached "파일명" : 로컬엔 남기되, git에선 remove
    </ul>
    <ul>
    디테일한 작동원리는 모르나
    git rm 후 add 안했을 시
    - git reset HEAD "파일명"
    - git checkout "파일명"
    - 실행시 rm한 파일 복구 
    서로 하는 역할 다름
    </ul>
</ol>

<ol>
    <ul>
    git remote add origin "github url"
    </ul>
    <ul>
    git push <리모트명> <브런치명>
    git push origin master
    </ul>
</ol>

<ol>
    <p>alias 설정하기</p>
    <ul>
    git config --global alias.ci commit
    : commit의 단축어로 ci 설정
    git config --global alias.st status
    : status의 단축어로 st 설정
    git config --global alias.br brunch
    : brunch의 단축어로 br 설정
    git config --global alias.co checkout
    : checkout의 단축어로 co 설정
    </ul>
    <ul>
    git config --global alias.st status
    git st = git status
    </ul>
</ol>

<ol>
    <p>.gitignore</p>
    <ul>
        #으로 시작하는 행은 코멘트
    </ul>
</ol>

<ol>
    <ul>
        git reset HEAD
        : 스테이지에 올린 변경사항을 취소함
    </ul>
    <ul>
        git checkout -- "파일명"
        git checkout -- "디렉터리명"
        : 파일, 폴더 변경을 취소함
        // add 안돼있다면, 직전 커밋한 스냅샷으로 되돌림
        git checkout -- .
        : 전체 변경 취소
    </ul>
</ol>

<ol>   
    <p>직전 커밋 고치기</p>
    <ul>
        git commit --amend
        - 깃허브에 Push한커밋은 되돌릴수없음
    </ul>
</ol>

<ol>
    <ul>
        git remote
        : 리모트 출력
    </ul>
    <ul>
        git remote -v
        : 리모트 + url(fetch : 가져오기, push : 올리기)
    </ul>
    <ul>
        git remote add 리모트명 리모트url
        : git remote add tutorial "url"
    </ul>
</ol>

<ol>
    <ul>
        git fetch 리모트명
        : git fetch origin
        : 깃허브에서 업데이트된 변경사항을 로컬레포로 가져오기
    </ul>
</ol>
<ol>
    <ul>
        git pull 리모트명 브런치명
        : git pull origin master
        : fetch + merge 기능
    </ul>
    <ul>
        pull의 주의점
        : git pull origin hoge 실행시
        - master 브랜치에 hoge 브랜치가 merge됨(현재 브랜치에 pull한 브랜치가 병합됨) * 주의 ! *
        - 확실히 이해하고 사용하자
    </ul>
</ol>
<ol>
    <ul>
        - git remote show origin
        - Fetch, Push의 URL
        - remote 브랜치
        - git pull과 git push의 활동
    </ul>
</ol>
<ol>
    <ul>
        - git remote rename 구리모트명 신리모트명
        : git remote rename tutorial new_tutorial
        : 리모트명 변경시
        - git rm 리모트명
        : git remote rm new_tutorial
        : 리모트 삭제시
    </ul>
</ol>
<ol>
    <ul>
        branch와 merge
    </ul>
    <ul>
        branch
        : 분리해서 개발하기 위한 것
        : 커밋을 가리키는 포인터
        HEAD
        : 지금 작업하고 있는 브랜치(가장 최근 커밋한 브랜치)
    </ul>
    <ul>
        - 브랜치 정리
        1. 분리해서 복수의 기능을 동시에 개발하기 위한 구조
        2. 브랜치는 커밋을 가리키는 포인터
        3. 브랜치 작성, 변경, merge가 다른 버전관리 툴보다 빠르다
        4. 그래서 git은 대규모 개발에 많이 사용되는 툴이다.
    </ul>
</ol>
<ol>
    <ul>
        git branch 브랜치명
        : git  branch feature
        : 브랜치를 신규추가
    </ul>
    <ul>
        git branch
        git branch -a
        : 브랜치 일람을 표시
    </ul>
    <ul>
        git log --oneline --decorate
        : 브랜치 변경 확인
        : d3b93ec (HEAD -> master, origin/master, feature) 201224 새벽공부 깃 어렵다
    </ul>
</ol> 
<ol>
    <ul>
        git checkout 존재브랜치명
        : git checkout 
        : 브랜치 변경
        git checkout -b 신규브랜치명
        : 브랜치를 만들면서 변경
    </ul>
</ol>
