---
classes: wide
title: "bit Operation"
date: 2020-07-02
categories: jekyll update
tags: bit_operation concept
sidebar:
  nav: "docs"
---

![Image of bit Operation](/assets/images/bit_operation.jpg "bit Operation")

[ [bit Operation](https://en.wikipedia.org/wiki/Bitwise_operation, "Wikipedia (bit Operation)") ]
{: .text-center}    

`특징` n비트 정수를 대상으로 하는 연산  

* `x & y` AND
* `x | y` OR
* `x ^ y` XOR
* `~x [-x - 1]` NOT
* `x << k [x * 2^k]` / `X >> k (x / 2^k 후 정수로 내림)` SHIFT

***

## bit Mask
`개념` 1 << k (k번째 위치에만 bit 1이 있고, 나머지 위치에 bit 0이 있는 정수)  
`활용도1` int형 정수 x의 bit 표현을 출력 가능함  
`활용도2` int형 정수의 특정한 bit 하나를 수정할 수 있음  
`특징` long long형 Bit Mask는 1LL << k  

* `x | ~(1<<k)` 정수 x의 k번째 비트를 1로 바꿈
* `x & ~(1<<k)` 정수 x의 k번째 비트를 0으로 바꿈
* `x ^ (1<<k)` 정수 x의 k번째 비트를 뒤집음
* `x & (x-1)` 정수 x의 가장 오른쪽 비트 1을 0으로 바꿈
* `x & -x` 정수 x의 모든 비트를 0으로 바꾸고, 비트 1 중에서 제일 오른쪽 것만 하나 남김
* `x | (x-1)` 정수 x의 마지막 비트 1 다음에 나오는 모든 비트를 뒤집음
* `x & (x-1) = 0` x는 2의 거듭제곱

***

### g++ 컴파일러 지원 함수
* `__builtin_clz(x)` 비트 표현의 왼쪽에 연속해서 있는 비트 0 개수
* `__builtin_ctz(x)` 비트 표현의 오른쪽에 연속해서 있는 비트 0 개수
* `__builtin_popcount(x)` 비트 표현에서 비트 1의 개수
* `__builtin_parity(x)` 비트 표현에서 비트 1의 개수에 대한 Parity (짝/홀수)

***

## 집합 표현
`개념` 집합 {0, 1, 2, ..., n-1}의 모든 부분집합을 n비트 정수를 이용하여 표현  

* `a & b` 교집합 a ∩ b
* `a | b` 합집합 a ∪ b
* `a & (~b)` 차집합 a ＼ b
* `~a` 여집합

***

* 모든 부분집합을 차례로 살펴보는 코드

```
[First Method]

for (int a=0; a<(1<<n); a++)
{
  Code for examing subgroups
}

[Second Method]

int b=0;

do
{
  Code for examing subgroups
} while (b = (b - x) & x);
```   

* 부분집합 중에서 원소의 개수가 정확히 k개인 것만 살펴봄

```
for (int a=0; a<(1<<n); a++)
{
  if(__builtin_popcount(b) == k)
  {
    Code for examing subgroups
  }
}
```

***

`C++ 표준 라이브러리` [bitset](https://changpulmu.github.io/jekyll/update/bitset-post/, "bitset")
***
<a href="https://changpulmu.github.io/jekyll/update/Recursion-Algorithm-post/" class="btn btn--inverse btn--large">Previous</a>
<a href="https://changpulmu.github.io/jekyll/update/Brute-Force-Algorithm-post/" class="btn btn--inverse btn--large">Next</a>{: .align-right}
