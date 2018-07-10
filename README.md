# whatisquene
# 큐(Quene)란 무엇인가

◎ 큐 : 한쪽 방향으로 데이터가 삽입되고 반대 방향으로 데이터가 삭제되는 구조를 말함.

실생활에서는 마트에 있는 계산대가 대표적인 사례라고 볼 수 있음.  
먼저 계산대에 온 사람이 먼저 물건들을 계산하고 떠나니까.  

√ 실제로 영어 단어 Quene  
→ 표를 사러 일렬로 늘어선 사람들로 이루어진 줄을 말함  
→ 먼저 줄을 선 사람이 먼저 나갈 수 있는 상황을 연상하면 좋음.  
→ 관공서, 은행, 병원 등에서 볼 수 있는 ‘번호표’  


## FIFO (First-In First-Out)
큐는 가장 먼저 삽입된 데이터가 가장 먼저 삭제되는 선입선출(FIFO : First-In First-Out) 구조를 띠고 있다.  
(나중에 집어 넣는 데이터가 먼저 나오는 Stack과는 반대되는 개념이겠지)  


## 어떨 때 Quene가 사용되는가?
- 프린터의 출력 처리  
- 윈도우 시스템의 메시지 처리기  
- 프로세스 관리  
등 데이터가 입력된 시간 순서대로 처리해야할 할 필요가 있을 때 사용한다  


## Quene는 어떻게 구현되는가?
- put(Insert)와 get(Delete)를 이용하여 구현됨  
- put : 큐에 자료를 넣는 것
- get : 큐에서 자료를 꺼내는 것

√ 데이터의 위치
- front(head) : 데이터를 get할 수 있는 위치
- rear(tail) : 데이터를 put할 수 있는 위치

√ 각 데이터 상황
- Overflow : Quene가 꽉 차서 더 이상 자료를 넣을 수 없는 경우(put 할 수 없는 경우)
- Underflow : Quene가 비어 있어 자료를 꺼낼 수 없는 경우 (get 할 수 없는 경우)


## Python 코드로 Quene 살펴보기
- Stack과 동일하게 Quene도 append(), pop() 함수를 사용함. 약간 다른점은 입력은 Stack과 Quene 똑같이 append()를 사용하지만 출력은 pop(0)을 사용한다는 점이다

<pre> a = [1, 2, 3, 4] <code>
a.append(5)
a.append(6)

a.pop(0)
1
a.pop(0)
2

print(a)
[3, 4, 5, 6]
