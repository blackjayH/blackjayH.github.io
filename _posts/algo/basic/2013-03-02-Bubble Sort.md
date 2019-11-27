---
title: "Bubble Sort"
date: 2013-03-01 08:26:28 -0400
categories: algo
---
---

> Bubble Sort(버블 정렬)

### 개념
```
이웃하는 두 수를 비교하여 큰 수를 뒤로 보내주는 정렬. 그 결과 1회전 후 가장 큰 값이 맨 뒤로 이동
시간복잡도 : O(N^2)
공간복잡도 : O(N)
```

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
