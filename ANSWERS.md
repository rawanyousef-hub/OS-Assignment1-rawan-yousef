# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[thread is a small part of a process, while a process is a full program. Threads work inside the same process. They share the same memory, but processes do not. This makes threads faster to use. In this assignment, each process runs as a thread. So they can run together at the same time.]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[In Round-Robin scheduling, if a process does not finish within its time quantum, it stops and goes back to the end of the ready queue. This lets other processes run before it continues. This way, all processes get a fair chance to use the CPU...]

Example from my output:
```
[P1 executing quantum [715ms]
Quantum progress: 100%
P1 completed quantum 715ms
Remaining time: 6ms]
```

**Explanation of example:**
[n this example, P1 used all its time quantum but did not finish because it still has 6ms left. So it will go back to the ready queue and wait for its turn again. This shows how the ready queue works in Round-Robin. It helps make sure all processes run fairly and no process takes all the CPU time.]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

In my program, P1 goes through different states while running.at first, P1 is in the New state when it is created but not started yet.then it becomes Runnable after calling Thread.start(), which means it is ready to run. after that, it becomes Running when the CPU starts executing it.Sometimes, P1 goes to Waiting when Thread.sleep() is used, so it pauses for a while.It can also go to Waiting when Thread.join() is used because it waits for another thread. Finally, P1 becomes Terminated when it finishes execution.

1. **New**: [P1 is in New state when it is created but not started yet.]

2. **Runnable**: [After calling Thread.start(), P1 becomes Runnable and waits for CPU..]

3. **Running**: [p1 is Running when CPU starts executing it.]

4. **Waiting**: [P1 goes to Waiting when Thread.sleep() is used, or when it waits using Thread.join().]

5. **Terminated**: [P1 becomes Terminated when it finishes execution.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [web server]

**Description**: 
[In a web server, many users send requests at the same time, and each one is handled by a thread.]

**Why Round-Robin works well here**: 
[Round-Robin gives each request a short time, then moves to the next one. This makes it fair and helps users not wait too long.]

### Example 2: [media player]

**Description**: 
[in a media player, tasks like audio, screen update, and user input run together.]

**Why Round-Robin works well here**: 
[Round-Robin lets each task run for a short time, so everything runs smoothly and the system stays responsive..]

---

## Summary

**Key concepts I understood through these questions:**
1. How Round-Robin scheduling works.
2. How processes move between states.
3. How fairness and responsiveness are important in scheduling.

**Concepts I need to study more:**
1.  More details about thread synchronization.
2. How different scheduling algorithms compare
