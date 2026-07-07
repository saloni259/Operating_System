# Operating System

## Definition
Operating System (OS) is system software that acts as an interface between user and hardware and manages system resources.

## Main Functions
- Process Management
- Memory Management
- File Management
- Device Management
- Security and Protection

## Why OS is Needed
- Hides hardware complexity.
- Provides easy access to hardware resources.
- Manages CPU, memory and devices.

## OS as Resource Manager
OS manages:
- CPU
- RAM
- Disk
- I/O Devices
- Network

## OS as Abstraction Layer
OS hides hardware details and provides simple interfaces to applications.

## Examples
- Windows
- Linux
- macOS
- Android
- iOS

## Interview One-Liner
Operating System is system software that manages computer resources and acts as an interface between user and hardware.
# Goals of Operating System

## 1. Maximum CPU Utilization
Keep CPU busy as much as possible.

Example:
- P1 is waiting for disk I/O.
- OS gives CPU to P2 instead of keeping CPU idle.

---

## 2. Maximum Throughput
Number of processes completed per unit time.

Formula:
Throughput = Completed Processes / Time

Example:
- 20 processes completed in 10 sec
- Throughput = 2 processes/sec

---

## 3. Minimum Turnaround Time
Total time taken from process arrival to completion.

Formula:
Turnaround Time = Completion Time - Arrival Time

Example:
Arrival = 2 sec
Completion = 12 sec
TAT = 10 sec

---

## 4. Minimum Waiting Time
Time spent waiting in ready queue.

Example:
Process arrives at 0 sec.
Starts execution at 5 sec.
Waiting Time = 5 sec.

---

## 5. Minimum Response Time
Time taken to give first response to user.

Example:
- Clicking Chrome and window opens in 0.5 sec.
- Smaller response time means better user experience.

---

## 6. Fair Resource Allocation
Every process should get a fair chance to execute.

Example:
A long-running process should not block small processes forever.

---

## 7. Reliability
System should continue working even if some components fail.

Example:
In multi-CPU systems, if one CPU fails, another can continue execution.

---

## 8. Security and Protection
One process should not access another process's memory.

Example:
Chrome cannot directly read WhatsApp's memory.

---

## Interview Answer
Goals of OS:
- Maximum CPU Utilization
- Maximum Throughput
- Minimum Turnaround Time
- Minimum Waiting Time
- Minimum Response Time
- Fairness
- Reliability
- Security
# Functions of Operating System

## 1. Process Management
Manages execution of processes.

Functions:
- Create process
- Schedule process
- Suspend process
- Resume process
- Terminate process

Example:
CPU executes:
Chrome → VS Code → Spotify

---

## 2. Memory Management
Manages RAM allocation and deallocation.

Functions:
- Allocate memory
- Free memory
- Track memory usage
- Protect memory

Example:
8GB RAM:
- Chrome → 2GB
- VS Code → 1GB
- Spotify → 500MB

---

## 3. File Management
Manages files and directories.

Functions:
- Create/Delete files
- Create/Delete folders
- Manage permissions

Example:
Creating or deleting a file is handled by OS.

---

## 4. Device Management
Controls hardware devices.

Functions:
- Allocate devices
- Release devices
- Manage device drivers

Example:
Keyboard → OS → Application

---

## 5. Security and Protection
Protects processes and files.

Example:
Chrome cannot access WhatsApp memory directly.

---

## 6. Resource Allocation
Distributes CPU, RAM and devices fairly.

Example:
CPU time is shared among Chrome, VS Code and Spotify.

---

## 7. Error Detection
Detects hardware and software failures.

Example:
Disk failure or printer disconnect.

---

## 8. Accounting
Tracks resource usage.

Example:
Task Manager showing CPU and RAM usage.

---

## 9. Communication Management
Allows processes to communicate.

Example:
Browser process communicates with network process.

---

## Interview One-Liner
OS manages processes, memory, files, devices and system resources efficiently.
# Types of Operating Systems

Operating Systems are classified based on how they manage processes, CPU, memory, and resources.

---

# 1. Single Process Operating System

## Definition
A Single Process OS allows only one process to execute at a time.

If one process is running, no other process can execute until it finishes.

## Why was it needed?
Early computers had limited memory and processing power, so running multiple programs together was not possible.

## Example
Suppose you open Calculator.

While Calculator is running:
- Browser cannot run.
- Music player cannot run.
- Text editor cannot run.

Only after Calculator closes can another program start.

## Real Example
- MS-DOS

## Advantages
- Simple design.
- Requires very little memory.

## Disadvantages
- CPU remains idle during I/O operations.
- Poor resource utilization.
- No multitasking support.

## Interview Point
Single Process OS executes only one process at a time.

---

# 2. Batch Operating System

## Definition
Batch OS collects multiple jobs and executes them in groups called batches.

Users do not interact directly with the computer during execution.

## Why was it needed?
In early computers, repeatedly loading jobs manually wasted time.

Grouping similar jobs together improved efficiency.

## Working
1. Users submit jobs to the operator.
2. Operator groups similar jobs into batches.
3. OS executes one batch after another.

## Example
A university wants to:
- Generate marksheets.
- Process fees.
- Generate attendance reports.

Instead of executing each job individually:

Batch 1 → Marksheet generation
Batch 2 → Fee processing
Batch 3 → Attendance processing

## Real Example
- IBM Mainframe Systems

## Advantages
- Better CPU utilization than single process systems.
- Suitable for repetitive jobs.
- Reduces setup time.

## Disadvantages
- Long waiting time.
- Difficult debugging.
- No user interaction.
- A high-priority job may wait behind low-priority jobs.

## Interview Point
Batch OS executes jobs in groups without user interaction.

---

# 3. Multiprogramming Operating System

## Definition
Multiple programs are loaded into memory simultaneously.

When one process waits for I/O, CPU executes another process.

## Why was it needed?
In Batch OS, CPU often stayed idle during I/O operations.

Multiprogramming keeps CPU busy.

## Example

Suppose:

P1 → Waiting for disk read
P2 → Ready to execute

Instead of keeping CPU idle:

CPU executes P2.

Thus CPU utilization increases.

## Main Goal
Increase CPU utilization.

## Characteristics
- Multiple processes in memory.
- Single CPU.
- Context switching occurs.
- CPU idle time decreases.

## Advantages
- Better CPU utilization.
- Higher throughput.
- Reduced idle time.

## Disadvantages
- Complex memory management.
- Requires scheduling algorithms.

## Interview Point
Multiprogramming improves CPU utilization by executing another process during I/O wait.

---

# 4. Multitasking Operating System

## Definition
Multitasking allows multiple tasks to appear to run simultaneously.

Actually, CPU rapidly switches between tasks.

## Why was it needed?
Users wanted to interact with multiple applications at the same time.

## Example
You can simultaneously:
- Listen to Spotify
- Browse Chrome
- Write code in VS Code
- Download files

CPU executes:

Chrome → Spotify → VS Code → Chrome → ...

The switching is extremely fast, creating an illusion of parallel execution.

## Characteristics
- Single CPU.
- Uses time sharing.
- Context switching occurs frequently.
- Improves responsiveness.

## Advantages
- Better user experience.
- Faster response time.
- Multiple applications can run together.

## Disadvantages
- Frequent context switching adds overhead.

## Examples
- Windows
- Linux
- macOS

## Interview Point
Multitasking focuses on responsiveness, whereas multiprogramming focuses on CPU utilization.

---

# Multiprogramming vs Multitasking

| Multiprogramming | Multitasking |
|-----------------|-------------|
| Goal is CPU utilization | Goal is responsiveness |
| Switching occurs during I/O wait | Switching occurs using time sharing |
| Mainly used in early systems | Used in modern systems |
| User interaction is less important | User interaction is important |

---

# 5. Multiprocessing Operating System

## Definition
A Multiprocessing OS uses more than one CPU to execute processes simultaneously.

## Why was it needed?
A single CPU can execute only one instruction at a time.

Multiple CPUs provide true parallel execution.

## Example

CPU1 → Chrome
CPU2 → VS Code
CPU3 → Spotify

Unlike multitasking, these processes actually run simultaneously.

## Characteristics
- Multiple CPUs available.
- True parallelism.
- Better reliability.

## Advantages
- Higher throughput.
- Better performance.
- Faster execution.
- Improved fault tolerance.

## Disadvantages
- Expensive hardware.
- Complex synchronization.

## Examples
- Modern desktops
- Servers
- Data centers

## Interview Point
Multiprocessing provides true parallelism because multiple CPUs are present.

---

# 6. Distributed Operating System

## Definition
Distributed OS manages multiple computers and makes them appear as a single system.

## Why was it needed?
Some tasks require more computational power than a single computer can provide.

## Example

Computer A
Computer B
Computer C

A large task is divided among these computers.

Users feel they are using one large computer.

## Examples
- Cloud computing
- Large data centers

## Advantages
- Scalability
- Resource sharing
- Fault tolerance
- Faster processing

## Disadvantages
- Complex implementation.
- Network dependency.

## Interview Point
Distributed OS uses multiple independent computers connected through a network.

---

# 7. Real-Time Operating System (RTOS)

## Definition
A Real-Time OS guarantees that tasks complete within strict deadlines.

Correctness depends on both:
- Correct result
- Correct timing

## Why was it needed?
Some systems cannot tolerate delays.

## Example
Car Airbag System:

If collision occurs,
the airbag must open within milliseconds.

Opening after 5 seconds is useless.

## Applications
- Air Traffic Control
- Medical Equipment
- Industrial Robots
- Missile Systems

## Types

### Hard Real-Time OS
Missing a deadline is unacceptable.

Example:
- Aircraft control systems
- Pacemakers

### Soft Real-Time OS
Occasional deadline misses are acceptable.

Example:
- Video streaming
- Online gaming

## Advantages
- Predictable behavior.
- High reliability.

## Disadvantages
- Expensive development.
- Complex scheduling.

## Interview Point
RTOS guarantees response within a predefined time limit.

---

# Final Interview Answer

Types of Operating Systems:
1. Single Process OS
2. Batch OS
3. Multiprogramming OS
4. Multitasking OS
5. Multiprocessing OS
6. Distributed OS
7. Real-Time OS

---

# Most Frequently Asked Interview Questions

1. Difference between Multiprogramming and Multitasking?
2. Difference between Multitasking and Multiprocessing?
3. What is RTOS?
4. Difference between Hard RTOS and Soft RTOS?
5. Why was Multiprogramming introduced?
# Program vs Process vs Thread

## Program

A program is just a file containing instructions stored in disk. It is not doing anything until we run it.

Examples:
- chrome.exe
- code.exe
- spotify.exe

These files are simply sitting in storage waiting to be executed.

So we can say:

Program = Instructions stored in disk.

Think of it like a recipe book lying on a table. The instructions are there but nobody is cooking yet.

---

## Process

When we run a program, OS loads it into RAM and starts executing it.

At this point the program becomes a process.

For example:

chrome.exe stored in SSD -> Program

Double click Chrome -> OS loads it into RAM -> Chrome Process is created.

Therefore,

Program + Execution = Process

Unlike programs, processes are active because they are actually using CPU and memory.

A process contains:
- Program code
- Data
- Stack
- Heap
- CPU registers
- Program counter

One important thing to remember:

A single program can create multiple processes.

Example:

Opening Chrome three times creates:
- Chrome Process 1
- Chrome Process 2
- Chrome Process 3

even though the program is still the same chrome.exe file.

---

## Thread

A process may need to do many things at the same time.

For example, while using Chrome:

- one task loads the webpage,
- another downloads files,
- another plays videos,
- another handles mouse clicks.

If only one execution path existed, Chrome would freeze frequently.

To solve this problem, a process is divided into smaller execution units called threads.

You can think of threads as workers inside a company.

Chrome = Company (Process)

Workers inside company:
- Download Worker
- Rendering Worker
- Network Worker
- UI Worker

These workers are threads.

All threads share resources of the process such as:
- Code section
- Heap memory
- Data section

But every thread keeps its own:
- Stack
- Registers
- Program Counter

Because threads share resources, creating a thread is much cheaper than creating a process.

That is why threads are called:

"Lightweight Processes"

---

## Quick Revision

Program:
Instructions stored in disk.

Process:
Program currently executing in memory.

Thread:
Smallest execution unit inside a process.

---

## One Line Interview Answer

Program -> Stored instructions.

Process -> Program under execution.

Thread -> Smallest unit of execution inside a process.
# Process Memory Layout

Whenever we run a program, the OS loads it into RAM and creates a process.

The OS does **not** place everything randomly in memory. Instead, it divides the process memory into different sections, and each section has a specific purpose.

A process memory layout looks like this:

+--------------------+
| Stack              |  ↓ Grows Down
+--------------------+
|                    |
| Heap               |  ↑ Grows Up
|                    |
+--------------------+
| Data Segment       |
+--------------------+
| Code Segment       |
+--------------------+

Each section stores different types of data.

---

# 1. Code Segment (Text Segment)

The Code Segment stores the actual instructions of our program.

Whatever functions we write are converted into machine code after compilation and stored here.

Example:

```cpp
int add(int a, int b){
    return a + b;
}
```

The compiled instructions of the `add()` function are stored in the Code Segment.

### Characteristics
- Stores executable instructions.
- Usually read-only so the program cannot accidentally modify its own code.
- If two processes run the same program (e.g., two Chrome windows), they can share the same code segment to save memory.

**Easy way to remember:**
Think of it as the **instruction manual** of the program.

---

# 2. Data Segment

The Data Segment stores **global variables** and **static variables** because they exist throughout the program's execution.

Example:

```cpp
int x = 10;
static int y = 20;
```

Both `x` and `y` are stored in the Data Segment.

The Data Segment has two parts:

### (a) Initialized Data Segment

Stores variables that already have a value.

Example:

```cpp
int marks = 100;
```

### (b) BSS (Uninitialized Data Segment)

Stores variables that are declared but not initialized.

Example:

```cpp
int count;
```

The OS automatically initializes such variables to **0**.

**Easy way to remember:**
Data Segment stores variables that live for the **entire lifetime of the program**.

---

# 3. Heap

Heap memory is used whenever memory is allocated **dynamically** during program execution.

Whenever we use:

- `new`
- `malloc()`
- `calloc()`
- `realloc()`

the memory comes from the Heap.

Example:

```cpp
int* arr = new int[100];
```

The array of 100 integers is stored in the Heap.

### Characteristics
- Used for dynamic memory allocation.
- Memory remains allocated until we explicitly free it.
- Grows upward.
- Slightly slower than Stack because the OS has to manage it.

Example:

```cpp
delete[] arr;
```

If we forget to free heap memory, it leads to a **Memory Leak**.

**Easy way to remember:**
Heap is like renting a room—you keep it until you return it.

---

# 4. Stack

The Stack stores temporary data needed while functions are executing.

It stores:
- Local variables
- Function parameters
- Return addresses
- Function call information

Example:

```cpp
void fun() {
    int x = 10;
}
```

The variable `x` is stored in the Stack.

When the function finishes, `x` is automatically removed.

### Characteristics
- Managed automatically by the compiler/OS.
- Very fast access.
- Grows downward.
- Memory is automatically freed when the function ends.

**Easy way to remember:**
Stack is like a notebook used during work. Once the work is finished, the notes are erased automatically.

---

# Complete Example

```cpp
int globalVar = 100;

int main() {

    int localVar = 10;

    int* ptr = new int(20);

    return 0;
}
```

Memory allocation:

- `globalVar` → Data Segment
- `main()` instructions → Code Segment
- `localVar` → Stack
- `ptr` (pointer variable) → Stack
- Value `20` created using `new` → Heap

---

# Why do Heap and Stack grow in opposite directions?

Stack grows downward.

Heap grows upward.

This design allows both to use the available memory efficiently.

As long as they don't meet, memory can be used safely.

If they collide, the program usually crashes due to memory overflow.

---

# Real-Life Analogy

Imagine a company.

📖 **Code Segment** → Company's rule book (instructions).

📂 **Data Segment** → Permanent employee records.

📦 **Heap** → Temporary storage room. Things remain there until someone removes them.

📝 **Stack** → Daily work notes. Once the day's work is finished, the notes are thrown away automatically.

---

# Interview Questions

### Q1. What are the four sections of Process Memory Layout?

- Code Segment
- Data Segment
- Heap
- Stack

---

### Q2. Where are local variables stored?

Stack.

---

### Q3. Where are global and static variables stored?

Data Segment.

---

### Q4. Where is dynamically allocated memory stored?

Heap.

---

### Q5. Why is Stack faster than Heap?

Because Stack memory is managed automatically, whereas Heap memory requires dynamic allocation and deallocation.

---

### Q6. What happens if Heap memory is not freed?

It causes a **Memory Leak**, where memory remains occupied even though it is no longer needed.

---

# Quick Revision

| Memory Section | Stores |
|---------------|--------------------------------|
| Code Segment | Program instructions/functions |
| Data Segment | Global & Static variables |
| Heap | Dynamically allocated memory (`new`, `malloc`) |
| Stack | Local variables, function calls, parameters |

---

# One-Line Summary

Whenever a program starts executing, the OS creates a process and divides its memory into four parts:
- **Code** for instructions,
- **Data** for global/static variables,
- **Heap** for dynamic memory,
- **Stack** for local variables and function calls.