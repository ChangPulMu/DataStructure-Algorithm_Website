---
classes: wide
title: "Search Algorithm"
date: 2020-07-03
categories: jekyll update
tags: search_algorithm concept
sidebar:
  nav: "docs"
---

![Image of Search Algorithm](/assets/images/search_algorithm.jpg "Search Algorithm")

[ [Serach Algorithm](https://en.wikipedia.org/wiki/Search_algorithm, "Wikipedia (Search Algorithm)") ]
{: .text-center}

---

### Binary Search `O(logn)`
`설명` 정렬된 배열에 특정 원소 존재 여부를 확인  
`Answer 1` 재귀적으로 배열의 탐색 범위를 절반으로 줄여가며 중앙의 원소를 검사함  
`Answer 2` 배열을 왼->오른쪽으로 n/2^k개(~1개)의 원소를 건너뛰며 해당 위치 원소를 검사함  

---

#### Finding Optimal Value (최적해 구하기)
`전제` valid(x)라는 함수는 x가 올바른 해면 true / 아니면 false 반환  
`조건` x<k일 때 valid(x)는 false & x>=k일 때 valid(x)는 true임을 알고 있는 상태  
`Idea` valid(x)가 false인 x의 최댓값을 이진 탐색으로 구함 (k = x+1일 때, valid(k)는 true인 최솟값)  
∴ valid()를 `O(logn)`만큼 호출함으로 전체 수행시간은 `O(logn * valid() 수행시간)`

---

`Question` 모든 작업을 처리하는데 드는 시간의 최솟값 (기계 n대를 이용해 k개의 작업을 처리)  
* `전제 1` i번 기계에 할당된 pi라는 값은 1개의 작업을 처리하는데 드는 시간  
* `전제 2` valid(x)는 x만큼의 시간 안에 모든 작업을 처리할 수 있는지를 판별하는 함수  
`Answer` valid(x) : i번 기계로 x만큼의 시간 안에 처리할 수 있는 작업의 최대 개수가 ⌞x/pi⌟임으로  
  `So` 모든 i에 대해 ⌞x/pi⌟를 합한 값이 k이상이라면 x는 올바른 해임  
    `Then` Binary Search를 이용하여 valid(x)가 true인 x의 최솟값을 구할 수 있게 됨  

∴ valid() 수행시간은 `O(n)`임으로 `O(nlog(k * [가장 짧은 시간에 하나의 작업을 수행하는 처리시간]))`

---

<a href="https://changpulmu.github.io/jekyll/update/Sort-Algorithm-post/" class="btn btn--inverse btn--large">Previous</a>
<a href="https://changpulmu.github.io/jekyll/update/Greedy-Strategy-post/" class="btn btn--inverse btn--large">Next</a>{: .align-right}
