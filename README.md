# 깃허브 사용법 정리
향후 추가할 내용이나 오류 해결 방법 등 계속해서 업데이트 예정

## 깃허브 commit/push 하는 방법(최초)
<pre>
<ol>
<li>사용할 깃허브 계정에 repository 생성</li>
<li>git init : git 로컬 저장소 만들기</li>
<li>git add <파일명> : git add . 은 모든 폴더/파일을 staging 추가</li>
<li>git commit -m '커밋 메시지' :  local repository에 추가(커밋 메시지 필수 입력)</li>
<li>git remote add origin <원격저장소URL> : 저장할 원격저장소 URL 복사하여 붙여넣기</li>
<li>git remote -v : 원격저장소와 잘 연결되었는지 확인</li>
<li>git push -u origin master : github에 최초 푸시</li>
</ol>
</pre>

## 깃허브 파일 업데이트 시 업로드 방법
<pre>
<ol>
<li>git add <업데이트할 파일명></li>
<li>git commit -m '커밋 메시지'</li>
<li>git push</li>
</ol>
</pre>

## 기존 repository remote 제거 - vscode에서 원격 저장소가 이미 연결되어 있을 때
<pre>
기존 repository 내용 제거
<ol>
<li>git pull</li>
<li>git add .</li>
<li>git commit -m 'clean push'</li>
</ol>
기존 repository 제거
<li>git remote remove origin (origin은 별칭이므로 자기 설정에 맞게 변경) *대부분 별칭은 origin으로 설정함</li>
</pre>

## 원격 저장소 이름 변경
<pre>
git remote rename <기존이름> <변경할이름>
</pre>

## 명령어 정리
<pre>
<ol>
<li>git log : 커밋 조회하기</li>
<li></li>
</ol>
</pre>

## 좋은 커밋 메시지의 8가지 규칙
<pre>
<li>제목과 본문을 빈 행으로 구분한다</li>
<li>제목은 영문 기준 50자 이내로</li>
<li>제목 첫 글자를 대문자로</li>
<li>제목 끝에 . 금지</li>
<li>제목은 명령조로</li>
<li>Github - 제목(이나 본문)에 이슈 번호 붙이기</li>
<li>본문은 영문 기준 72자마다 줄 바꾸기</li>
<li>본문은 어떻게보다 무엇을, 왜에 맞춰 작성하기</li>
</pre>

# 오류 해결 방법
### git push 오류 해결
<pre>
git push 명령어 실행시 Updates were rejected because the tip of your current branch is behind its remote.. 와 같은 오류 발생<br>
github repository를 생성할 때 READM.md를 생성했기 때문에 발생하는 오류라고 함.<br>
임시방편으로 +를 이용하여 해결이 가능 <br>
ex> git push -u origin +main(master)
</pre>

### .gitignore 파일 추가시
<pre>
repository에 파일이 있는 상태에서 .gitignore 파일을 push 해도 이미 자신의 깃허브에 올라가 있는 파일들은 ignore 되지 않는다.<br>
따라서 수동으로 해당 파일들을 버전 관리에서 제외해줘야 한다.<br>
git rm <파일명> : 원격 저장소와 로컬 저장소에 있는 파일 삭제<br>
git rm --cached <파일명> : 원격 저장소에 있는 파일만 삭제, 로컬 저장소에서는 삭제x<br>
<pre>
