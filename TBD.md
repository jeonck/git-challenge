## TBD(Trunk Based Development) 전략

**TBD의 개념**

TBD, 즉 Trunk Based Development는 소프트웨어 개발에서 모든 개발자가 단일 브랜치인 'trunk' 또는 'main'에 자주, 소규모로 커밋하는 전략입니다. 이 방식은 코드의 배포 가능 상태를 항상 유지하며, 개발자들이 각자의 작업을 신속하게 통합할 수 있도록 돕습니다[2][7][19].

**TBD의 장점**

1. **빠른 피드백**: 작은 변경 사항을 자주 커밋함으로써, 코드 변경에 대한 피드백을 빠르게 받을 수 있습니다. 이는 코드 리뷰와 테스트를 용이하게 만들어, 전체적인 코드 품질을 향상시킵니다[4][14].

2. **충돌 최소화**: 여러 개발자가 동시에 작업할 때 발생할 수 있는 충돌을 줄입니다. 각 개발자는 trunk에 직접 커밋하기 전에 코드 리뷰와 테스트를 통해 문제를 사전에 해결할 수 있습니다[5][11].

3. **지속적 통합**: TBD는 지속적 통합(CI)과 잘 결합되어, 코드 변경 사항이 즉시 통합되고 테스트됩니다. 이는 배포 주기를 단축시키고, 배포 과정에서의 리스크를 줄입니다[3][19].

4. **단순한 브랜치 관리**: 복잡한 브랜치 구조를 피하고, 모든 개발자가 동일한 코드베이스에서 작업하도록 강제함으로써, 코드의 일관성을 유지할 수 있습니다[6][10].

**TBD의 실행 방법**

- **작업 단위 쪼개기**: 개발자는 큰 기능을 작은 단위로 나누어 작업하고, 이를 trunk에 빠르게 반영해야 합니다. 이렇게 하면 각 커밋이 작고 관리하기 쉬워집니다[5][8].

- **자동화된 테스트**: 모든 커밋은 자동화된 테스트를 통과해야 하며, 이를 통해 trunk의 안정성을 보장합니다[11][15].

- **코드 리뷰와 실시간 커뮤니케이션**: 팀원 간의 실시간 코드 리뷰와 커뮤니케이션을 통해 코드 품질을 높이고, 문제를 조기에 발견할 수 있습니다[4][19].

**결론**

TBD는 특히 소규모 팀이나 빠른 배포가 필요한 프로젝트에서 유용한 전략입니다. 이 방식은 코드의 일관성을 유지하고, 개발자 간의 협업을 촉진하며, 배포 주기를 단축시키는 데 큰 도움이 됩니다. 따라서, 기존의 복잡한 브랜치 전략에서 벗어나 TBD를 도입하는 것은 많은 팀에게 긍정적인 변화를 가져올 수 있습니다[2][3][19].
[1] https://aliencoder.tistory.com/79
[2] https://velog.io/@woohm402/why-TBD
[3] https://softwareengineering.stackexchange.com/questions/450717/how-to-use-trunk-based-development-when-using-scrum
[4] https://www.toptal.com/software/trunk-based-development-git-flow
[5] https://helloinyong.tistory.com/335
[6] https://launchdarkly.com/blog/git-branching-strategies-vs-trunk-based-development/
[7] https://velog.io/@xmun74/Trunk-based-Development
[8] https://ltr2006.tistory.com/48
[9] https://www.anyflow.net/sw-engineer/gitops-git-practices
[10] https://softwareengineering.stackexchange.com/questions/442910/what-is-the-difference-between-trunk-based-development-and-gitflow
[11] https://softengbook.org/articles/branching-strategies
[12] https://medium.com/@mridulpandey/git-branching-strategy-33d1565ddee5
[13] https://pgo-dev.medium.com/git-flow-vs-tbd-%EC%96%B4%EB%96%A4-%EB%B2%84%EC%A0%84%EA%B4%80%EB%A6%AC-%EC%A0%84%EB%9E%B5%EC%9D%B4-%EC%9C%A0%EB%A6%AC%ED%95%A0%EA%B9%8C-cd238d3f2ff4
[14] https://uhgenie7.github.io/docs/dev/git/trunk-based-development
[15] https://www.anyflow.net/sw-engineer/trunk-based-development
[16] https://pypy.dev/dev/git-flow-%EC%9E%98%EB%AA%BB-%EC%93%B0%EA%B3%A0-%EC%9E%88%EC%97%88%EB%8B%A4-azure-devops-%EC%97%90%EC%84%9C-%EA%B6%8C%EC%9E%A5%ED%95%98%EB%8A%94-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EC%A0%84%EB%9E%B5/
[17] https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development
[18] https://www.reddit.com/r/devops/comments/1d7cpz8/tbd_where_do_you_draw_the_line_between_a_long/
[19] https://www.getunleash.io/blog/how-to-implement-trunk-based-development-a-practical-guide
[20] https://trunkbaseddevelopment.com/
