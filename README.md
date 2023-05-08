Download Link: https://assignmentchef.com/product/solved-solved-attached-solution-to-lab-4-abstract-data-types
<br>
Learning outcomesBy the end of this lab, you will be able to:

Define the new abstract data type called the queueImplement a queue using Python listsCompare the runtime efficiency of two different implementations of an ADT using simple profilingBrainstorm different implementations for an ADTTask 0 – Starter CodeDownload all files and put them into your labs/lab4 folder.

myqueue.py (Task 1)timer.py (Task 2)timequeue.py (Task 2)Task 1 – QueuesThis week we learned about stacks, a very simple ADT that always removes items in “reverse” order, so that the most recently added item is the first that gets removed. A queue is another simple ADT that does the opposite: when asked to remove an item, a queue always removes the item that was added first, making it a “first-in-first-out” (FIFO) data structure. Any time we’d like to model a line (of people at the grocery store, for example), queues are a natural choice. (You’ve been working with priority queues in Assignment 1. This is another ADT that elaborates the concept of a queue to add in the notion of priority.)

Here are the operations supported by the queue ADT:

__init__: create a new empty queueis_empty(): return True if the queue is empty (and False otherwise).enqueue(item): add item to the back of the queue.dequeue(): remove and return the front item, if there is one, or None if the Queue is empty.Your first task is to implement the Queue class found in myqueue.py. We strongly recommend you review the stack implementation from lecture to remember how we used a list to implement the Stack class.

After you’ve finished, complete the functions product and product_star in myqueue.py, which compute the product of all numbers in a queue (but have an important difference).

Task 2 – ProfilingLet’s test the performance of our Queue class against Stack from lecture. To start, open timequeue.py. Using the technique from class, run some experiments to measure the time it takes to enqueue and dequeue items as the size of the list grows. Feel free to add your own queue-manipulation methods for experimenting! We recommend having queue sizes in the 10 000’s to see some noticeable growth in the time taken.

You should see that at least one of your queue operations takes linear time (i.e., time to execute the operation grows proportionally to the size of the queue). Make sure that both you and your partner can explain to each other why this is the case.

Then, spend the remaining time brainstorming ways of changing your Queue implementation to make both enqueueand dequeue run in constant time (independent of the size of the queue). Be creative, and have fun!

Additional exercisesIf you finish the first two tasks, here are some additional exercises:

Write a function which takes a stack of numbers and removes all of the items which are greater than 5 (but leaves the original items in place).Repeat #1, but with a queue instead of a stack.Write a function which takes a stack and returns a new stack which contains two copies of every item in the old stack.Repeat #3, but with a queue instead of a stack.Write a program which continually prompts the user for a string, and stores the strings in a stack. When the user types “UNDO”, rather than storing that string, it prints out the most recently stored word, and removes it from the stack.