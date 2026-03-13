# Queue
Practice program 
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class Queue:
    def __init__(self):
        self.front = None
        self.rear = None
    def enqueue(self, data):
        new_node = Node(data)
        if self.rear is None:
            self.front = self.rear = new_node
        else:
            self.rear.next = new_node
            self.rear = new_node
        print "Enqueued:", data
    def dequeue(self):
        if self.front is None:
            print "Queue is empty"
            return
        print "Dequeued:", self.front.data
        self.front = self.front.next
        if self.front is None:
            self.rear = None
def display(self):
        current = self.front
        if current is None:
            print "Queue is empty"
            return
        print "Queue elements:"
        while current:
            print current.data
            current = current.next
q = Queue()
q.enqueue(1)
q.enqueue(2)
q.enqueue(3)
q.display()
q.dequeue()
q.display()
Output:
Enqueued: 1
Enqueued: 2
Enqueued: 3
Queue elements:
1
2
3
Dequeued: 1
Queue elements:
2
3
