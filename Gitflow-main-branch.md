## Git Flow 기반 코드 개발 절차 (Main 브랜치 사용)

Git Flow는 소프트웨어 개발을 위한 구조화된 브랜치 관리 전략으로, 여러 팀원이 동시에 작업할 수 있도록 돕습니다. 이 절차는 다음과 같은 단계로 구성됩니다:

### 1. 초기 설정

- **저장소 생성**: Git 저장소를 생성하고 초기화합니다.
- **브랜치 설정**: 기본적으로 `main`과 `develop` 브랜치를 설정합니다.
  - `main`: 항상 배포 가능한 안정적인 코드가 있는 브랜치.
  - `develop`: 다음 버전을 개발하는 브랜치.

### 2. 기능 개발

- **기능 브랜치 생성**: 새로운 기능을 개발하기 위해 `develop` 브랜치에서 기능 브랜치를 생성합니다.
  ```bash
  git checkout develop
  git pull origin develop
  git checkout -b feature/기능명
  ```
  
- **기능 개발**: 기능을 개발하고, 변경 사항을 자주 커밋합니다.
  ```bash
  git add .
  git commit -m "기능 추가 설명"
  ```

- **원격 저장소에 푸시**: 기능 브랜치를 원격 저장소에 푸시합니다.
  ```bash
  git push origin feature/기능명
  ```

- **풀 리퀘스트 생성**: GitHub 또는 GitLab에서 `feature` 브랜치에 대한 풀 리퀘스트를 생성하여 코드 리뷰를 요청합니다.

### 3. 기능 병합

- **리뷰 후 병합**: 코드 리뷰가 완료되면 `develop` 브랜치에 병합합니다.
  ```bash
  git checkout develop
  git merge feature/기능명
  git push origin develop
  ```

- **기능 브랜치 삭제**: 병합 후 더 이상 필요하지 않은 기능 브랜치를 삭제합니다.
  ```bash
  git branch -d feature/기능명
  git push origin --delete feature/기능명
  ```

### 4. 릴리스 준비

- **릴리스 브랜치 생성**: `develop` 브랜치에서 릴리스 브랜치를 생성하여 QA 및 최종 테스트를 진행합니다.
  ```bash
  git checkout develop
  git checkout -b release/버전번호
  ```

- **QA 및 수정**: 릴리스 브랜치에서 발견된 버그를 수정합니다. 수정 후 커밋합니다.
  ```bash
  git add .
  git commit -m "버그 수정 설명"
  ```

### 5. 릴리스 병합

- **릴리스 완료**: 릴리스가 준비되면 `main`과 `develop` 브랜치에 병합합니다.
  ```bash
  git checkout main
  git merge release/버전번호
  git push origin main

  git checkout develop
  git merge release/버전번호
  git push origin develop
  ```

- **버전 태그 추가**: 릴리스된 버전에 태그를 추가합니다.
  ```bash
  git tag -a v버전번호 -m "릴리스 설명"
  git push origin --tags
  ```

### 6. 핫픽스 처리

- **핫픽스 브랜치 생성**: `main`에서 핫픽스가 필요할 경우 핫픽스 브랜치를 생성합니다.
  ```bash
  git checkout main
  git checkout -b hotfix/버전번호
  ```

- **버그 수정**: 핫픽스 브랜치에서 버그를 수정하고 커밋합니다.
  ```bash
  git add .
  git commit -m "핫픽스 설명"
  ```

- **핫픽스 병합**: 수정이 완료되면 `main`과 `develop` 브랜치에 병합합니다.
  ```bash
  git checkout main
  git merge hotfix/버전번호
  git push origin main

  git checkout develop
  git merge hotfix/버전번호
  git push origin develop
  ```

- **핫픽스 브랜치 삭제**: 핫픽스 브랜치를 삭제합니다.
  ```bash
  git branch -d hotfix/버전번호
  git push origin --delete hotfix/버전번호
  ```

이러한 단계들을 통해 Git Flow를 기반으로 한 체계적인 코드 개발 절차를 수행할 수 있습니다. 각 단계는 팀의 협업을 원활하게 하고, 코드의 품질을 높이는 데 기여합니다.
[1] https://overcome-the-limits.tistory.com/entry/%ED%98%91%EC%97%85-%ED%98%91%EC%97%85%EC%9D%84-%EC%9C%84%ED%95%9C-Git-Flow-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0
[2] https://adjh54.tistory.com/364
[3] https://korin-learning.tistory.com/139
[4] https://medium.com/daangn/%EB%A7%A4%EC%9D%BC-%EB%B0%B0%ED%8F%AC%ED%95%98%EB%8A%94-%ED%8C%80%EC%9D%B4-%EB%90%98%EB%8A%94-%EC%97%AC%EC%A0%95-1-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EC%A0%84%EB%9E%B5-%EA%B0%9C%EC%84%A0%ED%95%98%EA%B8%B0-1a1df85b2cff
[5] https://inpa.tistory.com/entry/GIT-%E2%9A%A1%EF%B8%8F-github-flow-git-flow-%F0%9F%93%88-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EC%A0%84%EB%9E%B5
[6] https://gmlwjd9405.github.io/2018/05/12/how-to-collaborate-on-GitHub-3.html
[7] https://www.sktenterprise.com/bizInsight/blogDetail/dev/8122
[8] https://wonsss.github.io/etc/git-branch-strategy/
[9] https://castellan.tistory.com/79
[10] https://velog.io/@king_nono_1030/git-git-flow-strategy
[11] https://velog.io/@party3205/git-branch-git-flow-%EC%A0%95%EB%A6%AC
[12] https://burningfalls.github.io/git/git-flow/
[13] https://xxeol.tistory.com/37
[14] https://devocean.sk.com/blog/techBoardDetail.do?ID=165571&boardType=techBlog
[15] https://techblog.woowahan.com/2553/
[16] https://davidregalado255.medium.com/what-is-gitflow-b3396770cd42
[17] https://blog.ull.im/engineering/2019/06/25/git-workflow-for-ci-cd.html
[18] https://yeoonjae.tistory.com/entry/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-Git-flow-master-%EB%B0%8F-develop-branch-%EC%84%A4%EC%A0%95
[19] https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
[20] https://dev.to/ajmal_hasan/beginner-friendly-git-workflow-for-developers-2g3g
[21] https://m.blog.naver.com/adamdoha/222712473510
[22] https://medium.com/@cobchenyuk/git-flow-complete-guide-to-development-workflow-b732bf896a31
[23] https://nvie.com/posts/a-successful-git-branching-model/
[24] https://stackoverflow.com/questions/39478482/how-to-create-development-branch-from-master-on-github
[25] https://danielkummer.github.io/git-flow-cheatsheet/
[26] https://www.reddit.com/r/git/comments/16jcho9/how_to_manage_dev_and_main_branch_when_release/
[27] https://www.gitkraken.com/learn/git/git-flow
[28] https://geekiebarbs.hashnode.dev/gitflow-branching-model
