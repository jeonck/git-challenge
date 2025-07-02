**플리퀘스트(Pull Request)의 원어적 의미와 구분**

플리퀘스트(Pull Request, 줄여서 PR)는 소프트웨어 개발 협업 도구인 Git 및 GitHub, Bitbucket 등에서 사용되는 용어로, 그 원어적 의미와 기능적 구분은 다음과 같습니다.

### 1. 원어적 의미

- **Pull**: 영어로 "끌어오다", "당기다"라는 뜻입니다.
- **Request**: "요청"이라는 뜻입니다.
- **Pull Request**: 직역하면 "끌어오기 요청" 또는 "당겨오기 요청"입니다.  
  즉, **다른 저장소(혹은 브랜치)의 변경사항을 내 저장소(혹은 브랜치)로 '끌어와 달라'고 요청하는 행위**를 의미합니다[1][2].

### 2. 실질적 사용과 구분

| 용어           | 원어적 의미            | 실제 사용 맥락 및 역할                                                                                      |
|----------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| **Fork**       | "포크"= "갈라지다"     | 다른 사람의 저장소를 내 계정으로 복사(분기)하여 독립적으로 개발할 수 있게 함[3][4][5].                      |
| **Branch**     | "가지"                 | 저장소 내에서 독립적으로 작업할 수 있는 별도의 작업 공간을 만듦[4][5].                                      |
| **Pull Request** | "끌어오기 요청"        | 내(혹은 포크한) 저장소/브랜치에서 작업한 내용을 원본 저장소/브랜치로 병합해 달라고 요청하는 공식적인 절차[3][1][2][4][5][6]. |

#### 플리퀘스트의 구조적 구분
- **소스(Source) 저장소/브랜치**: 변경사항을 만든 쪽(요청자).
- **대상(Target) 저장소/브랜치**: 변경사항을 받아줄 쪽(관리자 또는 원본)[1].
- **요청(Request)**: 소스의 변경 내용을 대상에 병합(merge)해 달라는 공식적 제안.

#### 절차적 구분
1. **Fork**: 원본 저장소를 내 계정으로 복사(필요시).
2. **Branch 생성**: 내 저장소에서 새로운 작업 브랜치 생성.
3. **작업/커밋**: 브랜치에서 코드 수정 및 커밋.
4. **Push**: 내 저장소(혹은 포크된 저장소)에 변경사항 업로드.
5. **Pull Request 생성**: 원본 저장소(혹은 메인 브랜치)에 변경사항 병합을 요청[3][1][4][5][6].
6. **코드 리뷰 및 Merge**: 관리자가 변경사항을 검토 후 병합 여부 결정[1][6].

### 3. 요약

- **플리퀘스트(Pull Request)**는 영어 원어적 의미 그대로 "변경사항을 당겨와 달라는 요청"입니다.
- **실제 개발 협업에서는** 자신의 작업(포크/브랜치)을 원본 저장소에 반영해달라고 공식적으로 요청하는 절차를 의미합니다.
- **구조적으로는** 소스와 대상, 요청의 세 가지 요소로 구분할 수 있습니다[1].

> ‘풀리퀘’는 깃허브에서 타인의 코드에 리뷰를 요청하는 기능인 ‘풀 리퀘스트’의 줄임말입니다. 풀리퀘를 통해 코드는 더 발전합니다[2].

이처럼 플리퀘스트는 단순한 "끌어오기"가 아니라, **공식적인 변경 요청과 코드 리뷰, 협업의 핵심 도구**로 사용됩니다.

출처
[1] 풀 리퀘스트 | Atlassian Git Tutorial https://www.atlassian.com/ko/git/tutorials/making-a-pull-request
[2] [함께 쓰는 풀리퀘]“뭐 먹을래? 난 간짜장 곱빼기” AI로 번역해보니 https://www.bloter.net/news/articleView.html?idxno=43172
[3] git 초보를 위한 풀리퀘스트(pull request) 방법 https://wayhome25.github.io/git/2017/07/08/git-first-pull-request-story/
[4] 깃허브 브랜치(branch) & 포크(fork) & 풀리퀘스트(pull ... - 읽고 쓰기 https://youtaek123.tistory.com/38
[5] 2020.09.26_git pull request - 코린이의 정리노트 - 티스토리 https://korinkorin.tistory.com/30
[6] [Github/Git] 깃허브 PR이란? ,PR 하는법 , (풀리퀘스트, PullRequest) https://raon-2.tistory.com/46
[7] Pull Request 이해하기 - velog https://velog.io/@zansol/Pull-Request-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0
[8] 풀리퀘스트(Pull Requests) 그렇게 만들면 안되는데... - YouTube https://www.youtube.com/watch?v=VCqTCvwLVPk
[9] GitHub에서 Fork와 Pull Request 완벽 이해하기 | 포크 , 풀리 ... https://daddydontsleep.tistory.com/140
[10] github.com - Pull request - 1. 수업소개 - YouTube https://www.youtube.com/watch?v=uvsz2XgRPfM
