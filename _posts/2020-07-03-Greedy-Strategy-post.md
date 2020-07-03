---
classes: wide
title: "Greedy Strategy"
date: 2020-07-03
categories: jekyll update
tags: greedy_strategy concept
sidebar:
  nav: "docs"
---

![Image of Greedy Strategy](/assets/images/greedy_strategy.jpg "Greedy Strategy")

[Greedy Strategy](https://en.wikipedia.org/wiki/Greedy_algorithm, "Wikipedia (Greedy Algorithm)")는 탐욕법 기반의 전략으로써, 현재 상황에서 최선으로 보이는 선택을 하며, 1번 선택한 것은 되돌리지 않음

---

### Event Scheduling Problem
`Question` 대한 많은 수의 이벤트를 포함하는 스케줄 (이벤트 n개의 시작/종료시각이 주어졌을 때)  
* `Case 1` 이 순으로 이벤트 정렬 : 최대한 짧은 이벤트부터 차례로 선택 -> 반례 존재
* `Case 2` 시작시각 순으로 이벤트 정렬 : 가장먼저 시작하는 것을 차례로 선택 -> 반례 존재
* `Case 3 - Answer` 종료시각 순으로 이벤트 정렬 : 가장먼저 종료하는 것을 차례로 선택

∴ 항상 최적의 해

---

### Work & Deadline Problem
`Question` 작업 n개의 소요시간/데드라인 주어질 때, 작업의 순서를 정해서 최대 점수 구하기  
`조건` 각 작업에 대한 점수 : `d-x` (데드라인 – 작업완료 시각)  
`Answer` 최적의 해는 Deadline에 전혀 영향을 받지 않음 & 소요시간이 짧은 작업부터 작업 수행

---

<a href="https://changpulmu.github.io/jekyll/update/Search-Algorithm-post/" class="btn btn--inverse btn--large">Previous</a>
