# [DSA-project2]_2023171416
Heap 자료구조와 Sort 알고리즘(Heap, Sort, Insertion Sort 등)을 구현하고, 이를 활용하여 다양한 연산을 수행하는 프로그램이다. 이 프로젝트는 힙의 기본 속성을 유지하면서 삽입, 삭제, 정렬과 같은 연산을 지원한다.

# 파일 구조
1) heap.h: Heap 자료구조와 관련된 함수 선언이 포함된 header file
2) heap.c: Heap 자료구조의 기능 구현 및 sort 알고리즘 code file
3) project2_main.c: 프로그램의 주요 기능을 테스트하는 main file

#  compile 및 실행
1. Cygwin 실행: 프로젝트 파일이 위치한 directory로 이동한다.
   ex) cd /cygdrive/c/your_project_directory
   
2. Compile: Makefile을 이용해서 프로젝트를 compile 한 후 실행 파일을 make한다.

3. 프로그램 실행: compile이 완료되면 명령어로 실행 파일을 실행한다.
   ex) ./project2_main.exe


# 주요 기능 설명
1. Heap 구현 (함수 설명)
 : Min-Heap을 기반으로 동작하며 node 삽입, 삭제, heap 정렬을 작동한다.
 * bstToArrayRec: complete된 bst를 array로 변환
 *  buildHeap: 주어진 array를 기반으로 Min-Heap 구조로 변환
 *  deleteHeap: node 삭제
 *  findDepth: Heap의 depth 출력
 * insertNode: Heap에 새로운 node 값 삽입
 * dequeueHeap: Min-Heap에서 최솟값(root node)을 제거하고 반환하고 heap속성을 유지하며 bubble down 수행

2. Heap Sort
 : Min-Heap을 활용하여 array sort
 : array를 heap으로 변환 후 min heap 속성을 유지하며 sort
  + Heap sort는 O(nlogn)을 가진다.
 * heapsort: array를 min-heap으로 변환하고 heap에서 최솟값을 제거하면서 sort한다.
 * bubble sort: bubble sort를 수행하여 array sort
 * insertion sort: insertion sort를 수행하여 array sort
 * selection sort: selection sort를 수행하여 array sort
 * quick sort: quick sort를 수행하여 array sort

(자세한 함수에 대한 설명은 heap.c 파일의 코드 주석에 작성하였습니다.)

# 실행 예시
### Build Heap  
  Input Array: [4, 10, 3, 5, 1]
  Heap Built.
  Heap: [1, 4, 3, 10, 5]
  Depth = 3, Size = 5

### Insert Node
   
  Insert Value: 2
  Node with value 2 inserted successfully.
  Heap: [1, 2, 3, 10, 5, 4]
  Depth = 3, Size = 6

### Dequeue Node
   
   Dequeued Value: 1
   Heap after Dequeue: [2, 4, 3, 10, 5]
   Depth = 3, Size = 5

### Heap Sort
   
   Input Array: [4, 10, 3, 5, 1]
   Sorted Array: [1, 3, 4, 5, 10]

