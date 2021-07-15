# Develop

- [Git Workflow: git-flow](#Git-Workflow-git-flow)
  - [Branches](#Branches)
  - [Remotes](#Remotes)
  - [Commit Message Convention](#Commit-Message-Convention)
  - [Squash Merge](#Squash-Merge)
- [Versionings](#Versioning-majorminoretc)
  - [기획된 Renewal Capser Versions](#기획된-Renewal-Capser-Versions)

## Git Workflow: git-flow

git workflow 전략은 git-flow를 채택한다. 그 이유는 향후 다수의 개발자들과 협력하여 개발을 진행할 여지가 있고, 세분화되어 정리된 커밋과 브랜치가 이후에 참여할 개발자들의 전반적인 코드 이해와 추구하고자 하는 방향 이해를 도울 수 있을 것이라 판단하기 때문이다.

### Branches

- main: 서비스될 수 있는 메인 브랜치, 배포 가능한 상태만을 관리
- develop: 다음 출시 버전을 개발하는 브랜치
- feature/<feature>: 기능을 개발하는 브랜치
- release-<version>: 이번 출시 버전을 준비하는 브랜치
- hotfix-<version>: 출시 버전에서 발생한 버그의 긴급 수정용 브랜치

### Remotes

현재 단독 개발 시에는 편의성을 위해 원본 리포지토리에 직접적으로 작업을 수행하지만, 추후 개발에 참여하는 인력이 늘어나는 경우엔 원본 리포지토리에 직접적으로 작업하지 않고, Fork 후 자신의 로컬 리포지토리에서 작업하도록 한다.

### Commit Message Convention

Udacity Git Commit Message Style Guide의 일부를 따른다. 계속해서 세부 사항이 변경될 여지가 있다.

- 메시지 구조

```plain
type: subject

body

footer
```

- Type
  feat: (new feature for the user, not a new feature for build script)
  fix: (bug fix for the user, not a fix to a build script)
  docs: (changes to the documentation)
  style: (formatting, missing semi colons, etc; no production code change)
  refactor: (refactoring production code, eg. renaming a variable)
  test: (adding missing tests, refactoring tests; no production code change)
  chore: (updating grunt tasks etc; no production code change)

- Subject

영문, 명령조의 첫글자 대문자, 50자 이내로 . 를 끝에 붙이지 않는다.

- Body

선택사항으로 기재하며, 커밋에 대해 무엇을 그리고 그러한 이유에 대해 설명하는 내용을 작성한다.

- Footer

Body와 같이 선택사항이며, issue tracker id를 작성할 때 사용한다.

### Squash Merge

병합은 Squash Merge를 기본으로 한다. 커밋을 깔끔하게 관리한 경우 no-ff 머지로 관리하는 것이 좋을 수 있으나 그렇게 관지하지 못할 가능성이 높아, squash merge로 커밋을 깔끔하게 정리하되 필요할 경우 머지 기록에서 머지된 하위 커밋들의 내용을 확인할 수 있도록 한다.

## Versioning: <major>.<minor>.<etc>

버저닝은 다음과 같은 보편적인 규칙을 따른다.  
Version: `<major>.<minor>.<etc>`

- `major` : 호환이 안되는 변경, Framework 변경, 함수 삭제, 이름 변경, 구조 변경 등의 커다란 변경 사항
- `minor` : 호환이 가능한 변경, 기능, 컴포넌트, 클래스, 함수 추가 등 이전의 버전에서 추가되는 변경 사항
- `etc` : 버그 수정, 약간의 디자인 변경 등의 사소한 변동 사항

### 기획된 Renewal Capser Versions

v3.0.0 까지가 공식적으로 진행할 서비스 업그레이드 계획이다.

- v1.0.0: 본격적으로 기존의 홈페이지 기능을 모두 구현하여 홈페이지 이전이 가능한 상태
  v0.1.0 부터 차례로 기본 폼, 계정, 게시판, 로비, sos, rank, 사진첩, 디자인 및 구조 개편, 명예의 전당 등으로 나누어 v0.9.0 정도까지 진행하고 v1.0.0 오픈

- v2.0.0: 새로운 서비스들을 온전하게 통합한 형태로 외부 서비스를 별도로 운영하지 않아도 되는 상태
  v1.1.0부터 차례로 presentations, acitivty, roadmap 으로 v1.3.0 정도까지 진행하고 v2.0.0 오픈

- v3.0.0: 블로그 신규 업데이트
