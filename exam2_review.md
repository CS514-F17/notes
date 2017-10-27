Exam 2 Review
===========

### Topics
- Data structures
  - design and integration of data structures
  - efficiency concerns
  - Maps versus Lists
  - Common Java implementations
- Recursion
  - Algorithm design
  - Base case
  - Recursive case
- Linked Lists
- Concurrency
  - advantages of multithreaded programs
  - `Runnable` interface
  - `Thread` class
  - `WorkQueue`
    * advantages
    * implementation
    * limitations of IBM implementation
  - `wait/notify/notifyAll`
  - `synchronized`
  - atomicity
  - concurrent operations
  - read/write locks


### Sample Questions

Give an example of when you would choose to use an `ArrayList` rather than a `TreeSet`. Explain the specific example and why you chose this example.

---

Consider the following method from a class Lock that attempts to acquire a write lock. 

1. Explain how the bug in this method could cause incorrect behavior of the program.  
2. Explain how you would fix the problem.

```java
   public synchronized void lockWrite() {
		if(this.writers > 0 || this.readers > 0) {
   			try {
   				this.wait();
   			} catch (InterruptedException e) {
   				e.printStackTrace();
   			}
   		}
   		this.writers++;
   	}
```

---

Are the methods of the `Sample` class below threadsafe?  That is, should `setOne` and `setTwo` be synchronized?  For full credit, explain your answer.

```java
public class Sample {
	private volatile int a;

	public void setOne() {
   			a = 1;
	}

	public void setTwo() {
   			a = 2;
	}
}
```

---

Which of the following are conflicting operations?

1. read/read
2. read/write
3. write/write

---

What is an advantage to using a ReadWriteLock to ensure thread safety rather than using synchronized methods?

---

List all possible program outputs for the multithreaded program below.
 
```java
public class Worker implements Runnable {
	public String message;
	
	public Worker(String message) {
		this.message = message;
	}
	
	public void run() {
		System.out.println(message);
	}

	public static void main(String[] args) {
		Thread t1 = new Thread(new Worker("hello"));
		Thread t2 = new Thread(new Worker("goodbye"));
		t1.start();
		System.out.println("the end");
		t2.start();
	}
}

```

---

Write a method `getIth` for the `LinkedList` class. The method will take as input an integer `i` and will return the object from the ith node in the list. For a list containing A, B, C, D, E (in that order), given the input 2 the method would return B.

---

Implement a recursive method that takes as input a `char` and a `String` and returns the number of times the `char` appears in the `String`. Given input 'c' and 'computer' the method would return 1. For full credit, implement this method without using any loops.

---
Implement a `LinkedList` method `removeLastN`. The method takes as input an integer n and removes the last n nodes from the list. If the list contained 6 nodes, a call to `removeLastN(3)` would result in the list containing the first three nodes of the original list (e.g., original list: head->A->B->C->D->E->F new list: head->A->B->C)

---

What does the following method of a LinkedList class do?

```java
    public boolean mystery() {
        if(this.head == null) {
            return true;
        }
        return mystery(this.head, this.head.getNext());
    }
    private boolean mystery(Node n1, Node n2) {
        if(n2 == null)
            return true;
        if(n1.getData().compareTo(n2.getData()) < 0)
            return mystery(n2, n2.getNext());
        return false;
    }    
```