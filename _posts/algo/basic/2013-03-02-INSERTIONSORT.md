---
title: "Insertion Sort"
date: 2013-03-01 08:26:28 -0400
categories: algo
---
---

> Insertion Sort(삽입 정렬)

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
