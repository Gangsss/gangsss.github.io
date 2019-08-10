---
layout: post
title: "스택과 큐"
subtitle: ""
categories: data
tags: etc
comments: true
---

## Stack



- [Stack의 정의](https://ko.wikipedia.org/wiki/%EC%8A%A4%ED%83%9D)

  한 쪽 끝에서만 자료를 넣거나 뺄 수 있는 선형 구조(LIFO - Last In First Out)으로 되어 있다.

   

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/stack.png">





- Stack의 method
  - push : 스택에 item을 삽입하는 연산
  - pop : 스택에 있는 item중 가장 위의 item을 삭제하고 return
  - peek : 스택에 있는 item중 가장 위의 item을 return
  -  isEmpty : 스택이 공백인지 아닌지를 확인하는 연산 

 

list을 활용해 stack을 구현해보면 



    class Stack:
    	# stack 선언
        def init(self):
            self.s = []
            
        # 뒤에 들어가므로 append 활용
        def push(self, item):
            self.s.append(item)
            
        def isEmpty(self):
            if len(self.s) > 0:
                return False
            else:
                return True
    
    	# 가장 뒤에 것이 나와야한다.
        def pop(self):
            if self.isEmpty() == False: 
                return self.s.pop(-1)
            else:
                return None
                
    	# 뒤에 것을 보여주기만 해야한다. 
        def peek(self):
            if self.isEmpty() == False: 
                return self.s[-1]
            else:
                return None
    
        def size(self):
            return len(self.s)
    
        def print(self):
            print(self.s)



하지만, 파이썬에서는 list에서 스택을 사용 할 수 있다.



[참고](<https://docs.python.org/ko/3/tutorial/datastructures.html> )



```
>>> stack = [6,7,8]
>>> stack.append(9)
>>> stack.append(10)
>>> stack
[6,7,8,9,10]
>>> stack.pop()
10
>>> stack
[6,7,8,9]
>>> stack.pop()
9
>>> stack.pop()
8
>>> stack
[6,7]
```



push method는 append로 사용할 수 있고



pop은 구현이 되어있으며 



peek은 위의 예시에서 보면 stack[-1] 형태로 확인 할 수 있다.



## Queue



- Queue의 정의]([https://ko.wikipedia.org/wiki/큐_(자료_구조)](https://ko.wikipedia.org/wiki/%ED%81%90_(%EC%9E%90%EB%A3%8C_%EA%B5%AC%EC%A1%B0)) 

  먼저 집어 넣은 데이터가 먼저 나오는 FIFO (First In First Out)구조로 저장하는 형식 

  

<img src="https://raw.githubusercontent.com/Gangsss/gangsss.github.io/master/assets/img/queue.png">



- Queue의 method
  - enQueue : 큐의 item을 뒤에 삽입하는 연산
  - deQueue : 큐의 가장 앞에있는 item을 삭제하고 반환
  - delete : 큐의 가장 앞에있는 item을 삭제하는 연산
  - peek: 큐의 앞에 있는 item을 return



큐 또한 list을 활용한다.



    class Queue:
    	# 큐를 선언
        def init(self):
            self.q = []
            
        def isEmpty(self):
            if len(self.q) > 0:
                return False
            else:
                return True
                
    	# 큐에 item을 뒤에 삽입하므로 append
        def enQueue(self, item):
            self.q.append(item)
    
    	# 큐의 맨앞에 있는 item이므로 pop(0)
        def deQueue(self):
            if self.isEmpty() == False: 
                return self.q.pop(0)
    
        def size(self):
            return len(self.q)
    	
        def peek(self):
            if self.isEmpty() == False: 
                return self.q[0]
    
        def delete(self, item):
            if item in self.q: 
                self.q.remove(item)
            else:
                print("해당 아이템이 존재하지 않습니다.")



위와 같이 list을 활용해 큐를 구현 할 수 있지만 



 [`collections.deque`](https://docs.python.org/ko/3/library/collections.html#collections.deque) 을 사용하게 되면  더 빠르게 쓸 수 있습니다.



[참고](https://docs.python.org/ko/3/tutorial/datastructures.html)



```
>>> from collections import deque
>>> queue = deque(["Eric", "John", "Michael"])
>>> queue.append("Terry")           # 위에서 enqueue
>>> queue.append("Graham")          
>>> queue.popleft()                 # 위에서 dequeue
'Eric'
>>> queue.popleft()                 
'John'
>>> queue                           # 남아있는 queue
deque(['Michael', 'Terry', 'Graham'])
```



- 헷갈리지 말아야 하는 사항
  - popleft - 가장 왼쪽의 item 삭제 후 return(deQueue)
  - pop - 가장 오른쪽의 item 삭제 후 return



큐의 경우 뒤로 입력되고 앞에서 출력이 되는 구조인데 이런 구조를 변형해 DeQueue(Double Ended Queue) 즉, 양쪽에서 입력과 출력이 가능한 자료구조가 있다.



이는 이미지 viewer 혹은 mp3 플레이어 앞뒤의 곡을 불러오는 프로그램에 활용ㄴ되기도 한다.