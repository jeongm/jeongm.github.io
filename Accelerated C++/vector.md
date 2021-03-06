# vector
- C++에서 벡터는 표준 템플릿 라이브러리(STL)에서 제공하는 동적 배열구조 클래스입니다.
- C의 배열처럼 빠른 랜덤 접근이 가능하며 자동으로 배열의 크기 조절과 추가 삭제가 가능합니다.
- 모든 자료형에 대해 배열처럼 저장할 수 있지만 한번에 한 타입만 저장이 가능합니다.
- 자바의 벡터와 마찬가지로 배열 크기를 추가할때 기존 배열 크기의 100%가 늘어납니다.(2배)

## C++ vector 사용법

- vector<자료형> 변수명 
  >: 백터 생성
- vector<자료형> 변수명(숫자,0)
  >: (숫자)크기의 백터 생성, 0으로 초기화
- vector<자료형> 변수명 = {변수1,변수2,...}
  >: 백터 생성, 오른쪽 변수로 초기화   
```c++
vector<int> a;          //int형 vector생성

vector<int> a(3);       // int형 크기 3의 vector생성
vector<int> a(3,1);     // int형 크기 3의 vector생성, 1로 초기화

vector<int> a = {1,3,4}   // int형 백터 생성 후 1,3,4로 초기화
```

## vector 요소 삽입

- 변수명.push_back()
> : 백터의 마지막 부분에 새로운 요소 추가
- 변수명.pop_back()
> : 백터의 마지막 부분 제거
- 변수명.clear()
> : 백터의 모든 요소 지움(return size = 0)
- 변수명.swap(백터 변수) 
> : 백터와 백터 스왑

```c++
a.push_back(3);         // vector의 끝 부분에 3 추가
```


## +
삽입과 삭제가 빈번히 일어날 경우에는 vector보단 list나 deque를 사용하는 것이 바람직함
