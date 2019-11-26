---
title: "Sieve of Eratosthenes"
date: 2013-03-01 08:26:28 -0400
categories: algo
---
---

> Sieve of Eratosthenes(에라토스테네스의 체)

### 개념
```
가장 보편적인 방법으로 소수를 구하게되면 O(N^2)이다.
이보다 빠른 방법인 에라토스테네스의 체를 사용하면 시간복잡도는 O(logN)로 줄일 수 있다.
효율적인 소수 구하기의 간단히 방법을 설명하면, 소수의 배수를 제거하는 방식이다.
예를 들어, 11^2 > 120 이므로 11보다 작은 수의 배수들만 지워도 충분하다.
즉, 120보다 작거나 같은 수 가운데 2, 3, 5, 7의 배수를 지우고 남는 수는 모두 소수이다.
```

### CODE
```java
int rootSqrt = (int) Math.sqrt(n);
for(int i = 2;i <= rootSqrt; i++) {
    if (array[i])
        continue;
    for(int j = i + i; j <= 1000000; j+=i)
        array[j] = true;
}
```

### COMMENT
* 1 예외처리 필수
* 원리 문제 [GO 2960]

[GO 2960]: https://www.acmicpc.net/problem/2960
