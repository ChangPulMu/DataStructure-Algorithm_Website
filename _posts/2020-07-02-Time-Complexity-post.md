---
classes: wide
title: "Time Complexity"
date: 2020-07-01
categories: jekyll update
tags: time_complexity concept
sidebar:
  nav: "docs"
---

![Image of Time Complexity](/assets/images/time_complexity.jpg "Time Complexity")

[ [Time Complexity](https://en.wikipedia.org/wiki/Time_complexity, "Wikipedia (Time Complexity)") ]
{: .text-center}    

* Polynomial Algorithm (다항시간 알고리즘)

  + `O(1)` [Constant-time] : 수행 시간은 입력의 크기에 영향을 받지 않음  
    ex) 공식을 이용해 계산

  + `O(logn)` [Logarithmic] : 단계마다 입력의 크기를 절반씩 줄여나감

  + `O(root n)` [Square Root] : n개 원소를 각 O(root n)개씩의 원소로 이뤄진 그룹 O(root n)개로 나눌 수 있음

  + `O(n)` [Linear] : 입력을 1번씩 쭉 살펴보는 과정을 상수 번 수행함

  + `O(nlogn)` : 효율적인 정렬 알고리즘의 시간 복잡도

  + `O(n²)` [Quadratic] : 2중으로 중첩된 반복문  
    ex) 입력 원소 2개로 만들 수 있는 모든 조합

  + `O(n³)` [Cubic] : 3중으로 중첩된 반복문  
    ex) 입력 원소 3개로 만들 수 있는 모든 조합    

* NP-hard Problem

  + `O(2^n)`  
    ex) 입력 원소로 만들 수 있는 모든 부분집합을 1번씩 살펴봄

  + `O(n!)`  
    ex) 입력 원소로 만들 수 있는 모든 순열을 1번씩 살펴봄    


입력의 크기 (시간제한 1초일 때) | 추정 시간복잡도
--- | ---
n <= 10 | `O(n!)`
n <= 20 | `O(2^n)`
n <= 500 | `O(n³)`
n <= 5000 | `O(n²)`
n <= 10^6 | `O(nlogn)` / `O(n)`
n이 클 때 | `O(1)` / `O(logn)`


<a href="https://changpulmu.github.io/jekyll/update/Algorithm-post/" class="btn btn--inverse btn--large">Previous</a>
<a href="https://changpulmu.github.io/jekyll/update/Recursion-Algorithm-post/" class="btn btn--inverse btn--large">Next</a>{: .align-right}
