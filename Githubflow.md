## GitHub 전략 설명

GitHub에서의 브랜치 전략은 주로 **Git Flow**와 **GitHub Flow** 두 가지로 나눌 수 있습니다. 이 두 전략은 각각의 개발 환경과 팀의 요구에 따라 다르게 적용됩니다.

**Git Flow**

Git Flow는 복잡한 프로젝트에 적합한 전략으로, 다음과 같은 주요 브랜치가 포함됩니다:

- **master**: 배포 가능한 상태의 코드가 있는 브랜치입니다.
- **develop**: 다음 버전을 개발하는 브랜치입니다.
- **feature**: 새로운 기능을 개발하기 위한 브랜치로, develop 브랜치에서 분기됩니다.
- **release**: 배포 준비가 완료된 버전을 위한 브랜치입니다.
- **hotfix**: 배포된 코드에서 발생한 버그를 수정하기 위한 브랜치입니다.

이 전략은 명확한 구조를 제공하여 여러 개발자가 동시에 작업할 수 있도록 도와줍니다. 각 브랜치는 특정 목적을 가지고 있으며, 이를 통해 코드의 안정성을 높이고, 버전 관리를 용이하게 합니다[2][3][4].

**GitHub Flow**

GitHub Flow는 Git Flow보다 간단한 구조를 가지고 있으며, 주로 웹 애플리케이션 개발에 적합합니다. 이 전략의 주요 특징은 다음과 같습니다:

- **master**: 항상 배포 가능한 상태를 유지해야 하며, 모든 커밋은 빌드와 테스트를 통과해야 합니다.
- 새로운 기능이나 버그 수정을 위해 **topic 브랜치**를 master 브랜치에서 생성합니다.
- 작업이 완료되면 pull request를 통해 master 브랜치에 병합합니다.

GitHub Flow는 자동화된 배포를 지원하며, 지속적인 통합(CI) 및 지속적인 배포(CD)를 실현하기에 적합합니다. 이 전략은 특히 소규모 팀이나 자주 배포해야 하는 프로젝트에 유리합니다[2][4][5].

### **비교**

- **복잡성**: Git Flow는 복잡한 구조를 가지고 있어 대규모 프로젝트에 적합하지만, GitHub Flow는 간단하고 빠른 배포가 가능하여 소규모 프로젝트에 적합합니다.
  
- **버전 관리**: Git Flow는 여러 버전을 동시에 관리할 수 있는 반면, GitHub Flow는 최신 버전 하나만을 관리하는 데 초점을 맞춥니다.

- **자동화**: GitHub Flow는 CI/CD를 통해 자동화된 배포를 지원하는 반면, Git Flow는 수동으로 배포를 관리해야 할 경우가 많습니다[3][6][12].

이러한 전략들은 팀의 개발 스타일과 프로젝트의 요구 사항에 따라 선택되어야 하며, 각 전략의 장단점을 고려하여 최적의 방법을 결정하는 것이 중요합니다.
[1] https://parkstate.tistory.com/33
[2] https://inpa.tistory.com/entry/GIT-%E2%9A%A1%EF%B8%8F-github-flow-git-flow-%F0%9F%93%88-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EC%A0%84%EB%9E%B5
[3] https://www.gitkraken.com/learn/git/best-practices/git-branch-strategy
[4] https://hudi.blog/git-branch-strategy/
[5] https://devocean.sk.com/blog/techBoardDetail.do?ID=165571&boardType=techBlog
[6] https://www.harness.io/blog/github-flow-vs-git-flow-whats-the-difference
[7] https://rewind.com/blog/git-branching-strategies-explained/
[8] https://docs.github.com/en/get-started/using-github/github-flow
[9] https://velog.io/@kmina02/Git-%EA%B9%83-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EC%A0%84%EB%9E%B5-%EA%B0%9C%EB%85%90-%EC%A0%95%EB%A6%AC-%EC%9B%8C%ED%81%AC%ED%94%8C%EB%A1%9C%EC%9A%B0Git-Flow-Github-Flow
[10] https://www.abtasty.com/blog/git-branching-strategies/
[11] https://ksh-coding.tistory.com/109
[12] https://medium.com/@sreekanth.thummala/choosing-the-right-git-branching-strategy-a-comparative-analysis-f5e635443423
[13] https://gist.github.com/ihoneymon/a28138ee5309c73e94f9
[14] https://velog.io/@kw2577/Git-branch-%EC%A0%84%EB%9E%B5
[15] https://docs.aws.amazon.com/prescriptive-guidance/latest/choosing-git-branch-approach/advantages-and-disadvantages-of-the-git-hub-flow-strategy.html
[16] https://source-sc.tistory.com/74
[17] https://twojun-space.tistory.com/204
[18] https://www.reddit.com/r/webdev/comments/1hp1rad/can_someone_explain_to_me_how_branching_works_in/
[19] https://www.reddit.com/r/git/comments/1972njp/git_workflows_best_practices_branching_strategies/
