---
title: "Binary Search"
date: 2013-03-01 08:26:28 -0400
categories: algo
---
---

> Binary Search(이진 탐색)

### 개념
```
Divide and Conquer의 대표 예
반복문을 통해 탐색시 >> 시간복잡도 : O(N)
이진 탐색을 통해 O(logN)로 약간 단축 가능(단, 리스트가 정렬이 된 상태에서만 가능)

1. 배열의 중간을 먼저 탐색한다.
2. 중간값이 탐색값이면 중단.
3. 중간값이 탐색값이 아니라면 중간값과 탐색값의 크기를 비교한다.
4. 중간값 > 탐색값 - 중간값의 오른쪽 인덱스들은 제외
5. 중간값 < 탐색값 - 중간값의 왼쪽 인덱스들은 제외

** 문제의 정답이 최소값 or 최대값에 따라 return 하는 결과 값이 다름
java에서는 이진탐색이 이미 구현되어있음 ex) 2776 구현
>> Arrays.binarySearch(array, target);
EX)2776, 1920, 2805, 2512, 2343, 6236, 1654, 2110, 16434, 15732, 1300
```

### CODE
```java
class Main {
	public static void main(String[] args) throws Exception {
		int[] arr = { 8, 6, 5, 3, 4, 11, 2, 4, 15, 7, 31 };
		Arrays.sort(arr);
		System.out.println(binarySearch(arr, 7));
	}

	static int binarySearch(int[] arr, int target) {
		int start = 0, mid = 0;
		int end = arr.length - 1;
		while (start <= end) {
			mid = (start + end) / 2;
			if (target == arr[mid])
				break;
			else {
				if (target < arr[mid])
					end = mid - 1;
				else
					start = mid + 1;
			}
		}
		return mid;
	}
}
```

### COMMENT
* Divide and Conquer
