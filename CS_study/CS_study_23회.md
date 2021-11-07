# CS_study_23회

## 1. [알고리즘] Python sort()

> Python의 내장함수 sort에 사용된 정렬 방식을 설명해주세요.

- Python의 sort() 함수에 쓰인 알고리즘은 Timsort입니다.
- 삽입 정렬과 병합 정렬을 섞은 알고리즘으로, 정렬을 해야하는 전체 덩어리를 작은 덩어리로 자른 후 각각의 덩어리를 삽입 정렬로 정렬한 뒤, 병합 정렬로 병합하는 정렬입니다.

- '실제 데이터는 대부분 이미 정렬되어있을 것이다'라는 가정에 기반한 정렬 알고리즘으로 평균 O(nlogn)의 시간 복잡도를 가지며 stable sort에 속합니다.
- Python뿐만 아니라 Java SE 7, Android, Google chrome (V8), Swift 등에서 표준 정렬 알고리즘으로 채택된 알고리즘입니다.



## 2. [자료구조] B+tree

- B+tree 구조는 B-tree와 구조가 유사하지만, 리프노드가 연결리스트의 형태를 띠어 선형 검색이 가능하다는 점에서 차이가 있습니다. 이러한 특징으로 인해 신속한 검색이 가능합니다.

![img](https://media.vlpt.us/images/emplam27/post/64290106-d927-4a82-9e08-8e52783c7dd3/DB%20%EC%9D%B8%EB%8D%B1%EC%8A%A4.jpg)

![img](https://media.vlpt.us/images/emplam27/post/bcbce100-d475-4cda-aebe-946d1813949c/B%ED%94%8C%EB%9F%AC%EC%8A%A4%20%ED%8A%B8%EB%A6%AC%20%EA%B8%B0%EB%B3%B8%20%ED%98%95%ED%83%9C.jpg)

- B+tree의 특징
  1. 모든 key, data가 리프노드에 모여있습니다.
     - B-tree는 리프노드가 아닌 각 key마다 data를 가진다는 점에서 차이가 있습니다.
  2. 모든 리프노드가 연결리스트의 형태를 띠고 있습니다.
     - B-tree는 옆 리프노드를 검사 시 다시 루프노드부터 검사해야 하지만 B+tree는 리프노드에서 선형검사를 수행할 수 있어 시간복잡도가 크게 줄어듭니다.

참고: https://velog.io/@emplam27/%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0-%EA%B7%B8%EB%A6%BC%EC%9C%BC%EB%A1%9C-%EC%95%8C%EC%95%84%EB%B3%B4%EB%8A%94-B-Plus-Tree

