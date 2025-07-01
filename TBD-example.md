Trunk-Based Development(TBD) git 전략의 **절차를 간단한 예시 코드와 함께 설명**하면 아래와 같습니다.

### 1. main 브랜치에서 feature 브랜치 생성

```bash
git checkout main
git pull origin main
git checkout -b feature/header-section
```
- 항상 최신 main에서 새 브랜치를 짧게 만듭니다[1][3][7].

### 2. 기능 개발 및 커밋

```bash
# 코드 수정/추가
git add .
git commit -m "헤더 섹션 추가"
```
- 변경 사항을 작은 단위로 자주 커밋합니다[1][3][7].

### 3. main 브랜치로 병합

```bash
git checkout main
git pull origin main  # 혹시 동료가 main에 작업했을 수 있으니 최신화
git merge feature/header-section
git push origin main
```
- 작업이 끝나면 바로 main에 병합합니다.  
- 병합 전 반드시 main을 최신 상태로 맞춥니다[1][3][7].

### 4. (필요시) Pull Request(코드 리뷰)

- 협업 환경에서는 바로 push하지 않고 PR(Pull Request)로 코드 리뷰와 자동화 테스트를 거칩니다[2][5][7].

### 5. 브랜치 삭제

```bash
git branch -d feature/header-section
```
- 병합 후 feature 브랜치는 바로 삭제합니다.  
- 브랜치는 항상 짧게 유지합니다[1][3][7].

#### 전체 예시 절차

```bash
# 1. main에서 새 브랜치 생성
git checkout main
git pull origin main
git checkout -b feature/header-section

# 2. 개발 및 커밋
# (코드 수정)
git add .
git commit -m "헤더 섹션 추가"

# 3. main으로 병합
git checkout main
git pull origin main
git merge feature/header-section
git push origin main

# 4. 브랜치 삭제
git branch -d feature/header-section
```

**요약**
- main에서 짧은 feature 브랜치 생성 → 개발 및 커밋 → main으로 빠르게 병합 → 브랜치 삭제  
- 항상 main은 배포 가능한 상태로 유지  
- 자동화된 테스트(CI)와 코드 리뷰(Pull Request) 활용 권장[2][5][7]

이런 방식으로 TBD 전략을 실천할 수 있습니다.
[1] https://adjh54.tistory.com/364
[2] https://wonsss.github.io/etc/git-branch-strategy/
[3] https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development
[4] https://velog.io/@xmun74/Trunk-based-Development
[5] https://uhgenie7.github.io/docs/dev/git/trunk-based-development
[6] https://www.opsatscale.com/getting-started/Git-Trunk-based-development/
[7] https://bibi-story.tistory.com/59
[8] https://www.travis-ci.com/blog/explaining-trunk-based-development/
[9] https://circleci.com/blog/trunk-vs-feature-based-dev/
[10] https://helloinyong.tistory.com/335
[11] https://build-enough.tistory.com/383
[12] https://www.anyflow.net/sw-engineer/gitops-git-practices
[13] https://www.reddit.com/r/git/comments/14yyvvu/isnt_trunk_based_development_just_a_complete/?tl=ko
[14] https://velog.io/@draco94/%ED%98%91%EC%97%85%EC%9D%84-%EC%9C%84%ED%95%9C-%EA%B9%83-Trunk-Based-Development-%EC%A0%84%EB%9E%B5
[15] https://hackernoon.com/a-guide-to-git-with-trunk-based-development-93a350c
[16] https://tech.mfort.co.kr/blog/2022-08-05-trunk-based-development/
[17] https://medium.com/@sungjk/%EB%A7%A4%EC%9D%BC-%EB%B0%B0%ED%8F%AC%ED%95%98%EB%8A%94-%ED%8C%80%EC%9D%B4-%EB%90%98%EB%8A%94-%EC%97%AC%EC%A0%95-1-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EC%A0%84%EB%9E%B5-%EA%B0%9C%EC%84%A0%ED%95%98%EA%B8%B0-59484ede3186
[18] https://medium.com/@elischleifer/minimum-viable-git-for-trunk-based-development-81a5da7a77a7
[19] https://www.anyflow.net/sw-engineer/trunk-based-development
[20] https://softwareengineering.stackexchange.com/questions/442910/what-is-the-difference-between-trunk-based-development-and-gitflow
[21] https://softwareengineering.stackexchange.com/questions/450717/how-to-use-trunk-based-development-when-using-scrum
[22] https://www.reddit.com/r/git/comments/14yyvvu/isnt_trunk_based_development_just_a_complete/
[23] https://launchdarkly.com/blog/git-branching-strategies-vs-trunk-based-development/
[24] https://docs.aws.amazon.com/prescriptive-guidance/latest/choosing-git-branch-approach/trunk-branching-strategy.html
[25] https://www.getunleash.io/blog/how-to-implement-trunk-based-development-a-practical-guide
[26] https://trunkbaseddevelopment.com/
[27] https://www.atlassian.com/ko/continuous-delivery/continuous-integration/trunk-based-development
[28] https://www.reddit.com/r/devops/comments/wq1ht2/how_to_do_trunk_based_development_with_github/
