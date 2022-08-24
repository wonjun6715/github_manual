# 깃허브 사용법 정리
향후 추가할 내용이나 오류 해결 방법 등 계속해서 업데이트 예정

## 깃허브 commit/push 하는 방법(최초)
<pre>
<ol>
<li>사용할 깃허브 계정에 repository 생성</li>
<li>git init : git 초기화</li>
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

## 좋은 커밋 메시지의 8가지 규칙
<pre>
<li>제목과 본문을 한 줄 띄워 분리하기</li>
<li>제목은 영문 기준 50자 이내로</li>
<li>제목 첫 글자를 대문자로</li>
<li>제목 끝에 . 금지</li>
<li>제목은 명령조로</li>
<li>Github - 제목(이나 본문)에 이슈 번호 붙이기</li>
<li>본문은 영문 기준 72자마다 줄 바꾸기</li>
<li>본문은 어떻게보다 무엇을, 왜에 맞춰 작성하기</li>
</pre>









