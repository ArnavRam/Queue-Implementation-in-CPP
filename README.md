# Experiment 19 - Queue Implementation using Array

---

## Aim
- To study and implement Queue operations in C++, including insertion (enqueue), deletion (dequeue), and display.
- To understand how queues manage data based on the FIFO (First In, First Out) principle using an array.

---

## Tools Used
- Visual Studio Code
- MinGW-w64 with g++ Compiler

---

## Theory
A **Queue** is a linear data structure that follows the **FIFO (First In, First Out)** principle. The element that is inserted first is the first one to be removed, similar to a real-life queue. A queue is managed with two pointers:
- **`front`:** Points to the first element in the queue (the one to be dequeued).
- **`rear`:** Points to the last element in the queue (where new elements are enqueued).

### Key Characteristics
- **FIFO Order:** The first element added is the first to be removed.
- **Restricted Access:** Insertions (enqueue) happen only at the `rear`, and deletions (dequeue) happen only at the `front`.
- **Overflow/Underflow:** Overflow occurs when an attempt is made to enqueue an element into a full queue. Underflow occurs when an attempt is made to dequeue an element from an empty queue.

---

## Algorithm / Logic
1.  **Start**
2.  Initialize an integer array `queue_array` of a fixed `SIZE`.
3.  Initialize `front = -1` and `rear = -1`.
4.  Display a menu with options: 1. Insert (Enqueue), 2. Delete (Dequeue), 3. Display, 4. Exit.
5.  Use a loop to repeatedly ask the user for their choice until they select Exit.

    -   **Case 1: Insert (Enqueue)**
        -   Check if the queue is full (`rear == SIZE - 1`). If so, print "Queue Overflow".
        -   Otherwise, prompt the user for a value to insert.
        -   If `front == -1`, set `front = 0`.
        -   Increment `rear` by 1.
        -   Store the value at `queue_array[rear]`.

    -   **Case 2: Delete (Dequeue)**
        -   Check if the queue is empty (`front == -1` or `front > rear`). If so, print "Queue Underflow".
        -   Otherwise, display the element at `queue_array[front]`.
        -   Increment `front` by 1.

    -   **Case 3: Display**
        -   Check if the queue is empty. If so, print "Queue is empty".
        -   Otherwise, use a `for` loop to iterate from `front` to `rear` and print each element of the queue.

    -   **Case 4: Exit**
        -   Terminate the program.

6.  **End**

---

## Conclusion
Queues are essential data structures for managing data in a FIFO order. This experiment demonstrated how to implement a queue using an array and manage its state with `front` and `rear` pointers. The core operations of enqueue (insertion at the rear) and dequeue (deletion from the front) were successfully implemented, along with checks for overflow and underflow conditions. Mastering queues is crucial for solving real-world problems related to scheduling, data buffering, and resource allocation in systems.
