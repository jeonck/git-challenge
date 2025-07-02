**머지리퀘스트(Merge Request, MR)**가 **직관적으로 느껴지는 이유**는 용어 자체가 실제로 일어나는 동작, 즉 "브랜치를 병합(Merge)해 달라는 요청(Request)"을 명확하게 드러내기 때문입니다.  
다음과 같은 차이점이 있습니다.

| 용어            | 의미와 관점                          | 실제 동작과의 직관성                |
|-----------------|-------------------------------------|-------------------------------------|
| **Pull Request**| "변경사항을 끌어와(Pull) 달라는 요청" | GitHub 등에서 사용하는 용어. 요청자가 아닌 메인 저장소의 입장에서 "내 쪽으로 끌어오겠다"는 의미라 초심자에게는 다소 추상적으로 느껴질 수 있음[2][5]. |
| **Merge Request**| "변경사항을 병합(Merge)해 달라는 요청" | GitLab 등에서 사용하는 용어. 실제로 브랜치를 병합하는 행위와 용어가 일치해 **더 직관적으로 느껴짐**[1][2][6][7]. |

- **Merge Request**는 브랜치를 다른 브랜치로 **병합해 달라는 요청**임을 명확히 드러내고, 실제로 MR을 생성하면 코드 변경 내역, 리뷰, 승인, 병합 등 일련의 과정이 "병합"을 중심으로 진행됩니다[1][6][7].
- **Pull Request**는 "내가 작업한 내용을 메인 저장소가 끌어와 달라"고 요청하는 개념이지만, 실제로는 병합(Merge)이 일어납니다. 용어와 실제 동작 사이에 간극이 있어 헷갈릴 수 있습니다[2][5].

따라서, **"Merge Request"라는 용어가 실제 개발 협업에서 일어나는 과정을 더 명확하고 직관적으로 표현**한다고 느끼는 사람이 많습니다.  
실제로 **GitLab** 등에서는 Merge Request를 공식 용어로 사용하고 있습니다[1][6][7].  
반면 **GitHub** 등에서는 Pull Request가 표준이지만, 두 용어는 기능적으로는 거의 동일합니다[2].

출처
[1] [Gitlab] Merge Request 기능이란? - velog https://velog.io/@leyuri/Gitlab-Merge-Request-%EA%B8%B0%EB%8A%A5%EC%9D%B4%EB%9E%80
[2] [Git]PR(Pull Request)과 MR(Merge Request)의 차이는?? https://youngtoad.tistory.com/47
[3] [Git] 코드 Merge 요청하기/Pull request - 이롭게 현명하게 - 티스토리 https://devyihyun.tistory.com/43
[4] Github를 이용한 협업에 관하여 - part 3. Pull Request부터 코드 리뷰 ... https://velog.io/@2juzzang/Github%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%9C-%ED%98%91%EC%97%85%EC%97%90-%EA%B4%80%ED%95%98%EC%97%AC-part-3.-Pull-Request%EB%B6%80%ED%84%B0-%EC%BD%94%EB%93%9C-%EB%A6%AC%EB%B7%B0-Merge%EA%B9%8C%EC%A7%80
[5] [Github] Github의 Issue와 PR (Pull Request) 알아보기 (PR 병합 후 ... https://devwriter.tistory.com/42
[6] GitLab Merge Request. 내 소스코드도 끼워주세요ㅜ | by Sonny https://techblog.cjenm.com/gitlab-merge-request-89346cfecfa6
[7] Merge Request를 통한 협업 | InfoGrab, DevOps 전문 기술 기업 https://insight.infograb.net/docs/user/merge_request
[8] gitlab에서 소스코드 Pull Request와 Merge 하기 https://www.bearpooh.com/77
[9] [GitLab] Merge 정책 3가지 이해하기 https://iseunghan.tistory.com/330
