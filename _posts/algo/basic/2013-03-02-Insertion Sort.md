---
title: "Insertion Sort"
date: 2013-03-01 08:26:28 -0400
categories: algo
---
---

> Insertion Sort(삽입 정렬)

###개념
```
현재 위치보다 좌측 위치의 모든 수를 비교하여 들어갈 위치에 삽입하는 알고리즘
시간복잡도 : O(N^2)
공간복잡도 : O(N)
```

### CODE
```java
public void insertionSort(int[] ary) {
	int size = ary.length;
	for (int i = 1; i < size; i++) {
	int currentValue = ary[i];
	int position = i;
	while (position > 0 && ary[position - 1] > currentValue) {
		ary[position] = ary[position - 1];
		position--;
		}
		ary[position] = currentValue;
	}
}
```

### COMMENT
