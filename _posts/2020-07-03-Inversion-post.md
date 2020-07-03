---
classes: wide
title: "Inversion"
date: 2020-07-03
categories: jekyll update
tags: inversion concept
sidebar:
  nav: "docs"
---

![Image of Inversion](/assets/images/inversion.jpg "Inversion")

[Inversion](https://en.wikipedia.org/wiki/Inversion_(discrete_mathematics), "Wikipedia (Inversion)")은 역위로써, 배열 내 두 원소의 순서가 잘못되었을 때, 두 원소를 나타내는 Index의 쌍  
`Example` 오름차순 기준 : 1 2 2 6 3 5 9 8 -> 역위 : (3, 4) (3, 5) (6, 7)  

`기능` 역위의 개수는 배열 정렬에 필요한 작업량을 나타냄
* `Example 1` 배열의 역위가 존재하지 않을 때, 정렬이 완벽하게 된 것
* `Example 2` 배열의 원소가 역순일 때, 역위의 개수가 최대인 경우 = 1+2+...+(n-1) = n(n-1) / 2 = `O(n²)`

---

<a href="https://changpulmu.github.io/jekyll/update/Comparison-Operator-post/" class="btn btn--inverse btn--large">Next</a>{: .align-right}
