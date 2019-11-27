---
title: "Selection Sort"
date: 2013-03-01 08:26:28 -0400
categories: algo
---
---

> Selection Sort(선택 정렬)

###개념
```
현재 위치보다 우측 위치의 모든 수를 비교하여 가장 작은 숫자를 현재 위치에 선택하는 알고리즘
시간복잡도 : O(N^2)
공간복잡도 : O(N)
```

### CODE
```java
public void selectionSort(int[] ary) {
	int size = ary.length;
	for (int i = 0; i < size - 1; i++) {
		int min_idx = i;
		for (int j = i + 1; j < size; j++)
			if (ary[min_idx] > ary[j])
				min_idx = j;
		if (min_idx == i)
			continue;
		int temp = ary[min_idx];
		ary[min_idx] = ary[i];
		ary[i] = temp;
	}
}
```

### COMMENT
