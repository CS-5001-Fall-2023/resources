Exam 2 Study Guide
==================

## Logistics

Exam 2 will take place in person on Monday, December 4 from 6-7:40pm. It will be 8-12 questions in length. You may be asked to define terminology, trace code, explain code, and write code. 

## Topics

The exam may cover any topics we have discussed this semester. It is recommended that you review the Exam 1 study guide as well.

* Recursion
  - Given a recursive function, describe what it does
  - Given a recursive function, identify the base case
  - Given a recursive function, describe how the recursive call makes progress toward the base case
  - Identify and fix a bug in a recursive function
  - Write a recursive function to solve a given problem
* Errors/Error Handling
  - Use try/except to handle an error
  - Write a function that raises errors
* Dictionaries
  - Insert a new item into a dictionary
  - Determine if a value exists in a dictionary
  - Find a data item stored in a dictionary
* Classes
  - Create an instance of a class
  - Call a method on an object
* Stacks
  - Describe the result of applying one or more push/pop operations
  - Identify and fix bugs in a Stack implementation
  - Add additional operations to a Stack implementation
  - Use a Stack to solve a problem (e.g., determining whether parens are matching)
* Queues
  - Describe the result of applying one or more enqueue/dequeue operations
  - Identify and fix bugs in a Queue implementation that uses a circular buffer
* Efficiency
  - Determine the runtime bounds of an algorithm or code snippet (e.g., understand running time of operations on lists versus dictionaries)
  - Design a data structure to ensure a particular runtime bound for a given operation 
* Linear search
  - Find an item in a list
* Binary search
  - Identify and fix bugs in a binary search implementation
  - Trace the execution of a binary search implementation
* Sorting
  - Trace the execution of a sorting algorithm -- insertion, selection, or bubble sort


## Example Problems

**Question 1**
Write a function called validation that behaves as follows:

Function: validation
   perform multiplication with different types
Parameters:
   one. an negative integer value
   two. a positive floating point number less than 1000
Returns the product of the two parameter values

The function will raise an error if one is not a negative integer or if two is not a postive floating point numebr less than 1000.

**Question 2**
Write a function called get\_key\_string that receives a dictionary and returns the keys of the dictionary as a string separated by the character '-'.

**Question 3**
Write a function called initialize that creates and returns a dictionary that contains the following data:

|Keys| Values	                    |
|---|----------------------------|
| Maria | Associate Professor |
| Jodi | Associate Dean of Network Programs |
| Beth | Dean of Khoury |

**Question 4**

```python
class Pair:

	def __init__(self, x, y):
		self.x = x
		self.y = y	
				
	def sum(self):
		return self.x + self.y
```

Given the class definition above write a code fragment that does the following:

1. Create an instance of Pair
2. Call the sum method and print the result

**Question 5**
What is the result of applying the following operations on a ```Stack```? Provide the output of the code fragment.

```python
stack = Stack(5)
stack.push(23)
stack.push(37)
stack.push(92)
print(stack.pop())
stack.push(45)
print(stack.pop())
print(stack.pop())
```

**Question 6**
What is the result of applying the following operations on a ```Queue```? Provide the output of the code fragment.

```python
queue = Queue(5)

queue.enqueue(23)
queue.enqueue(37)
queue.enqueue(92)
print(queue.dequeue())
queue.enqueue(45)
print(queue.dequeue())
print(queue.dequeue())
```

**Question 7**
Consider a ```Stack``` implementation that uses a list to store the items in the ```Stack```. One possible implementation for ```push``` is to insert the new item at the beginning of the list. The implementation of ```pop``` then removes the item at position 0. Another possible implementation for ```push``` is to append the new item at the end of the list. The implementation of ```pop``` then removes the last item. Which approach is better *and why*?

**Question 8**
Given a ```Queue``` implemented using a circular buffer, what is the big-oh running time of the ```enqueue``` operation and the ```dequeue``` operation?

**Question 9**
Consider an email application. Assume the top-level data structured used in the application is a dictionary that maps a username to a data structure that stores a collection of individual messages. Would you choose to store the collection of individual messages in a list or a dictionary? Explain your answer.

**Question 10**
The ```selection_sort``` algorithm can be implemented as follows:

```python
def selection_sort(things):
    '''
    Function: selection_sort -- sorting the elements of a list by inserting
                                each element into a list in order
    Parameters:
       things -- the elements to be sorted
    Returns a new list with all of the elements in sorted order
    '''
    for i in range(len(things) - 1):
        # select the next element by finding it in things
        min = i
        for j in range(i + 1, len(things)):
            if things[j] < things[min]:
                min = j
        things[i], things[min] = things[min], things[i]
    return things
```

Given the following input, show the state of the list things after every iteration of the outer for loop:

```things = [5, 2, 6, 1, 7, 3, 4]```

**Question 11**
Write a recursive function ```check_wordle``` that takes as input a wordle word and a guess and returns the number of *green* letters -- that is, the number of letters that are the same letter in the same position in both the wordle word and the guess.