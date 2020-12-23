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

