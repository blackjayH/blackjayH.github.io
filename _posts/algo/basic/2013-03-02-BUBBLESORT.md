---
title: "Bubble Sort"
date: 2013-03-01 08:26:28 -0400
categories: algo
---
---

> Bubble Sort(버블 정렬)

### CODE

```java
public void bubbleSort(int[] ary) {
	int size = ary.length;
	for (int i = 0; i < size - 1; i++) {
		for (int j = 1; j < size - i; j++) {
			if (ary[j - 1] > ary[j]) {
				int temp = ary[j];
				ary[j] = ary[j - 1];
				ary[j - 1] = temp;
			}
		}
	}
}
```
### COMMENT
