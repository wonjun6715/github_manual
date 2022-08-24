# 깃허브 사용법 정리
#### 향후 추가할 내용이나 오류 해결 방법 등 계속해서 업데이트 예정

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
