git init            : git 초기설정

git add "파일명"    : 특정파일 stage에 올림
git add ./          : 변경사항 전부 state에 올림

git commit              : 커밋 메세지 입력 창
git commit -m "메세지"  : 메세지 입력창 없이 바로 커밋가능
git commit -v           : 커밋사항 출력

git diff        : git add 전 파일의 변경사항 출력

git diff --staged : git add 후 파일의 변경사항 출력

git log     : 변경사항(Commit) 출력
git log --oneline : 간략하게 출력
git log -p "파일명" : 특정파일의 변경사항 출력
git log -n 커밋수   : 출력할 커밋의수 제한(최근 커밋부터)

git rm "파일명"
git rm -r "디렉터리명"

git rm --cached "파일명" : 로컬엔 남기되, git에선 remove

