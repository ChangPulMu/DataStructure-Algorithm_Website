---
classes: wide
title: "Recursion Algorithm"
date: 2020-07-02
categories: jekyll update
tags: recursion_algorithm concept
sidebar:
  nav: "docs"
---

![Image of Recursion Algorithm](/assets/images/recursion_algorithm.jpg "Recursion Algorithm")

[ [Recursion Algorithm](https://en.wikipedia.org/wiki/Recursion_(computer_science), "Wikipedia (Recursion Algorithm)") ]
{: .text-center}    
***
### Generate Subset Problem

재귀 함수 형식으로 vector에 push_back(포함) / pop_back(제외)을 반복하여 구하기

***
### Generate Permutation Problem

부분집합 생성 방법 + 순열 포함여부 나타내는 bool 배열로 확인

C++ 표준 라이브러리의 next_permutation(v.begin(), end()) do~while문의 조건식으로 넣기

***
## Backtracking
```
비어있는 해로 탐색을 시작 -> 단계마다 해를 확장해나감
```

해를 생성하는 모든 방법을 재귀적으로 하나하나 살펴보게 됨

### N Queen Problem


<a href="https://changpulmu.github.io/jekyll/update/Algorithm-post/" class="btn btn--inverse btn--large">Previous</a>
<a href="https://changpulmu.github.io/jekyll/update/Recursion-Algorithm-post/" class="btn btn--inverse btn--large">Next</a>{: .align-right}
