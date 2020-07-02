---
classes: wide
title: "Brute-Force Algorithm"
date: 2020-07-02
categories: jekyll update
tags: brute_force_algorithm concept
sidebar:
  nav: "docs"
---

![Image of Brute-Force Algorithm](/assets/images/brute_force_algorithm.jpg "Brute-Force Algorithm")

[ [Brute-Force Algorithm](https://en.wikipedia.org/wiki/Brute-force_search, "Wikipedia (Brute-Force Algorithm)") ]
{: .text-center}

---

### 최대 부분배열 합
`문제` 배열에서 연속해 있는 값들 중 그 합이 최대인 경우  

`O(n³)` 직관적인 방법으로 가능한 모든 부분배열을 하나씩 살펴봄 (3중 반복문)  
`O(n²)` 부분배열의 오른쪽 끝을 이동해 가면서 그 합도 같이 계산 (2중 반복문)  
`O(n)` 배열의 각 위치에 대해, 그 위치에서 끝나면서 합이 최대인 부분배열 계산 (반복문)  
  * 위치 k에서 끝나면서 부분배열이 최대인 경우  
    `Case 1` 부분배열이 위치 k의 원소 하나만으로 이뤄진 경우  
    `Case 2` 위치 k-1에서 끝나는 부분배열 + 위치 k의 원소  

---

### 두 Queen 문제
`문제` nxn 체스판 내 퀸 2개를 서로 공격할 수 없도록 배치하는 방법의 수

`O(n⁴)` 모든 경우를 살펴봄 (1번째 퀸 위치 정하는 경우 n² x 2번째 퀸이 놓일 수 있는 위치 n²-1)  
`O(n²)` 1번째 퀸으로 인해 가로/세로 n-1개 양쪽 대각선 d-1개 공격 가능으로 2번째 퀸 O(1)  
`O(n)` 점화식 q(n)로 재귀적 풀이를 함  
  * `q(n-1)` 마지막 행/열에 퀸을 배치하지 않을 때 가능한 경우의 수
  * `2n-1` 마지막 행/열에 퀸을 배치할 수 있는 칸의 개수
  * `n²-3(n-1)-1` 2번째 퀸 배치가능한 칸 개수 / 3(n-1)은 1번째 퀸이 공격 가능한 칸 (행/열/대각선)
  * `(n-1)(n-2)` 마지막 행과 열에 퀸 2개를 배치하는 방법의 수 (2&3에서 2번씩 계산했음으로 빼야함)
```
∴ q(n) = q(n-1) + (2n-1)(n²-3(n-1)-1) - (n-1)(n-2)
```

`O(1)` 닫힌 형태의 공식 (Closed-form Formula)

---

<a href="https://changpulmu.github.io/jekyll/update/bit-Operation-post/" class="btn btn--inverse btn--large">Previous</a>
<a href="https://changpulmu.github.io/jekyll/update/Sort-Algorithm-post/" class="btn btn--inverse btn--large">Next</a>{: .align-right}
