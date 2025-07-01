**TBD(Trunk-Based Development) git 전략**은 모든 개발자가 **하나의 메인 브랜치(main, trunk)**를 중심으로 개발하는 방식입니다. 이 전략의 핵심은 **작고 빈번한 커밋**과 **빠른 머지**, 그리고 **장수(longevity)가 짧은 브랜치** 사용에 있습니다[1][2][3][4][5][7][8][9].

### 주요 특징

- **단일 메인 브랜치:** trunk(main) 브랜치 하나만 상시 운영하며, 항상 배포 가능한 상태로 유지합니다[2][3][4][5][7][8][9].
- **짧은 생명주기의 브랜치:** 필요할 때만 feature 브랜치를 생성하고, 작업이 끝나면 빠르게 trunk로 병합합니다. 오래 유지되는 브랜치는 지양합니다[1][4][5][9].
- **작은 단위의 작업:** 작업을 최대한 작은 단위로 쪼개어 자주 커밋하고, 빠르게 병합합니다[1][3][4][5][7].
- **빠른 코드 리뷰 및 머지:** 코드 리뷰와 병합이 지체되면 전략의 효과가 떨어지므로, 리뷰와 머지를 신속히 진행해야 합니다[5].
- **자동화된 테스트와 CI/CD:** trunk에 병합 전 자동화 테스트를 필수로 하며, CI/CD 파이프라인을 통해 trunk가 항상 배포 가능한 상태임을 보장합니다[5][6].
- **Branch by abstraction, Feature flags:** 장수 브랜치를 피하기 위해 추상화 레이어 도입이나 기능 플래그(Feature flag)를 적극 활용합니다[6].

### 실무 적용 방법

- **브랜치 명명:** release, feature, hotfix 등의 prefix를 강제하지 않으며, 필요에 따라 단명 브랜치를 생성합니다[6].
- **병합 방식:** 
  - `merge --squash` 방식으로 커밋 히스토리를 단순화하거나,
  - `rebase + merge --no-ff` 방식으로 히스토리 유지가 가능합니다[6].
- **릴리즈 관리:** trunk에서 release 브랜치를 잠깐 생성해 배포 준비를 하며, 필요시 cherry-pick으로 trunk의 커밋을 반영합니다. release 브랜치에서 trunk로 다시 병합하지 않습니다[6].
- **문제 발생 시:** trunk의 상태가 깨질 경우, 최우선으로 복구합니다[5][6].

### 장점

- **대규모 병합의 위험 감소:** 장기 브랜치가 없으므로 대규모 충돌이나 병합 이슈가 줄어듭니다[5].
- **최신 상태 유지:** trunk가 항상 최신 상태를 반영하므로, 개발자 모두가 최신 코드를 기반으로 작업할 수 있습니다[5][7].
- **배포 자동화/효율화:** CI/CD와 결합 시, 배포 빈도가 높고 안정적입니다[5][6].

### 주의사항 및 한계

- **자동화 인프라 필수:** 자동화 테스트와 CI/CD가 미흡하다면 trunk의 품질 보장이 어렵습니다[5][6].
- **팀 규모와 프로젝트 성격:** 대규모 팀이나, 여러 버전 지원이 필요한 경우에는 다른 브랜치 전략이 더 적합할 수 있습니다[6].

**TBD 전략은 빠른 개발 주기, 자동화된 품질 보증, 단순한 브랜치 관리가 필요한 SaaS, 웹서비스, DevOps 환경에 특히 적합합니다.** 반면, 정기적 대규모 릴리즈나 여러 버전 동시 지원이 필요한 프로젝트에는 Git-Flow 등 다른 전략이 더 나을 수 있습니다[1][6].
[1] https://velog.io/@ahn-sujin/효율적인-git-branch-전략을-향해-TBD에서-Git-Flow로
[2] https://helloinyong.tistory.com/335
[3] https://uhgenie7.github.io/docs/dev/git/trunk-based-development
[4] https://weaklion1.tistory.com/35
[5] https://www.anyflow.net/sw-engineer/trunk-based-development
[6] https://www.anyflow.net/sw-engineer/gitops-git-practices
[7] https://velog.io/@woohm402/why-TBD
[8] https://ltr2006.tistory.com/48
[9] https://disco-biscuit.tistory.com/207
