---
classes: wide
title: "Sort Algorithm"
date: 2020-07-02
categories: jekyll update
tags: sort_algorithm concept
sidebar:
  nav: "docs"
---

![Image of Sort Algorithm](/assets/images/sort_algorithm.jpg "Sort Algorithm")

[ [Sort Algorithm](https://en.wikipedia.org/wiki/Sorting_algorithm, "Wikipedia (Sort Algorithm)") ]
{: .text-center}

---

### Bubble Sort `O(n²)`
`흐름` n번의 라운드로 이루어져있으며, 라운드마다 배열의 원소를 1번씩 쭉 살펴봄  
+ `if` 연달아 있는 원소 2개의 순서가 잘못되어 있으면 [ [역위](https://changpulmu.github.io/jekyll/update/Inversion-post/) ]  
+  `then` 두 원소를 맞바꿈  
  * `결과` 1번째 라운드가 끝나면 내림/오름차순에 따라 가장 작은/큰 원소가 올바른 위치(맨 끝)에 놓임  
∴ n번의 라운드가 끝나면, 배열 전체가 정렬됨

---

### Merge Sort `O(nlogn)`
`특징` 재귀 호출의 단계(부분배열을 절반으로 줄여나가기)가 O(logn) x 각 단계를 처리할 때 O(n)  
`흐름` 재귀를 이용하여 부분배열 array[a...b]를 아래 순서에 따라 정렬  
+ `if` a==b `then` 정렬 x (부분배열이 원소 1개로 구성되어 있으며, 이는 이미 정렬되어 있음)  
  * `Step 1` 가운데 원소의 위치 k = ⌞(a+b)/2⌟
  * `Step 2` 재귀적으로 부분배열 array[a...k]와 array[k+1...b]를 정렬
  * `Step 3` 정렬된 부분배열 array[a...k]와 array[k+1...b]를 병합하여 정렬된 부분배열 array[a...b]을 생성

---

♂ 배열의 원소를 비교하는데 기반을 둔 정렬 알고리즘의 경우는 Ω(nlogn) ♂

---

### Counting Sort `O(n)`
`의미` 배열의 원소를 직접 비교하지 않고, 다른 정보를 이용함  
`특징` 원래 배열의 원소를 장부배열의 인덱스로 사용할 수 있을 만큼 c가 작을 때만 사용 가능  
`기준` 배열의 모든 원소가 0...c 범위 정수이며, c = O(n)이고, 장부배열의 Index는 원래 배열의 원소들
  * `Step 1` 원래 배열을 1번 살펴보면서, 각각의 원소가 배열에 몇 개 들어있는지 계산
  * `Stpe 2` 각각의 원소가 배열에 들어있는 개수는 장부배열의 각 원소 Index가 가지는 내부 값이 됨  
∴ 장부배열 만드는데 O(n) & 정렬된 배열을 만드는데 O(n) = 전체 시간복잡도 O(n)

---

### C++ Sort Function
`기능` 리스트/벡터 등의 자료구조 내 원소(숫자/문자...)를 오름차순으로 정렬함  
`조건` 정렬할 원소의 자료형에 대해 [비교연산자](https://changpulmu.github.io/jekyll/update/Comparison-Operator-post)가 정의되어 있어야 함  
`특징` 외부에서 정의된 Comparison Function(비교함수)를 Call-back 함수 형태로 줄 수 있음
```
sort(v.begin(), v.end());
sort(a, a+n);
sort(v.rbegin(), v.rend());
sort(v.begin(), v.end(), comp);
```

---

### Sweep Line Algorithm
`개념` 정렬된 순서대로 처리되는 이벤트의 집합으로 문제를 모델링하는 방법
* 음식점 동시 최대 손님 수 최댓값  
  `조건` 모든 손님이 언제 방문/떠났는지에 대한 정보를 모두 알 때  
    + `Step 1` 손님마다 방문/떠남이라는 이벤트 2개를 만들고 모든 이벤트를 시간 순으로 정렬해 차례로 살핌  
    + `Step 2` Counter 변수를 하나 만들어서, 손님이 방문하면 증가 / 떠나면 감소  
    + `Step 3` 답은 Counter의 최댓값  
  ∴ 이벤트 정렬 `O(nlogn)` & Sweep Line과 관련된 살피는 부분   `O(n)`  
  = 전체 시간복잡도 `O(nlogn)`

---

<a href="https://changpulmu.github.io/jekyll/update/Brute-Force-Algorithm-post/" class="btn btn--inverse btn--large">Previous</a>
<a href="https://changpulmu.github.io/jekyll/update/Search-Algorithm-post/" class="btn btn--inverse btn--large">Next</a>{: .align-right}
