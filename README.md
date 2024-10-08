# GIT 명령어

## 기본 명령어

1. git --version (git 버전 확인 방법)
2. git init (현재 프로젝트에서 변경사항 추적(버전 관리)을 시작)
3. git status (git 상태 확인)
4. git add . (모든 파일의 변경사항을 추적하도록 지정)
5. git commit -m "커밋 메시지" (메세지(-m)와 함께 버전을 생성)
6. git push origin master (origin이랑 별칭의 원격 저장소로 버전 내역 전송)
7. git pull (git 원격 저장소에서 업데이트 된 코드 다운로드)
8. git clone [주소](git 원격 저장소에서 코드 복제)
9. git remote add orgint [주소] (origin이랑 별칭으로 원격 저장소를 연결)
10. git reset --hard HEAD~1 (최신 커밋 하나를 취소하고 되돌아가기)
11. git reset --hard ORIG_HEAD (커밋 취소 된 상태에서 다시 복구 시킬 때)
12. git branch -m master main (마스터 브랜치 이름을 main으로 변경)

## 개행 문자(New line) 설정

### macOS

- $git config --global core.autocrlf input

### windows

- $git config --global core.autocrlf true

## 사용자 정보

### 커밋(버전 생성)을 위한 정보 등록

- $git config --global user.name "사용자 이름"
- $git config --global user.email "사용자 이메일"

## 구성 확인

### Q키를 눌러서 종료!

- $git config --global --list

## 새로운 프로젝트 Push

1.  git init
2.  git config --global init.defaultBranch main (마스터 브랜치 이름을 main으로 변경)
3.  git config --global core.autocrlf input
4.  git config --global user.name "사용자 이름"
5.  git config --global user.email "사용자 이메일"
6.  git config --global --list
7.  git add . (모든 파일 추가)
8.  git commit -m "커밋 메시지" (깃 커밋 생성)
9.  git log (깃 커밋 로그 확인)
10. git remote add origin [주소] (깃 원격 저장소 주소 추가)
11. git push origin master (깃 원격 저장소에 업로드)

## Branch 명령어

1. git branch (브랜치 목록 확인)
2. git branch -a (모든 브랜치 목록 확인)
3. git branch [브랜치 이름] (새로운 브랜치 생성)
4. git checkout [브랜치 이름] (브랜치 이동)
5. git merge [브랜치 이름] (브랜치 병합)
6. git branch -d [브랜치 이름] (브랜치 삭제)

## GIT 버전 관리하지 않을 폴더 및 파일 설정

- .gitignore 로 설정

```
  .idea
  .vscode
  .node_modules
  .DS_Store
```

- .gitignore 에 추가해야 하지만 실수로 하지 않았을 때 대처

```
  1. .gitignore 생성
  2. 추가할 파일 명시
  3. git rm -r --cached . (깃에 있는 파일이나 폴더를 전체 제거)
```

## GIT 브랜치 전량 (GIT FLOW)

- main(master) : 기본 / 메인 / 제품 브랜치
- dev(develop) : 다음 제품 출시를 위해 여러 기능을 병합하는 브랜치
- feature/\* : 각 기능 개발을 위한 브랜치
- release : 이번 제품 출시 직전 최종 테스트(QA)를 위한 브랜치
- hotfix : 제품에 버그가 확인되었을 떄 긴급 수정을 위한 브랜치

  ![alt text](/images/readme/image.png)
