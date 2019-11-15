---
title: "Selection Sort"
date: 2013-03-01 08:26:28 -0400
categories: algo
---
---

> Selection Sort(선택 정렬)

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
