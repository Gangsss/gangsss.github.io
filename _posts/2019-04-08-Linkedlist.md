---
layout: post
title: " Linked List 개념"
subtitle: ""
categories: data
tags: etc
---



현재 학교에서 자료구조 수업을 듣고 있습니다.

자료구조 수업은 개념을 듣고서 이를 실생활이나 머신러닝 라이브러리에 적용되는 사례에 대해 코드로 구현해보고 있습니다.



이번에는 Linked-List에 대한 개념과 이를 python 코드로 구현한 것을 소개해드리고 



다음 글에는 Linked-List을 활용한 TDM(Term-Document Matrix) - 희소행렬과 희소행렬 곱셈을 수행하는 함수에 대해 소개와 python 코드를 작성해보겠습니다.



# Linked List

- 노드를 연결시킨 자료구조

- 자료를 연속적인 메모리 공간에 할당할 필요없이 임의 공간에 자료를 저장하고 링크를 이용해 연결함

- 리스트에서 원소를 탐색하기 위해서는 순차탐색을 하여야 함

- 배열에서는 삽입/삭제 시 원소 이동이 필요한데 반해 리스트에서는 삽입/삭제가 원활함

- head에는 사과 노드의 주소가 저장됨

- 사과노드는 과일을 저장할 수 있는 장소와 다음 노드의 주소를 저장하는 장소로 구성됨

- 마지막 노드의 링크는 null 이 저장됨

  <img src="https://drive.google.com/uc?id=1hgU-79vThtZWe_0wWB0ZTGHmgmPtE020">





Linked List 설계

-  Node: item으로 value를 가지고 link를 가진다. link가 없을 경우, None을 입력한다.

```
class Node:
    def __init__(self, item = None):
        self.item = item
        self.link = None
```



 * root: 리스트 루트 노드이고 Linked List는 root 노드의 주소를 가진다.

```
# root 노드 만들기

class LinkedList: 
# 변수가 합성어라면 대문자로 구분시켜준다.
# Linked+List
    def __init__(self):
        self.root = Node()

fruits = LinkedList() 
# fruits는 LinkedList 클래스의 인스턴스
```



- append method: item을 주면 item 노드를 Linked List 마지막 노드에 추가하는 메소드

```
class LinkedList:
    def __init__(self):
        self.root = Node()

    def append(self, item):
   # 새로운 노드 생성 
   # 새로운 노드의 root의 item이 None이면 newNode를 
   root로 지정하고
        newNode = Node(item)
        curNode = self.root
        if curNode.item == None:
            self.root = newNode
            
    # 아니면 리스트의 끝까지 이동한 후,
      마지막 노드의 링크에 newNode의 주소를 삽입  
      
        else:
            while curNode.link != None:
                curNode = curNode.link
            curNode.link = newNode
    
    def print(self):
    # 아이템들이 다 print 될 수 있게!
        curNode = self.root
        print(curNode.item)
        while curNode.link != None:
            curNode = curNode.link
            print(curNode.item)
       
```



- insert method : index로 새로운 노드를 추가하는 메소드

```

def listSize(self):
# linked-list의 item 수를 리턴해주는 메소드
    curNode = self.root
    cnt = 1
    while curNode.link != None:
        curNode = curNode.link
        cnt += 1
    return cnt

def insert(self, idx, item):
    n = self.listSize()
    # 예외 처리
    if idx < 0 or idx >= n:
        print("index range error")
    else:
        newNode = Node(item)
        curNode = self.root
        # 인덱스가 0 일 경우 root로 추가
        if idx == 0:
            _tmp = self.root
            self.root = newNode
            newNode.link = _tmp
        else:
        # 해당 위치의 index-1번째 링크에 있는 주소를 대입
        # _tmp 이렇게 쓸경우 주로 버리는 변수에 이용한다
            for curIdx in range(idx-1):
                curNode = curNode.link
            _tmp = curNode.link
            curNode.link = newNode
            newNode.link = _tmp
```



- delete 메소드  : 주어진 값을 이용해 해당 노드를 찾고 지운다.

```
def delete(self,item): 
#item이 들어간다!
    delYN = False
    curNode = self.root
    preNode = curNode
    # 첫번째 노드와 같다면 링크에 대입
    if curNode.item == item:
        self.root = self.root.link
        delYN = True
    else:
    #중간 노드라면 index-1번째 링크에 item을 대입
        while curNode.link != None:
            preNode = curNode
            curNode = curNode.link
            if curNode.item == item:
                preNode.link = curNode.link
                delYN = True 
    # 마지막 노드였다면 마지막 링크에 none을 대입
    if curNode.item == item:
        preNode.link = None
        delYN = True
     # 예외 처리
    if delYN == False:
        print("delete failed")
```



- find method : Linked List에서 해당 아이템을 찾고 index를 리턴한다. 없으면 -1을 리턴한다. 

```
def find(self, item):
# 마찬가지로 item을 기준으로!
# index을 리턴하기위해 -1부터 시작!
    find = -1
    idx = 0
    if self.root.item == item:
        find += 1
    else:
        curNode = self.root
        while curNode.link != None:
            curNode = curNode.link
            idx += 1
            if curNode.item == item:
                find = idx
                print(find)
            else:
            	print('Not in LinkedList')
```



참고

[생활코딩](https://opentutorials.org/module/1335/8821)

[초코 몽키의 블로그](https://wayhome25.github.io/cs/2017/04/17/cs-19/)

