## 삽입정렬(insertionSort)
- 삽입정렬은 전체 배열 중 정렬되어 있는 부분배열에 새 원소를 끼워넣는 일을 반복하는 방식으로 동작함
- 두 번째 자료부터 시작하여 그 앞(왼쪽)의 자료들과 비교하여 정렬한다.

![이미지 이름(아무거나 상관x)](https://miro.medium.com/max/663/1*GzjS6_EJkOcHkdwJdzS8oQ.png)

```java
package Sort;

public class insertionSort {
	public static void main(String[] args) {
		int B[] = {4,7,2,3,8,0};
		
		for(int i = 1; i < B.length;i++) {	// i를 기준으로 i의 앞부분이 오름차준으로 정렬되어있음
			int j = i;
			while(j > 0 && B[j-1]>B[j] ) // 앞의 친구가 나보다 크면 
			{
				int tmp = B[j];			//둘이 자리 바꿔줌
				B[j] = B[j-1];
				B[j-1] = tmp;
				--j;
			}
		}
	}
}

```
### 시간 복잡도
- 최선의 경우
- - 이미 처음부터 정렬된 배열이 주어진 경우
- - (N - 1)번 즉, O(N)
- 최악의 경우
- - 역순으로 정렬된 배열이 주어진 경우
- - while문 N번, for문 N번 즉, O(N^2)
> 이 경우 전체 시간 복잡도는 선택 정렬과 같은 O(N^2)이  된다.
> 삽입 정렬은 입력의 종류에 따라 O(N)의 속도까지 낼 수 있으며, 최악의 경우 O(N^2)인 선택정렬의 시간복잡도와 같다.
> 따라서 임의의 순열이라고 할 때, 대부분의 경우 삽입 정렬이 선택 정렬보다 빠르다.