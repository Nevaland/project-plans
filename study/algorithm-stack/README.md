# Alogithm Stack

본 기획안의 스터디는 아래의 리포지토리로 운영 중<sup>(2021)</sup>이며, 본 기획안과 일치 시켜 운영하려는 목적이 아닌 해당 기획의 문서 정리 목적입니다.  
https://github.com/CASPER-REPSAC/algorithm-stack

## 프로젝트 개요

### 기획 대상

동아리 내의 알고리즘, 자료구조, 코딩 테스트 스터디 활동 및 기록을 위한 리포지토리

### 기획 배경과 목적

코딩 문제 풀이를 공유하고 서로 코드 리뷰를 더 편히 해줄 수 리포지토리를 기획하였다.

1. 자율성  
   누구나 편하게 언제든 스터디에 참여할 수 있는 분위기를 조성하고, 선 후배 간의 구별 없는 코드 리뷰로 적극적인 정보 공유와 교류를 유도한다.

2. 강제성  
   주마다 문제가 선정되어 스터디에 공식적으로 참여하는 이는 이를 함께 풀어봄으로써 서로의 풀이가 공유되고, 코드 리뷰의 접근성이 높아진다.

### 기대 효과

주기적으로 알고리즘 문제 풀이와 코드 리뷰를 통해 개발 능력을 함양하고, 쌓여가는 코드들과 코드 리뷰들로 다양한 풀이와 생각을 더욱더 손쉽게 접할 수 있게 될 것이다.

## 프로젝트 내용

### 1. README 와 링크를 이용한, 보다 보기 쉬운 구조

스터디 날짜 기준이 아닌 문제 문항 기준의 디렉터리 구조를 사용해, 해당 폴더가 이후에도 계속 재사용되어, 한번 작성된 풀이가 계속해서 사용자들에게 노출되고, 이용될 수 있도록 구상하였다.

```
algorithm-stack (Repository)
├── README.md (1)
│
└── 문제 분류 ex)boj, programmers,,
    ├── README.md (2)
    │
    └── 문제 ex)1000, 1001,,
        ├── README.md (3)
        ├── solved.md
        │
        └── 닉네임 ex)neva,,
            └── 코드 파일 ex)1000.py
```

- **README.md** (1) <sup>[algorithm-stack (Repository)] </sup>  
  Algorithm Study를 총괄하는 메인 리드미로 리포지토리 설명, 주간 문제, 기타 문제가 나열되어 있다.  
  각 문제는 해당 문제 폴더로 링크가 연결되어 있고, 이때 주간 문제 문항은 유일성을 가지지 않는다.  
  (주간 문제는 같은 문제가 중복해 등장할 수 있다.)

  <details>  
    <summary>주간 문제가 해를 거듭함에 따라 사이즈가 커져 분리하고자 하는 경우</summary>  
    <sup>리드미 내용을 해 별로 분리해 현재 해당 년도의 내용만을 리드미 파일에 담고 외의 년도의 내용은 README(20~21).md 등의 형태로 분리시킨다.</sup>
  </details>
  <details>
    <summary>만약 스터디가 분리되어 운영돼 리드미를 변경하고자 하는 경우</summary>
    <sup>해당 스터디 별로 현 위치에 폴더를 생성해 그 곳에 리드미를 생성 후 이 리드미의 내용을 담고 이 리드미의 내용은 운영된(되는) 스터디의 기간과 해당 폴더 링크 만을 담도록 변경한다.</sup>
  </details>

- **README.md** (2) <sup>[문제 분류 ex)boj, programmers,,]</sup>  
  문제 분류로 나뉜 폴더의 리드미로 예를 들어 BOJ(백준) 폴더가 있고 그의 리드미라고 생각할 수 있다.  
  문제 링크들만 나열되어있다. 문제는 이름 명을 기준으로 정렬되어있다.

- **README.md** (3) <sup>[문제 ex)1000, 1001,,]</sup>  
  해당 문제에 대한 리드미로 문제의 내용만이 작성되어있다.

- **solved.md**  
  문제별 언어별 풀이 파일들의 링크를 한 곳에 모아 정리한 파일로 자신이 보고자 하는 언어로 작성된 문제 풀이를 쉽게 찾아 볼 수 있도록 해준다.

- [+] 추가 의견 README.md (4) <sup>[닉네임 ex)neva,,]</sup>  
  각자 자신의 풀이 코드들이 담긴 폴더의 리드미로 문제 제출 결과에 대한 정보를 담아놓을 수 있다.

### 2. 운영 방식

#### 1. 주간 문제

주마다 문제가 선정된다.  
스터디 참가자는 해당 주차 내에 풀되 풀어내지 못하더라도 코드를 작성해 제출한다.  
또한 참가자가 아니더라도 자유롭게 주간 문제 풀이에 참여할 수 있고 과거에 올라온 주간 문제는 기간에 무관하게 풀면 된다.

#### 2. 개발 및 반영 방식

개발은 각자 자신의 닉네임으로 브랜치를 생성해 작업하고 개발이 완료되면 main 브랜치로 `Pull Request`를 요청한다.  
그 후 특정 기간 (ex. 1주일), 특정 조건 (ex. Approve) 이 완료되면 `Squash Merge`로 main 브랜치에 병합하고 자신의 브랜치는 개발이 더 진행되지 않을 경우 제거한다.
<sup>`Squash Merge` 를 사용하는 이유는 커밋 히스토리를 보다 깔끔하게 유지하기 위함이다.</sup>

  <details>
    <summary>리포지토리의 전체 사이즈가 너무 커진 경우</summary>
    <sup>sparseCheckout 기능을 활용하여 특정 폴더만 복제해 작업한다.</sup>
  </details>

#### 3. 코드 리뷰

코드 리뷰는 작성된 PR(Pull Request)에서 언급하고자 하는 코드와 함께 코멘트를 작성해 리뷰하며, 이미 닫힌 PR에 대해서도 언제든 코드 리뷰를 남겨줄 수 있다. <sub>단, 닫힌 과거의 PR에 대해서는 당사자가 리뷰를 요청했거나 현재 진행 중인 스터디의 과거 PR인 경우에만 코드 리뷰를 남기도록 한다.</sub>

코드 리뷰 내용은 대상에 따라 상이하나 알고리즘 문제의 경우 `설계`, `기능`, `복잡성`, `작명`, `주석` 등의 사항을 검토해 리뷰한다. <sup>스타일은 스타일 가이드를 스터디에서 정한 경우 포매터 등의 툴로 각자 맞추고, 스타일에 대해서는 크게 형태가 무너지거나 통일성이 깨지지 않는 한 리뷰 하지 않는다.</sup>

또한 좋은 부분을 발견할 경우에도 이를 리뷰로 언급할 수 있고, 리뷰는 친절하고 논증을 기반하여야 한다.  
<sup>
(멘토링 측면에서 개발자에게 잘못된 것을 말하는 것보다 그들이 무엇을 잘했는지를 말하는 것이 훨씬 더 가치 있다)
</sup>

받은 코드 리뷰를 항상 따를 필요는 없으며 코드 리뷰 내용에 대해 깊게 토론할 수 있고, 그다지 중요치 않은 선호도에 가까운 개선점의 경우 `Nit:` 과 같은 접두어를 붙여 코드 작성자에게 이를 밝혀야 한다.

- "리뷰어"  
  코드 리뷰는 언제든 누구나 유동적으로 수행하나, 여건에 따라 추가로 리뷰어를 특정하여 코드 작성자들에게 보다 질 좋은 코드 리뷰를 제공할 수 있도록 운영한다.

#### 4. 봇

문제 선정 및 문제 폴더 생성, 문제 설명이 담긴 리드미 파일 생성, 링크 작성, solved 파일 작성 등의 작업은 봇으로 작업시키도록 한다.