Bitbucket에서 **풀리퀘스트(Pull Request, PR) 중심의 처리 절차**는 다음과 같은 단계로 진행됩니다.

**1. 브랜치 생성 및 작업 분리**

- 새로운 기능 개발, 버그 수정 등 각 작업은 별도의 브랜치에서 시작합니다.
- 브랜치는 Bitbucket 웹 UI 또는 로컬에서 생성할 수 있습니다.
- 로컬에서 작업한 후 변경사항을 커밋하고, Bitbucket 원격 저장소로 푸시합니다[1][3].

**2. 풀리퀘스트 생성**

- 작업이 완료된 브랜치를 메인(또는 다른 대상) 브랜치에 병합하기 위해 풀리퀘스트를 생성합니다.
- Bitbucket 리포지토리에서 **+** 버튼을 클릭하고 **Create a pull request(풀리퀘스트 만들기)**를 선택합니다.
- 풀리퀘스트 양식에서 다음을 지정합니다:
  - **Source(원본)**: 변경사항이 있는 브랜치
  - **Destination(대상)**: 병합하려는 브랜치(예: main)
  - **Title(제목)**, **Description(설명)**: 변경사항 요약 및 상세 설명
  - **Reviewers(검토자)**: 코드 리뷰를 담당할 팀원 지정[1][3].

**3. 코드 리뷰 및 피드백**

- 검토자는 풀리퀘스트에서 변경된 코드(diff)와 커밋 내역을 확인할 수 있습니다.
- 코드의 특정 부분, 파일, 혹은 전체에 대해 댓글이나 피드백을 남길 수 있습니다.
- 필요에 따라 작성자는 피드백을 반영해 추가 커밋을 올릴 수 있습니다[1][3].

**4. 승인 및 병합**

- 충분한 리뷰와 승인을 받으면, 풀리퀘스트 작성자 또는 관리자 권한을 가진 사용자가 **Merge(병합)** 버튼을 클릭해 브랜치를 병합합니다.
- 병합 후에는 옵션에 따라 소스 브랜치를 자동으로 삭제할 수도 있습니다[1].

**5. 자동화 및 배포(선택 사항)**

- Bitbucket Pipelines와 같은 CI/CD 도구를 연동하면, 풀리퀘스트 병합 시 자동으로 빌드, 테스트, 배포가 진행될 수 있습니다.
- 예를 들어, main 브랜치에 병합될 때 스테이징 환경에 배포하고, production 브랜치에 병합될 때 프로덕션에 배포하도록 파이프라인을 구성할 수 있습니다[2].

**요약 표**

| 단계             | 주요 내용                                         |
|------------------|--------------------------------------------------|
| 브랜치 생성      | 작업 분리, 로컬/원격 브랜치 생성 및 푸시         |
| 풀리퀘스트 생성  | 병합 요청, 검토자 지정, 변경사항 설명            |
| 코드 리뷰        | 변경 코드 확인, 피드백 및 추가 커밋              |
| 승인 및 병합     | 리뷰 후 승인, 병합 버튼 클릭, 브랜치 삭제 가능    |
| 자동화/배포      | CI/CD 연동 시 자동 빌드·테스트·배포(선택 사항)   |

**Bitbucket 풀리퀘스트 중심 개발 프로세스의 장점**
- 코드 품질 향상: 여러 명이 코드 리뷰에 참여하여 버그와 문제를 사전에 발견할 수 있습니다.
- 협업 및 기록: 변경 이력과 피드백이 모두 기록되어 투명한 협업이 가능합니다.
- 자동화 연계: CI/CD와 연동해 효율적인 배포 및 테스트가 가능합니다[1][2][3].

출처
[1] Bitbucket으로 더 나은 코드 만들기: 시작 4단계 https://www.atlassian.com/ko/software/bitbucket/guides/basics/four-starting-steps
[2] Bitbucket Pipelines를 통한 지속적 배포에 대해 알아보기 https://www.atlassian.com/ko/devops/continuous-delivery-tutorials/continuous-delivery-bitbucket-pipelines
[3] Bitbucket Cloud에서 코드 리뷰에 대해 알아보기 https://www.atlassian.com/ko/git/tutorials/learn-about-code-review-in-bitbucket-cloud
[4] [PDF] KOREA STARTUP INDEX 2019 https://dev.born2global.com/data/dext5/2020/10/20201023_150931269_70228.pdf
[5] 2020년 상반기. 양질의 기술 아티클 모음 - velog https://velog.io/@rkdrhksdn/2020%EB%85%84-%EC%83%81%EB%B0%98%EA%B8%B0-%EC%96%91%EC%A7%88%EC%9D%98-%EA%B8%B0%EC%88%A0-%EC%95%84%ED%8B%B0%ED%81%B4-%EB%AA%A8%EC%9D%8C%EC%A7%91
[6] 소프트웨어 부트캠프 설계 및 운영사례(42Seoul) | PDF - SlideShare https://www.slideshare.net/slideshow/ss-256674213/256674213
[7] 키자드에 등록된 zzang9ha의 네이버 블로그 포스트 목록 https://keyzard.org/register/nb/zzang9ha
