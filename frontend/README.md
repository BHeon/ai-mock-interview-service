# 브랜치 사용 규칙 안내

이 프로젝트는 GitHub Pull Request와 CI를 사용하는 방식으로 협업합니다.
아래 순서를 꼭 지켜주세요.

# 브랜치 구성

## main
배포 기준 브랜치입니다.
직접 push 하지 않습니다.
PR과 CI 통과 후 관리자 승인으로만 병합됩니다.

## develop
개발 통합 브랜치입니다.
모든 기능은 develop을 기준으로 합쳐집니다.
직접 push 하지 않습니다.

## feature 브랜치
각자 기능 개발용 브랜치입니다.
본인 기능마다 하나씩 생성해서 사용합니다.

# 작업 순서

## develop 브랜치 최신 상태로 받기

git checkout develop  
git pull origin develop  

## 본인 기능 브랜치 생성

git checkout -b feature/기능명  

## 기능 구현 후 커밋

git add .  
git commit -m "기능 설명"  

작업 중간중간 여러 번 커밋해도 괜찮습니다.

## 기능 브랜치 원격 저장소에 push

git push origin feature/기능명  

GitHub에서 Pull Request 생성

base는 develop  
compare는 본인 feature 브랜치로 설정합니다.

PR을 생성하면 CI가 자동으로 실행됩니다.

# CI 통과 후 관리자 승인으로 merge

CI 실패 시 수정 후 다시 push 하면 자동으로 재검증됩니다.  
merge는 관리자만 진행합니다.

# Pull Request 관련 안내

Pull Request는  
내가 만든 기능을 develop 브랜치에 합쳐달라고 요청하는 과정입니다.

PR이 생성되거나 수정되면  
자동으로 CI가 실행되어 빌드 검증을 합니다.

# 주의사항

main 브랜치에 직접 push 하지 않습니다.  
develop 브랜치에 직접 push 하지 않습니다.  
PR 없이 merge 하지 않습니다.  
다른 사람 feature 브랜치에 커밋하지 않습니다.

# 한 줄 요약

## develop에서 브랜치를 따서 작업하고  
## feature 브랜치로 push한 뒤  
## Pull Request를 통해 CI 검증 후 merge합니다.
