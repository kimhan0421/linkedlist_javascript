# linkedlist_javascript
linkedlist for javascript

- Data Type : integer
- 기능 : Tail Add, Tail Remove, Search change, Search remove, Ascending Sort(오름차순 정렬)

-----------------
## 링크드리스트 이론
### 배열이 있는데, 왜 필요한가요?
#### 배열) 반복적 접근성 가짐 + 선언 쉬움
BUT! 정렬되어 있는 배열에 새로운 데이터를 넣기 위해 많은 반복 작업이 필요.   
정렬을 시키는 것 조차도 불편함(링크드리스트도 같은 불편함 가짐)   

#### 링크드리스트) 
각 노드들 (동적할당 된 데이터들)이 포인터로 연결되어 있음   
따라서, 새로운 데이터를 동적할당해서 넣기 때문에 서로 연결만 수정 하면 됨.   
- 장점 : 배열에 비해 추가, 삭제 용이   
- 단점: 주소 계산 안됨.
따라서, 순차탐색으로 탐색속도 느림 (cf. 배열은 바이트 수로 주소계산 가능.) 

#### 프로그래머의 판단) 
- 탐색, 정렬 ⇒ 배열
- 추가, 삭제 ⇒ 링크드리스트

-----------------
## 링크드리스트 실습

- 결과-예시)
처음 결과 ) 5 -> 1 -> 6 -> 3 -> 4 -> 8 -> 7 ->   
마지막 노드 삭제 ) 5 -> 1 -> 6 -> 3 -> 4 -> 8 ->   
원하는 값(3) 삭제 ) 5 -> 1 -> 6 -> 4 -> 8 -> 7 ->   
원하는 값(3)을 바꾸기(10) ) 5 -> 1 -> 6 -> 1000 -> 4 -> 8 -> 7 ->   
오름차순 정렬 ) 1 -> 3 -> 4 -> 5 -> 6 -> 7 -> 8 ->   
- 예시 결과 코드)
```javascript
const newList = new LinkedList();
newList.tailPush(5);
newList.tailPush(1);
newList.tailPush(6);
newList.tailPush(3);
newList.tailPush(4);
newList.tailPush(8);
newList.tailPush(7);
newList.print(); // 링크드리스트 출력
```

-----------------
## 자바스크립트는 입력받을 수 없나요?
자바스크립트(Node.js)에는 C언어의 scanf, Java의 Scanner와 같이 편리하게 입력할수 있는 시스템이 없어요.   
따라서, 랜덤을 생성하는 함수에 원하는 만큼 값을 입력하면 됩니다.

```javascript
randomNumbers(number) {
    for (var i = 0; i < number; i++) {
        this.tailPush(Math.floor(Math.random() * 100 + 1));
    }
}
```
