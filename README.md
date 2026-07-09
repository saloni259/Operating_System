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
# Process Control Block (PCB)

## What is PCB?

Whenever a program starts running, it becomes a **process**.

Now imagine multiple processes are running at the same time:

- Chrome
- VS Code
- Spotify
- WhatsApp

The OS has to manage all of them.

To do this, the OS creates a **PCB (Process Control Block)** for every process.

Simply remember:

> **PCB is the identity card + record book of a process.**

It stores all the important information about that process so that the OS can manage it properly.

---

## Why do we need PCB?

Let's understand with an example.

Suppose Chrome is running.

After a few milliseconds, the OS gives the CPU to VS Code.

Now Chrome is paused.

Later, when Chrome gets the CPU again, how will it know from where to continue?

Without saving its current information, Chrome would have to start from the beginning every time.

To avoid this, before removing Chrome from the CPU, the OS saves its current state inside the PCB.

Later, when Chrome gets the CPU again, the OS reads the PCB and resumes execution from exactly where it stopped.

So,

**PCB helps the OS pause and resume a process without losing its progress.**

---

# What information does PCB store?

## 1. Process ID (PID)

Every process gets a unique ID.

It helps the OS identify processes.

Example:

Chrome → PID = 101

VS Code → PID = 102

Spotify → PID = 103

Think of PID like your **college roll number**.

---

## 2. Process State

PCB stores the current state of the process.

Possible states are:

- New
- Ready
- Running
- Waiting
- Terminated

Example:

If Chrome is downloading a file, it may be in the **Waiting** state.

The OS checks the PCB and knows that Chrome should not get the CPU until the download operation is ready.

---

## 3. Program Counter (PC)

This is one of the most important fields in PCB.

It stores the address of the **next instruction** that the process should execute.

Example:

```cpp
int a = 10;
int b = 20;
int c = a + b;
cout << c;
```

Suppose the CPU has already executed the first two statements.

The Program Counter stores the address of:

```cpp
int c = a + b;
```

When the process runs again, execution starts from this instruction instead of starting from the beginning.

---

## 4. CPU Registers

While a process is running, the CPU stores temporary values in registers.

During context switching, these register values are saved in the PCB.

When the process gets the CPU again, these values are restored.

This allows the process to continue normally without losing calculations.

---

## 5. CPU Scheduling Information

The scheduler needs some information before deciding which process should run next.

PCB stores details such as:

- Process Priority
- Queue Number
- Scheduling Information

Example:

Chrome Priority = 5

Spotify Priority = 2

The scheduler may give the CPU to Chrome first because it has higher priority.

---

## 6. Memory Management Information

PCB stores information about the memory used by the process.

This helps the OS know where the process is located in RAM.

Examples:

- Base Address
- Limit Register
- Page Table
- Segment Table

We will study these in detail in Memory Management.

---

## 7. Accounting Information

The OS also keeps some statistics about the process.

Examples:

- CPU time used
- Process creation time
- User ID

This information is useful for monitoring and system management.

Example:

When Task Manager shows:

Chrome → CPU Usage = 15%

this information comes from accounting data.

---

## 8. I/O Status Information

PCB stores information related to input/output devices.

Examples:

- Which files are open?
- Which printer is being used?
- Which devices are allocated?

Example:

If Chrome is downloading a file, PCB may store:

- Network Card in use
- File "movie.mp4" is open

---

# PCB and Context Switching

This is the most important use of PCB.

Suppose Chrome is running.

Now the OS wants to execute VS Code.

The OS performs three steps:

### Step 1
Save Chrome's current information into its PCB.

Information saved:
- Program Counter
- Registers
- Process State
- Other details

### Step 2
Load VS Code's PCB.

Restore:
- Registers
- Program Counter

### Step 3
VS Code starts executing.

Later, when Chrome gets the CPU again, the OS loads Chrome's PCB and execution continues from exactly where it stopped.

This entire process is called **Context Switching**.

Without PCB, context switching would not be possible.

---

# Where is PCB stored?

All PCBs are stored in a table maintained by the Operating System.

This table is called the **Process Table**.

Example:

Process Table

PID 101 → Chrome PCB

PID 102 → VS Code PCB

PID 103 → Spotify PCB

Whenever the OS needs information about a process, it simply checks its PCB.

---

# Life Cycle of PCB

1. Process is created.
2. OS creates a PCB.
3. PCB is updated while the process runs.
4. When the process finishes, its PCB is deleted.

So,

**One Process = One PCB**

---

# Real-Life Analogy

Think of a hospital.

Every patient has a file containing:

- Patient ID
- Current condition
- Medicines
- Reports
- Doctor's notes

Doctors never remember everything by heart.

They simply open the patient's file.

Similarly,

Every process has a PCB.

Whenever the OS needs information, it checks the PCB.

---

# Quick Revision

- Every process has its own PCB.
- PCB is created when the process is created.
- PCB is deleted when the process terminates.
- PCB stores all important information about the process.
- PCB is essential for context switching.

---

# Interview Questions

### What is PCB?

PCB (Process Control Block) is a data structure maintained by the Operating System that stores all the information required to manage a process.

---

### Why is PCB needed?

PCB allows the OS to:
- Manage processes.
- Perform context switching.
- Pause and resume processes.
- Keep track of process information.

---

### How many PCBs are created?

One PCB is created for every process.

Example:

5 running processes → 5 PCBs.

---

### Which PCB field is most important during context switching?

- Program Counter
- CPU Registers
- Process State

These are saved before switching and restored when the process gets the CPU again.

---

# Easy Way to Remember

Think of PCB as the **personal file of a process**.

Just like every student has a file in the college office containing all important details,

every process has a PCB containing all the information required by the Operating System.
# Process States

## What is a Process State?

When a program starts executing, it becomes a **process**.

A process is not always running. Sometimes it is waiting for CPU, sometimes waiting for an I/O operation, and sometimes it has already finished.

The **current condition of a process** at any particular time is called its **Process State**.

In simple words,

> Process State tells us **what the process is doing right now.**

The Operating System stores the current state of every process inside its **PCB (Process Control Block).**

---

# Why do we need Process States?

Suppose you open three applications:

- Chrome
- VS Code
- Spotify

A single CPU cannot execute all three at the same time.

So the OS keeps changing their states and decides:

- Which process should run?
- Which process should wait?
- Which process has finished?

Without process states, the OS would not know what each process is doing.

---

# Types of Process States

Every process generally passes through **five states** during its lifetime.

```
New
 ↓
Ready
 ↓
Running
 ↙      ↘
Waiting  Terminated
   ↓
 Ready
```

Let's understand each one.

---

# 1. New State

A process enters the **New State** immediately after it is created.

At this stage:

- OS creates the Process Control Block (PCB).
- Memory is allocated.
- Required resources are prepared.

The process is **not executing yet** because it has not received the CPU.

### Example

Suppose you double-click Chrome.

The OS starts creating the Chrome process.

At this moment, Chrome is in the **New State**.

### Easy Analogy

Think of a student entering the examination hall.

The student has entered the hall but hasn't started writing yet.

This is similar to the **New State**.

---

# 2. Ready State

After the process is created, it moves to the **Ready State**.

In this state:

- Memory has been allocated.
- PCB has been created.
- All required resources are available.

The process is simply waiting for the CPU.

Remember:

**Ready means waiting only for CPU.**

### Example

Suppose there are three processes:

- Chrome
- VS Code
- Spotify

CPU is currently executing Chrome.

VS Code and Spotify are ready to execute but are waiting for the CPU.

So they are in the **Ready State**.

### Important Point

All ready processes are kept in a **Ready Queue**.

The CPU Scheduler selects one process from this queue and gives it the CPU.

---

# 3. Running State

When the CPU is allocated to a process, it enters the **Running State**.

This means the CPU is currently executing the instructions of that process.

### Example

If Chrome is currently using the CPU, then Chrome is in the **Running State**.

### Important Point

In a system with a single CPU,

**only one process can be in the Running State at a time.**

---

# 4. Waiting State (Blocked State)

Sometimes a process cannot continue its execution because it is waiting for some external event.

Common reasons are:

- Reading a file
- Waiting for keyboard input
- Waiting for network response
- Waiting for printer
- Waiting for disk operation

Instead of wasting CPU time, the OS moves that process to the **Waiting State**.

### Example

Suppose Chrome is downloading a file.

It sends a request to the disk.

Until the disk sends the data, Chrome cannot continue.

So Chrome enters the **Waiting State**.

Meanwhile, the CPU starts executing another process.

### Important Point

Waiting means:

**Waiting for an event (mostly I/O).**

It is **NOT waiting for CPU.**

---

# Ready State vs Waiting State

This is one of the most common interview questions.

### Ready State

The process has everything it needs except the CPU.

It is simply waiting for CPU allocation.

Example:

A student is sitting inside the exam hall with a pen and question paper.

He is only waiting for the teacher to say "Start."

---

### Waiting State

The process is waiting for some event.

Even if CPU becomes free, it still cannot execute.

Example:

A student forgot his pen.

Even if the teacher says "Start writing," he cannot write until he gets a pen.

---

# 5. Terminated State

When a process finishes its work, it enters the **Terminated State**.

The OS releases:

- Memory
- CPU
- Open files
- Devices
- PCB

The process is completely removed from the system.

### Example

You close Chrome.

The Chrome process ends.

Its memory is released and its PCB is deleted.

---

# How does a Process move from one State to another?

### New → Ready

The process is created and all required resources are allocated.

Now it is ready to execute.

---

### Ready → Running

The CPU Scheduler selects the process and allocates the CPU.

Execution starts.

---

### Running → Waiting

The process requests an I/O operation.

Example:

- Reading a file
- Waiting for network
- Printing a document

The process cannot continue, so it enters the Waiting State.

---

### Waiting → Ready

The required event (usually I/O) is completed.

Now the process is ready to execute again.

It goes back to the Ready Queue.

---

### Running → Ready

Sometimes the process is still executing, but its CPU time (time quantum) finishes.

The OS removes the CPU from that process and puts it back into the Ready Queue.

This happens in Round Robin Scheduling.

---

### Running → Terminated

The process completes its execution.

The OS releases all resources and deletes the PCB.

---

# Can a Process move directly from Waiting to Running?

**No.**

This is an important interview question.

When an I/O operation finishes,

the process first enters the **Ready State**.

Only after the CPU Scheduler selects it again does it enter the Running State.

So the sequence is:

Waiting → Ready → Running

Never:

Waiting → Running

---

# Real-Life Analogy

Imagine visiting a hospital.

### New

You enter the hospital.

### Ready

You complete registration and wait for your turn.

### Running

The doctor is examining you.

### Waiting

The doctor asks you to get an X-ray.

You wait for the report.

### Ready

The report is ready.

Now you're waiting outside the doctor's cabin again.

### Running

Doctor calls you and continues the check-up.

### Terminated

Treatment is complete and you leave the hospital.

---

# Quick Revision

- **New** → Process is being created.
- **Ready** → Waiting only for CPU.
- **Running** → CPU is executing the process.
- **Waiting** → Waiting for an external event (mostly I/O).
- **Terminated** → Process has finished execution.

---

# Interview Questions

### What is a Process State?

A Process State tells the current status of a process during its execution.

---

### What are the five basic process states?

- New
- Ready
- Running
- Waiting (Blocked)
- Terminated

---

### Difference between Ready and Waiting State?

**Ready State:**
Process is waiting only for CPU.

**Waiting State:**
Process is waiting for an event such as disk, keyboard, printer, or network.

---

### Can multiple processes be in Running State?

- Single CPU → Only one process.
- Multi-core CPU → One process per CPU core.

---

### Can a process directly move from Waiting to Running?

No.

It always follows:

Waiting → Ready → Running

---

# Easy Way to Remember

Think of the life of a student in an exam.

- Enter Exam Hall → New
- Waiting for Question Paper → Ready
- Writing Exam → Running
- Waiting for Extra Answer Sheet → Waiting
- Exam Finished → Terminated

This analogy makes it easy to remember all process states.
# Process Queues and Process Schedulers

After understanding **Process States**, the next question is:

> If there are hundreds of processes in the system, how does the OS manage all of them?

The answer is **Process Queues**.

The OS groups processes based on their current state. Instead of keeping them randomly, it places them into different queues. This makes process management much easier.

---

# What is a Process Queue?

A Process Queue is simply a list of processes waiting for a particular resource or event.

For example,
- Some processes are waiting to enter memory.
- Some are waiting for the CPU.
- Some are waiting for an I/O operation.

The OS keeps moving processes from one queue to another depending on their current state.

---

# Types of Process Queues

There are mainly three queues:

1. Job Queue
2. Ready Queue
3. Waiting Queue (Device Queue)

Let's understand each one.

---

# 1. Job Queue

## What is it?

The Job Queue contains all newly created processes that are **not yet loaded into RAM**.

These processes are still stored in secondary memory (Hard Disk/SSD).

Since RAM is limited, every process cannot enter memory immediately.

The OS decides which process should be loaded first.

### Example

Suppose you try to open:

- Chrome
- VS Code
- Spotify
- Photoshop
- Android Studio

But your RAM has space for only three applications.

The remaining applications have to wait.

These waiting processes form the **Job Queue**.

### Easy Analogy

Imagine a cinema hall.

The hall is full.

People are standing outside waiting for someone to leave.

Those people represent the **Job Queue**.

### Important Points

- Stored in secondary memory.
- Waiting to enter RAM.
- Controlled by the Long-Term Scheduler.

---

# 2. Ready Queue

## What is it?

The Ready Queue contains processes that are already loaded into RAM and are ready to execute.

The only thing they are waiting for is the CPU.

Remember this line:

**Ready = Waiting only for CPU.**

### Example

Suppose RAM contains:

- Chrome
- VS Code
- Spotify

CPU is currently executing Chrome.

VS Code and Spotify are ready but waiting for CPU.

Therefore they are in the Ready Queue.

### Easy Analogy

Imagine students sitting outside an interview room.

They have completed registration and are fully prepared.

They are simply waiting for their turn.

That is exactly the Ready Queue.

### Important Points

- Processes are already in RAM.
- Waiting only for CPU.
- Managed by the Short-Term Scheduler.

---

# 3. Waiting Queue (Device Queue)

## What is it?

Sometimes a process cannot continue execution because it needs an external event.

Examples:
- Reading a file
- Writing to disk
- Waiting for printer
- Waiting for internet
- Waiting for keyboard input

Such processes are moved to the Waiting Queue.

### Example

Suppose Chrome is downloading a movie.

It sends a request to the disk.

Until the disk sends the data, Chrome cannot continue.

Instead of wasting CPU time, the OS moves Chrome to the Waiting Queue and gives the CPU to another process.

Once the download is ready, Chrome moves back to the Ready Queue.

### Easy Analogy

You order food at a restaurant.

Now you're waiting for the food to arrive.

You cannot start eating even if a table is empty.

Similarly, a waiting process cannot execute until its event is completed.

### Important Points

- Waiting for an event, not CPU.
- Mostly waits for I/O operations.
- After the event finishes, it moves back to the Ready Queue.

---

# Process Flow

A process usually moves like this:

```
Job Queue
     │
     ▼
Ready Queue
     │
     ▼
Running
  │       │
  │       ▼
  │   Terminated
  ▼
Waiting Queue
     │
     ▼
Ready Queue
```

Try to remember this flow because it is asked frequently in interviews.

---

# Process Schedulers

Now the question is:

Who moves processes from one queue to another?

The answer is:

**Schedulers**

A Scheduler is a part of the Operating System that decides which process should move next.

There are three schedulers.

---

# 1. Long-Term Scheduler (Job Scheduler)

## Work

Moves processes from:

Job Queue → Ready Queue

In other words,

It selects which processes should enter RAM.

### Why is it needed?

RAM is limited.

If the OS loads every process into memory, the system will become slow.

So the Long-Term Scheduler carefully selects processes.

### Example

100 processes are waiting on the disk.

RAM has space for only 20.

The Long-Term Scheduler selects 20 processes and loads them into memory.

### Important Points

- Works on Job Queue.
- Runs less frequently.
- Controls the Degree of Multiprogramming (number of processes in RAM).

---

# 2. Short-Term Scheduler (CPU Scheduler)

## Work

Moves processes from:

Ready Queue → Running

It decides which process gets the CPU.

### Example

Ready Queue contains:

- Chrome
- VS Code
- Spotify

The CPU Scheduler selects Chrome.

Chrome enters the Running State.

### Important Points

- Works on Ready Queue.
- Runs very frequently.
- Fastest scheduler because CPU decisions happen continuously.

---

# 3. Medium-Term Scheduler

## Work

Temporarily removes processes from RAM and stores them on disk.

This process is called **Swapping**.

Later, when memory becomes available, the process is brought back into RAM.

### Why is it needed?

Sometimes RAM becomes full.

Instead of crashing the system, the OS temporarily removes some processes.

### Example

RAM = 8 GB

Running processes require 10 GB.

The OS temporarily moves Spotify to disk.

Later, when memory is available, Spotify is loaded back into RAM.

### Important Points

- Performs Swapping.
- Helps manage memory efficiently.
- Improves overall system performance.

---

# Comparison of Schedulers

| Scheduler | Main Work |
|-----------|-----------|
| Long-Term Scheduler | Moves processes from Disk → RAM |
| Short-Term Scheduler | Gives CPU to a process |
| Medium-Term Scheduler | Swaps processes between RAM and Disk |

---

# Quick Revision

### Job Queue
- Processes are on Disk.
- Waiting to enter RAM.

### Ready Queue
- Processes are in RAM.
- Waiting only for CPU.

### Waiting Queue
- Processes are waiting for I/O or some event.

### Long-Term Scheduler
- Job Queue → Ready Queue

### Short-Term Scheduler
- Ready Queue → Running

### Medium-Term Scheduler
- Performs Swapping.

---

# Interview Questions

### What is a Process Queue?

A Process Queue is a collection of processes waiting for a particular resource or event.

---

### Difference between Job Queue and Ready Queue?

**Job Queue**
- Stored on Disk.
- Waiting to enter RAM.

**Ready Queue**
- Already in RAM.
- Waiting only for CPU.

---

### Which scheduler is the fastest?

Short-Term Scheduler, because it runs whenever the CPU becomes free.

---

### Which scheduler controls the Degree of Multiprogramming?

Long-Term Scheduler.

---

### Which scheduler performs Swapping?

Medium-Term Scheduler.

---

# Easy Way to Remember

Think of a hospital.

- **Job Queue** → Patients waiting outside the hospital.
- **Ready Queue** → Patients sitting outside the doctor's cabin.
- **Running** → Patient is with the doctor.
- **Waiting Queue** → Patient has gone for an X-ray or blood test.
- **Terminated** → Patient's treatment is complete.

The schedulers are like hospital staff:

- **Long-Term Scheduler** admits patients into the hospital.
- **Short-Term Scheduler** sends the next patient to the doctor.
- **Medium-Term Scheduler** temporarily shifts patients out if the hospital becomes overcrowded.

This analogy makes the entire concept very easy to remember.
# Context Switching

## What is Context Switching?

A CPU can execute only **one process at a time** (assuming a single CPU system).

But in our computer, many applications run together like:
- Chrome
- VS Code
- Spotify
- WhatsApp

It looks like all of them are running simultaneously, but actually the OS keeps switching the CPU from one process to another very quickly.

This switching is called **Context Switching**.

In simple words,

> **Context Switching means saving the current process and loading another process so the CPU can execute it.**

---

# What is "Context"?

Before understanding Context Switching, we need to know what **Context** means.

Context is all the information required to restart a process from the exact point where it stopped.

For example,

Suppose Chrome is executing:

```cpp
int a = 10;
int b = 20;
int c = a + b;
cout << c;
```

If Chrome has already executed the first two lines and the OS switches the CPU to VS Code, Chrome should not start again from the first line.

The OS saves Chrome's current information.

Later, when Chrome gets the CPU again, it continues from:

```cpp
int c = a + b;
```

This saved information is called the **Context** of the process.

---

# Where is Context Stored?

The context of every process is stored inside its **PCB (Process Control Block).**

Some important information stored in PCB is:

- Program Counter (next instruction to execute)
- CPU Registers
- Process State
- Stack Pointer
- Scheduling Information
- Memory Information

Whenever a process is paused, this information is saved in its PCB.

---

# Why do we need Context Switching?

Imagine there are three processes:

- Chrome
- VS Code
- Spotify

If the CPU keeps executing only Chrome,

VS Code and Spotify will never run.

To give every process a chance to execute, the OS keeps switching the CPU between them.

Without Context Switching:
- No multitasking.
- Poor CPU sharing.
- Bad user experience.

---

# How does Context Switching happen?

Suppose Chrome is currently running.

Now its time quantum finishes.

The OS wants to execute VS Code.

The following steps happen:

### Step 1

The OS saves Chrome's current information into its PCB.

It saves things like:
- Program Counter
- Registers
- Process State

Now Chrome is paused.

---

### Step 2

The CPU Scheduler selects VS Code from the Ready Queue.

---

### Step 3

The OS loads VS Code's saved information from its PCB.

It restores:
- Program Counter
- Registers
- Stack Pointer

---

### Step 4

CPU starts executing VS Code.

Later, when Chrome gets the CPU again, its PCB is loaded and execution continues from exactly where it stopped.

---

# What information is saved during Context Switching?

The OS mainly saves:

- Program Counter
- CPU Registers
- Process State
- Stack Pointer
- Scheduling Information
- Memory Information

This information is enough to restart the process without losing progress.

---

# Context Switching Overhead

Context Switching takes time.

During switching, the CPU is **not executing any user program**.

It is only:
- Saving one process.
- Loading another process.

This extra time is called **Context Switching Overhead**.

Since no useful work is done during this time, it slightly reduces system performance.

---

# Advantages of Context Switching

- Makes multitasking possible.
- Improves CPU utilization.
- Gives every process a chance to execute.
- Improves system responsiveness.

---

# Disadvantages of Context Switching

- Takes extra time.
- Frequent switching reduces performance.
- CPU does no useful work during switching.

---

# Process Context Switching vs Thread Context Switching

## Process Context Switching

Switching CPU from one process to another.

Example:

Chrome → VS Code

Since both processes have different memory spaces, the OS has to switch:
- Registers
- Program Counter
- Memory Mapping
- Page Tables

Therefore, it is **slower**.

---

## Thread Context Switching

Switching between threads of the same process.

Example:

Chrome Download Thread → Chrome Render Thread

Since threads share the same memory, only a few things need to be switched:
- Registers
- Program Counter
- Stack

Therefore, Thread Context Switching is **faster**.

---

# Real-Life Analogy

Imagine you're reading two books.

You read Book A up to page 50.

Before starting Book B, you place a bookmark in Book A.

Now you read Book B.

Later, when you return to Book A, you don't start from page 1.

You continue from page 50 using the bookmark.

Here,

- Book = Process
- Bookmark = Context
- Changing books = Context Switching

---

# Quick Revision

- CPU executes only one process at a time.
- OS switches CPU between processes very quickly.
- This switching is called Context Switching.
- Context = Current state of a process.
- Context is stored in PCB.
- During Context Switching:
  - Current process state is saved.
  - Next process state is loaded.
- Context Switching takes extra time, called **Context Switching Overhead**.

---

# Common Mistakes

❌ Context Switching means two processes run together.

✅ Wrong.

Only one process runs at a time on a single CPU.
The CPU is simply switched very quickly.

---

❌ Context Switching happens only when a process finishes.

✅ Wrong.

It can happen when:
- Time quantum expires.
- Process requests I/O.
- Higher priority process arrives.
- Interrupt occurs.

---

# Interview Questions

### What is Context Switching?

Context Switching is the process of saving the current state of one process and restoring the state of another process so that the CPU can switch between them.

---

### Why is PCB important in Context Switching?

Because PCB stores all the information required to pause and later resume a process.

---

### What is Context Switching Overhead?

The extra time spent saving and restoring process information during Context Switching.

---

### Which is faster: Process Context Switching or Thread Context Switching?

Thread Context Switching is faster because threads share the same memory space.

---

# Easy Way to Remember

**Save → Switch → Restore**

1. Save the current process.
2. Switch the CPU.
3. Restore the next process.

This is Context Switching.
# Zombie Process, Orphan Process and Daemon Process

Before learning these concepts, we need to understand one thing.

Whenever a process creates another process:

- The process that creates it is called the **Parent Process**.
- The newly created process is called the **Child Process**.

Example:

```
Chrome (Parent)
   │
   ├── Download Process (Child)
   ├── Render Process (Child)
   └── Network Process (Child)
```

One parent process can create multiple child processes.

---

# 1. Zombie Process

## What is a Zombie Process?

A Zombie Process is a process that has **already finished execution**, but its entry is still present in the **Process Table (PCB)** because the parent process has not collected its exit status.

In simple words,

> **The process is dead, but its PCB is still alive.**

---

## Why does Zombie Process occur?

Whenever a child process finishes, it informs the OS that it has completed its work.

But the OS does not immediately delete the PCB.

It waits for the parent process to read the child's exit status using `wait()` or `waitpid()`.

If the parent does not do this, the child process becomes a Zombie Process.

---

## Example

Suppose:

```
Parent Process
      │
      └── Child Process
```

Child finishes execution.

Normally:

```
Child finishes
      ↓
Parent calls wait()
      ↓
OS deletes PCB
```

But if Parent never calls `wait()`:

```
Child finishes
      ↓
PCB remains in Process Table
      ↓
Zombie Process
```

---

## Does Zombie Process use CPU?

No.

The process has already completed.

It does **not** use:
- CPU
- RAM
- Disk

Only a small PCB entry remains inside the Process Table.

---

## Why are Zombie Processes bad?

One Zombie Process is not a problem.

But if many Zombie Processes keep accumulating, they occupy entries in the Process Table.

Eventually, the OS may not be able to create new processes.

---

## How can Zombie Process be removed?

The parent process should call:

```c
wait();
```

or

```c
waitpid();
```

After that, the OS removes the PCB.

If the parent itself terminates, Linux automatically assigns the Zombie to the **init/systemd** process, which collects the exit status and removes it.

---

## Easy Analogy

Imagine a student has graduated from college.

He has left the college.

But the college office has not removed his record yet.

Student → Gone

Record → Still exists

This is exactly what a Zombie Process is.

---

# 2. Orphan Process

## What is an Orphan Process?

An Orphan Process is a child process whose **parent process terminates before the child finishes execution**.

In simple words,

> **Parent dies first, child is still running.**

---

## Example

Suppose:

```
Parent
   │
   └── Child
```

Now,

Parent crashes.

But Child is still executing.

The child has no parent now.

This child becomes an **Orphan Process**.

---

## What happens to the Orphan Process?

The OS does not kill the child.

Instead, it assigns a new parent.

In Linux, the new parent is usually:

- `init`
- `systemd`

The child continues executing normally.

---

## Does Orphan Process use CPU?

Yes.

Unlike Zombie Processes, Orphan Processes are still running.

They continue to use:
- CPU
- Memory
- Other resources

until they finish execution.

---

## Easy Analogy

Imagine a child whose parents are no longer alive.

The government appoints a legal guardian.

Similarly, the OS assigns a new parent (`init/systemd`) to the child process.

---

# 3. Daemon Process

## What is a Daemon Process?

A Daemon Process is a background process that continuously runs and provides services to other processes.

It usually starts automatically when the system boots.

Users normally do not interact with it directly.

---

## Why do we need Daemon Processes?

Many system services should always be available.

Examples:

- Printing
- Internet
- Bluetooth
- Email
- Web Server

Instead of starting these services every time, the OS keeps them running in the background.

---

## Example

Suppose you print a document.

The flow is:

```
User
   ↓
Print Command
   ↓
Printer Daemon
   ↓
Printer
```

The Printer Daemon receives the request and sends it to the printer.

---

## Examples of Daemon Processes

- Print Service
- Bluetooth Service
- Network Manager
- Web Server (Apache/Nginx)
- SSH Service

---

## Characteristics of Daemon Process

- Runs in the background.
- Starts automatically during system boot.
- No user interaction.
- Provides system services.
- Keeps running until the system shuts down.

---

## Easy Analogy

Think of a security guard in a shopping mall.

Even if no customers are present, the guard keeps doing his duty.

Similarly, a Daemon Process keeps running in the background waiting for requests.

---

# Zombie Process vs Orphan Process

| Zombie Process | Orphan Process |
|---------------|----------------|
| Child has finished execution | Child is still executing |
| Parent is alive | Parent has terminated |
| PCB still exists | Child gets a new parent (`init/systemd`) |
| Uses only PCB entry | Uses CPU and Memory |
| Removed using `wait()` | Continues execution normally |

---

# Zombie Process vs Daemon Process

| Zombie Process | Daemon Process |
|---------------|----------------|
| Dead process | Background service process |
| Does no useful work | Performs useful system services |
| Temporary state | Runs continuously |
| Undesirable | Necessary for the OS |

---

# Quick Revision

### Zombie Process
- Child has finished execution.
- Parent has not collected exit status.
- PCB still exists.
- Does not use CPU.
- Removed using `wait()`.

---

### Orphan Process
- Parent terminates first.
- Child is still running.
- Adopted by `init/systemd`.
- Continues execution normally.

---

### Daemon Process
- Background process.
- Starts during system boot.
- Provides system services.
- Runs continuously.

---

# Interview Questions

### What is a Zombie Process?

A terminated process whose PCB still exists because the parent process has not collected its exit status.

---

### What is an Orphan Process?

A child process whose parent terminates before the child finishes execution.

---

### What is a Daemon Process?

A background process that continuously provides system services.

---

### Does a Zombie Process use CPU?

No.

Only its PCB entry remains.

---

### Who adopts an Orphan Process?

In Linux, `init` or `systemd`.

---

### Which function removes a Zombie Process?

`wait()` or `waitpid()`.

---

# Easy Way to Remember

### Zombie Process

**Dead Child + Living Parent**

Child has finished.

Parent has not collected the exit status.

---

### Orphan Process

**Dead Parent + Living Child**

Parent has terminated.

Child continues execution.

---

### Daemon Process

**Background Worker**

Always running.

Always ready to provide services.
# CPU Scheduling (Introduction)

Before learning scheduling algorithms like FCFS, SJF, Priority, or Round Robin, we first need to understand **what CPU Scheduling is** and **why it is needed**.

---

# Why do we need CPU Scheduling?

A computer may have many processes running at the same time.

Example:
- Chrome
- VS Code
- Spotify
- WhatsApp

But in a single CPU system, the CPU can execute **only one process at a time**.

Now the question is,

**Which process should get the CPU first?**

The Operating System needs a way to decide this.

This decision-making process is called **CPU Scheduling**.

---

# What is CPU Scheduling?

CPU Scheduling is the process of selecting **one process from the Ready Queue** and allocating the CPU to it.

In simple words,

> CPU Scheduling decides **which ready process should execute next.**

The process selected by the scheduler moves from the **Ready State** to the **Running State**.

---

# Who performs CPU Scheduling?

CPU Scheduling is performed by the **Short-Term Scheduler**, also called the **CPU Scheduler**.

Its job is simple:

```
Ready Queue
     │
     ▼
CPU Scheduler
     │
     ▼
Running Process
```

Whenever the CPU becomes free, the scheduler selects one process from the Ready Queue.

---

# Why is CPU Scheduling important?

If CPU Scheduling did not exist,

the OS would not know which process should execute first.

Some processes might never get CPU time, while others could keep using the CPU forever.

A good scheduling algorithm helps in:

- Better CPU utilization.
- Faster execution.
- Fair allocation of CPU.
- Better user experience.

---

# Goals of CPU Scheduling

A good scheduling algorithm tries to achieve the following goals.

---

## 1. Maximum CPU Utilization

CPU is the most important resource in a computer.

The scheduler should keep the CPU busy as much as possible.

Example:

Suppose Process P1 is waiting for a disk operation.

Instead of keeping the CPU idle, the OS gives the CPU to Process P2.

This increases CPU utilization.

---

## 2. Maximum Throughput

Throughput means the number of processes completed in a given amount of time.

Formula:

Throughput = Number of Completed Processes / Time

Example:

System A completes 20 processes in one minute.

System B completes 10 processes in one minute.

System A has better throughput.

Higher throughput means better system performance.

---

## 3. Minimum Turnaround Time (TAT)

Turnaround Time tells us how much total time a process spends in the system.

Formula:

Turnaround Time = Completion Time − Arrival Time

Example:

Arrival Time = 2 sec

Completion Time = 12 sec

Turnaround Time = 10 sec

Smaller Turnaround Time means processes finish faster.

---

## 4. Minimum Waiting Time

Waiting Time is the time a process spends waiting in the Ready Queue before getting the CPU.

Example:

A process arrives at 10:00 AM.

It gets the CPU at 10:05 AM.

Waiting Time = 5 minutes.

A good scheduler always tries to reduce Waiting Time.

---

## 5. Minimum Response Time

Response Time is the time taken by the system to give the **first response** to the user.

Example:

When you click Chrome,

if the Chrome window opens immediately, the Response Time is good.

This is very important for interactive applications.

---

## 6. Fairness

Every process should get a fair chance to execute.

One process should not keep the CPU forever.

Otherwise, other processes may keep waiting indefinitely.

This situation is called **Starvation**, which we will study later.

---

# When does CPU Scheduling happen?

The scheduler runs whenever the CPU becomes free or needs to be assigned to another process.

Common situations are:

### 1. Running → Waiting

Example:

The running process requests a file from the disk.

Since it cannot continue, the CPU becomes free.

The scheduler selects another process.

---

### 2. Running → Ready

Example:

The process has used its allotted time (Time Quantum).

The OS moves it back to the Ready Queue and selects another process.

---

### 3. Waiting → Ready

Example:

A disk operation is completed.

The waiting process becomes ready again.

Now it joins the Ready Queue.

---

### 4. Process Terminates

When a process finishes execution, the CPU becomes free.

The scheduler selects the next process from the Ready Queue.

---

# Types of CPU Scheduling

There are two types of CPU Scheduling.

---

## 1. Non-Preemptive Scheduling

Once a process gets the CPU, it keeps the CPU until:

- It finishes execution, or
- It goes into the Waiting State.

The OS cannot forcibly take the CPU away.

### Example

P1 needs 10 seconds.

P2 needs 2 seconds.

If P1 gets the CPU first,

P2 has to wait until P1 finishes.

---

## 2. Preemptive Scheduling

In Preemptive Scheduling, the OS can take the CPU away from a running process whenever needed.

This usually happens when:

- Time Quantum expires.
- A higher-priority process arrives.

### Example

Suppose P1 is running.

Suddenly, a high-priority process P2 arrives.

The OS pauses P1 and immediately gives the CPU to P2.

---

# Difference Between Preemptive and Non-Preemptive Scheduling

| Non-Preemptive | Preemptive |
|---------------|------------|
| CPU cannot be taken away until the process finishes or waits for I/O. | CPU can be taken away whenever required. |
| Simpler to implement. | More complex. |
| Less Context Switching. | More Context Switching. |
| Lower overhead. | Higher overhead. |
| Poor response time. | Better response time. |

---

# Common CPU Scheduling Algorithms

The Operating System can use different algorithms to decide which process gets the CPU.

The most important algorithms are:

- FCFS (First Come First Serve)
- SJF (Shortest Job First)
- SRTF (Shortest Remaining Time First)
- Priority Scheduling
- Round Robin
- Multilevel Queue Scheduling
- Multilevel Feedback Queue Scheduling

We will study each algorithm separately with numerical examples.

---

# Quick Revision

- CPU can execute only one process at a time.
- CPU Scheduling decides which Ready process gets the CPU.
- CPU Scheduling is performed by the Short-Term Scheduler.
- Main goals:
  - Maximum CPU Utilization
  - Maximum Throughput
  - Minimum Turnaround Time
  - Minimum Waiting Time
  - Minimum Response Time
  - Fairness

---

# Interview Questions

### What is CPU Scheduling?

CPU Scheduling is the process of selecting one process from the Ready Queue and allocating the CPU to it.

---

### Which scheduler performs CPU Scheduling?

The Short-Term Scheduler (CPU Scheduler).

---

### Why do we need CPU Scheduling?

Because multiple processes compete for a single CPU, and the OS needs a rule to decide which process should execute next.

---

### What are the goals of CPU Scheduling?

- Maximum CPU Utilization
- Maximum Throughput
- Minimum Turnaround Time
- Minimum Waiting Time
- Minimum Response Time
- Fairness

---

### What is the difference between Preemptive and Non-Preemptive Scheduling?

**Non-Preemptive:** Once a process gets the CPU, it cannot be interrupted.

**Preemptive:** The OS can interrupt a running process and allocate the CPU to another process.

---

# Easy Way to Remember

Imagine there is only one cashier in a bank.

Many customers are waiting in line.

The cashier has to decide **who should be served next**.

That decision is exactly like **CPU Scheduling**.

The customers are processes, the cashier is the CPU, and the bank manager deciding the order is the CPU Scheduler.
# FCFS (First Come First Serve) Scheduling

FCFS is the simplest CPU Scheduling algorithm.

As the name suggests,

**First Come → First Serve**

The process that arrives first in the Ready Queue gets the CPU first.

No priority is given to any process.

No process can jump the queue.

---

# Why do we need FCFS?

Suppose three processes are waiting for the CPU.

```
P1
P2
P3
```

The CPU can execute only one process at a time.

Now the OS has to decide:

**Which process should execute first?**

FCFS follows a very simple rule:

> The process that arrives first gets the CPU first.

---

# What is FCFS?

FCFS (First Come First Serve) is a **Non-Preemptive CPU Scheduling Algorithm** in which processes are executed according to their arrival time.

The process that enters the Ready Queue first gets the CPU first.

---

# Why is FCFS called Non-Preemptive?

Once a process gets the CPU,

the OS cannot take the CPU back until:

- the process finishes execution, or
- the process goes into Waiting State (I/O).

Example:

```
P1 = 10 sec
P2 = 2 sec
```

If P1 starts first,

P2 has to wait for the complete 10 seconds.

Even though P2 needs only 2 seconds,

the OS cannot interrupt P1.

Therefore FCFS is a **Non-Preemptive Scheduling Algorithm**.

---

# How does FCFS work?

Let's take an example.

| Process | Arrival Time | Burst Time |
|----------|--------------|------------|
| P1 | 0 | 5 |
| P2 | 1 | 3 |
| P3 | 2 | 2 |

### Step 1: Arrange processes according to Arrival Time

```
P1 → P2 → P3
```

### Step 2: Execute them in the same order

```
P1 → P2 → P3
```

### Step 3: Draw the Gantt Chart

```
0        5        8       10
|   P1   |   P2   |   P3   |
```

---

# Completion Time (CT)

Completion Time means the time at which a process finishes execution.

From the Gantt Chart,

| Process | CT |
|----------|----|
| P1 | 5 |
| P2 | 8 |
| P3 | 10 |

---

# Turnaround Time (TAT)

Turnaround Time tells us how much total time a process spends in the system.

Formula:

```
TAT = Completion Time - Arrival Time
```

Calculation:

P1 = 5 - 0 = 5

P2 = 8 - 1 = 7

P3 = 10 - 2 = 8

| Process | TAT |
|----------|-----|
| P1 | 5 |
| P2 | 7 |
| P3 | 8 |

---

# Waiting Time (WT)

Waiting Time is the time a process waits in the Ready Queue before getting the CPU.

Formula:

```
WT = Turnaround Time - Burst Time
```

Calculation:

P1 = 5 - 5 = 0

P2 = 7 - 3 = 4

P3 = 8 - 2 = 6

| Process | WT |
|----------|----|
| P1 | 0 |
| P2 | 4 |
| P3 | 6 |

---

# Average Waiting Time

Formula:

```
Average WT = (Sum of all Waiting Times) / Number of Processes
```

Calculation:

```
(0 + 4 + 6) / 3

= 10 / 3

= 3.33
```

---

# Average Turnaround Time

Formula:

```
Average TAT = (Sum of all Turnaround Times) / Number of Processes
```

Calculation:

```
(5 + 7 + 8) / 3

= 20 / 3

= 6.67
```

---

# Advantages of FCFS

### 1. Easy to understand

FCFS is the simplest scheduling algorithm.

---

### 2. Easy to implement

Processes are simply executed according to their arrival time.

---

### 3. Fair Scheduling

Every process gets the CPU in the same order in which it arrives.

No process is skipped.

---

### 4. No Starvation

Every process will eventually get CPU time.

No process waits forever.

---

# Disadvantages of FCFS

### 1. Convoy Effect (Most Important)

This is the biggest disadvantage of FCFS.

Example:

| Process | Burst Time |
|----------|------------|
| P1 | 20 |
| P2 | 2 |
| P3 | 1 |

Execution:

```
P1 → P2 → P3
```

Although P2 and P3 require very little CPU time,

they must wait until P1 finishes.

This unnecessary waiting is called the **Convoy Effect**.

Think of a slow truck on a one-lane road.

All vehicles behind it must also move slowly.

---

### 2. High Waiting Time

If a long process comes first,

all smaller processes have to wait.

This increases the average waiting time.

---

### 3. Poor Response Time

Small or interactive processes cannot start quickly if a large process is already running.

Therefore FCFS is not suitable for interactive systems.

---

# Where is FCFS used?

FCFS is mainly used where simplicity is more important than speed.

Examples:

- Printer Queue
- Batch Processing Systems
- Simple Job Scheduling

---

# Quick Revision

- FCFS = First Come First Serve.
- Processes are executed according to Arrival Time.
- It is a Non-Preemptive Scheduling Algorithm.
- Once CPU is allocated, it cannot be taken back until the process finishes or waits for I/O.
- Biggest disadvantage = Convoy Effect.
- No Starvation because every process eventually gets CPU time.

---

# Interview Questions

### What is FCFS Scheduling?

FCFS is a Non-Preemptive Scheduling Algorithm in which the process that arrives first gets the CPU first.

---

### Why is FCFS called Non-Preemptive?

Because once a process gets the CPU, the OS cannot interrupt it until it finishes execution or enters the Waiting State.

---

### What is the Convoy Effect?

When a long process executes before shorter processes, forcing them to wait for a long time, it is called the Convoy Effect.

---

### Does Starvation occur in FCFS?

No.

Every process gets CPU time according to its arrival order.

---

### Is FCFS suitable for interactive systems?

No.

Because small processes may have to wait behind long processes, leading to poor response time.

---

# Easy Way to Remember

Imagine standing in a queue at a railway ticket counter.

The person who comes first gets the ticket first.

Nobody can skip the queue.

This is exactly how FCFS Scheduling works.
# Shortest Job First (SJF) Scheduling

After studying FCFS, we noticed one major problem.

If a long process comes first, all the small processes have to wait for a long time. This increases the average waiting time.

To solve this problem, the Operating System introduced **Shortest Job First (SJF)** Scheduling.

---

# What is SJF Scheduling?

SJF (Shortest Job First) is a **Non-Preemptive CPU Scheduling Algorithm**.

In this algorithm, the process having the **smallest Burst Time** is executed first.

In simple words,

> **The process that requires the least CPU time gets the CPU first.**

Unlike FCFS, SJF does **not** consider arrival order (when all processes are available). It mainly considers the Burst Time.

---

# What is Burst Time?

Burst Time is the amount of CPU time required by a process to complete its execution.

Example:

| Process | Burst Time |
|----------|------------|
| P1 | 6 |
| P2 | 2 |
| P3 | 8 |
| P4 | 3 |

Here,

P2 has the smallest Burst Time.

So, P2 will execute first.

---

# Why is SJF called Non-Preemptive?

Once a process starts executing,

the OS will not stop it until it finishes.

Even if another process with a smaller Burst Time arrives later,

the currently running process continues its execution.

Only after it finishes does the scheduler choose the next shortest job.

---

# How does SJF work?

Consider the following processes:

| Process | Arrival Time | Burst Time |
|----------|--------------|------------|
| P1 | 0 | 6 |
| P2 | 0 | 2 |
| P3 | 0 | 8 |
| P4 | 0 | 3 |

Since all processes arrive at the same time,

we compare only their Burst Time.

Execution order:

```
P2 → P4 → P1 → P3
```

### Gantt Chart

```
0      2      5      11      19
| P2 | P4 | P1 | P3 |
```

---

# Completion Time (CT)

Completion Time means the time at which a process finishes execution.

| Process | CT |
|----------|----|
| P2 | 2 |
| P4 | 5 |
| P1 | 11 |
| P3 | 19 |

---

# Turnaround Time (TAT)

Turnaround Time tells us the total time spent by a process in the system.

Formula:

```
TAT = Completion Time - Arrival Time
```

Calculation:

P2 = 2 - 0 = 2

P4 = 5 - 0 = 5

P1 = 11 - 0 = 11

P3 = 19 - 0 = 19

| Process | TAT |
|----------|-----|
| P2 | 2 |
| P4 | 5 |
| P1 | 11 |
| P3 | 19 |

---

# Waiting Time (WT)

Waiting Time is the time a process waits in the Ready Queue before getting the CPU.

Formula:

```
WT = Turnaround Time - Burst Time
```

Calculation:

P2 = 2 - 2 = 0

P4 = 5 - 3 = 2

P1 = 11 - 6 = 5

P3 = 19 - 8 = 11

| Process | WT |
|----------|----|
| P2 | 0 |
| P4 | 2 |
| P1 | 5 |
| P3 | 11 |

---

# Average Waiting Time

Formula:

```
Average WT = (Sum of Waiting Times) / Number of Processes
```

Calculation:

```
(0 + 2 + 5 + 11) / 4

= 18 / 4

= 4.5
```

This is smaller than FCFS, which is why SJF is considered a better scheduling algorithm in terms of average waiting time.

---

# Why does SJF give Minimum Average Waiting Time?

SJF executes small processes first.

As a result:

- Small processes finish quickly.
- Most processes spend less time waiting.
- Average Waiting Time becomes minimum.

This is one of the biggest advantages of SJF and is a very common interview question.

---

# What if Arrival Times are Different?

Suppose:

| Process | Arrival Time | Burst Time |
|----------|--------------|------------|
| P1 | 0 | 6 |
| P2 | 2 | 2 |
| P3 | 4 | 1 |

At time **0**, only P1 has arrived.

Even though P2 has a smaller Burst Time,

the CPU cannot execute it because it has not arrived yet.

So,

P1 starts first.

After P1 finishes, the scheduler chooses the shortest Burst Time among the processes that are available.

**Important:**

SJF always selects the shortest job from the processes that have already arrived.

---

# Advantages of SJF

### 1. Minimum Average Waiting Time

Among all Non-Preemptive Scheduling Algorithms, SJF gives the minimum average waiting time.

---

### 2. Better Turnaround Time

Since shorter jobs finish earlier, the average turnaround time is also reduced.

---

### 3. Better CPU Performance

Processes spend less time waiting, improving overall system efficiency.

---

# Disadvantages of SJF

### 1. Starvation (Most Important)

Suppose there is one long process:

```
P1 = 20 sec
```

Now small processes keep arriving:

```
P2 = 1 sec
P3 = 2 sec
P4 = 1 sec
P5 = 2 sec
```

The scheduler keeps selecting the shortest process.

The long process (P1) keeps waiting and may never get the CPU.

This situation is called **Starvation**.

---

### 2. Burst Time Must Be Known

The scheduler must know the Burst Time before execution.

In real operating systems, it is difficult to know exactly how long a process will run.

Because of this, pure SJF is rarely used directly.

---

# FCFS vs SJF

| FCFS | SJF |
|------|-----|
| Executes process based on Arrival Time | Executes process based on Burst Time |
| Simple to implement | Slightly more complex |
| Higher Average Waiting Time | Lower Average Waiting Time |
| No Starvation | Starvation may occur |
| Fair based on arrival | Long processes may wait longer |

---

# Quick Revision

- SJF = Shortest Job First.
- It is a **Non-Preemptive** Scheduling Algorithm.
- Process with the smallest Burst Time gets the CPU first.
- Gives the minimum Average Waiting Time.
- Biggest disadvantage = Starvation.
- Burst Time should be known before execution.

---

# Interview Questions

### What is SJF Scheduling?

SJF is a Non-Preemptive CPU Scheduling Algorithm in which the process with the smallest Burst Time is executed first.

---

### Why is SJF better than FCFS?

Because SJF gives the minimum Average Waiting Time.

---

### What is the biggest disadvantage of SJF?

Starvation and the requirement of knowing Burst Time in advance.

---

### Is SJF Preemptive?

No.

SJF is Non-Preemptive.

The Preemptive version of SJF is called **Shortest Remaining Time First (SRTF).**

---

### Can Starvation occur in SJF?

Yes.

Long processes may wait indefinitely if smaller processes continue to arrive.

---

# Easy Way to Remember

Imagine four customers standing at a supermarket billing counter.

- Customer A → 20 items
- Customer B → 2 items
- Customer C → 1 item
- Customer D → 3 items

If the cashier serves the customers with fewer items first, more customers leave quickly and the queue becomes shorter.

This is exactly how **Shortest Job First (SJF)** Scheduling works.

# Shortest Remaining Time First (SRTF) Scheduling

After studying SJF, we learned that it always executes the process with the shortest Burst Time.

But SJF has one limitation.

Once a process starts executing, it cannot be interrupted, even if another shorter process arrives later.

To solve this problem, **Shortest Remaining Time First (SRTF)** Scheduling was introduced.

---

# What is SRTF?

SRTF (Shortest Remaining Time First) is the **Preemptive version of SJF**.

Instead of comparing the total Burst Time, it compares the **Remaining Burst Time** of all available processes.

Whenever a new process arrives, the OS checks:

**"Does the new process require less CPU time than the remaining time of the currently running process?"**

If the answer is **Yes**, the CPU is immediately taken away from the current process and given to the new one.

This process is called **Preemption**.

---

# What is Remaining Time?

Remaining Time means the CPU time that is still required to complete a process.

Formula:

```
Remaining Time = Burst Time − Executed Time
```

Example:

A process has Burst Time = 10 sec.

It has already executed for 4 sec.

Remaining Time:

```
10 − 4 = 6 sec
```

SRTF always compares these remaining times.

---

# Why is SRTF called Preemptive?

Because the Operating System can interrupt a running process whenever a new process arrives with a smaller Remaining Time.

Example:

Suppose:

```
P1 (Remaining Time = 7 sec) → Running
```

Now,

```
P2 arrives (Burst Time = 3 sec)
```

Since

```
3 < 7
```

the OS immediately stops P1 and gives the CPU to P2.

Later, after P2 finishes, P1 continues from where it stopped.

---

# How does SRTF work?

Let's understand with an example.

| Process | Arrival Time | Burst Time |
|----------|--------------|------------|
| P1 | 0 | 8 |
| P2 | 1 | 4 |
| P3 | 2 | 2 |

### Step 1

Time = 0

Only P1 has arrived.

CPU starts executing P1.

Remaining Time of P1 becomes:

```
7
```

---

### Step 2

Time = 1

P2 arrives.

Compare:

```
P1 Remaining = 7

P2 Burst = 4
```

Since P2 has less remaining time,

CPU switches from P1 to P2.

This is called **Preemption**.

---

### Step 3

Time = 2

P3 arrives.

Compare:

```
P2 Remaining = 3

P3 Burst = 2
```

Again,

P3 is shorter.

CPU immediately switches to P3.

---

### Step 4

P3 finishes.

Now compare:

```
P1 Remaining = 7

P2 Remaining = 3
```

P2 is shorter.

So CPU executes P2.

---

### Step 5

P2 finishes.

Only P1 remains.

CPU executes P1 until completion.

---

# Gantt Chart

```
0     1      2      4      7             14

| P1 | P2 | P3 | P2 |      P1      |
```

Notice that the CPU keeps switching whenever a shorter process arrives.

This is the biggest difference between SJF and SRTF.

---

# Why is SRTF better than SJF?

In SJF,

once a process starts, it cannot be interrupted.

In SRTF,

if a shorter process arrives, it immediately gets the CPU.

Because of this,

- Small processes finish faster.
- Response Time improves.
- Average Waiting Time becomes even smaller.

---

# Advantages of SRTF

### 1. Better Response Time

Small processes get CPU quickly.

This makes the system more responsive.

---

### 2. Lower Average Waiting Time

Compared to FCFS and even SJF (when arrivals differ), SRTF generally provides a lower average waiting time.

---

### 3. Good for Interactive Systems

Interactive applications require quick responses.

SRTF helps provide faster responses to newly arriving short processes.

---

# Disadvantages of SRTF

### 1. Too Many Context Switches

Every time a shorter process arrives,

the OS performs Context Switching.

Frequent Context Switching increases overhead and reduces performance.

---

### 2. Starvation

Suppose there is one long process.

If small processes keep arriving,

the long process may never get enough CPU time to finish.

This problem is called **Starvation**.

---

### 3. Burst Time Must Be Known

The scheduler needs to know the Burst Time in advance.

In real systems, it is difficult to predict exactly how much CPU time a process will require.

---

# SJF vs SRTF

| SJF | SRTF |
|------|------|
| Non-Preemptive | Preemptive |
| Compares Burst Time | Compares Remaining Time |
| Running process cannot be interrupted | Running process can be interrupted |
| Fewer Context Switches | More Context Switches |
| Slightly higher Response Time | Better Response Time |

---

# FCFS vs SRTF

| FCFS | SRTF |
|------|------|
| Executes based on Arrival Time | Executes based on Remaining Time |
| Non-Preemptive | Preemptive |
| Convoy Effect occurs | Convoy Effect is reduced |
| Higher Waiting Time | Lower Waiting Time |

---

# Quick Revision

- SRTF = Shortest Remaining Time First.
- It is the **Preemptive version of SJF**.
- CPU always executes the process with the smallest Remaining Time.
- A running process can be interrupted if a shorter process arrives.
- Gives better Response Time and lower Average Waiting Time.
- Biggest disadvantages:
  - Starvation
  - High Context Switching Overhead
  - Burst Time must be known.

---

# Interview Questions

### What is SRTF Scheduling?

SRTF is the Preemptive version of SJF in which the process with the shortest Remaining Time gets the CPU.

---

### Why is SRTF called Preemptive?

Because the OS can interrupt the currently running process if another process arrives with a shorter Remaining Time.

---

### What is compared in SRTF?

Remaining Burst Time.

---

### Can Starvation occur in SRTF?

Yes.

Long processes may keep waiting if smaller processes continue arriving.

---

### Which is better: SJF or SRTF?

SRTF usually gives better Response Time and lower Waiting Time because it allows preemption.

However, it causes more Context Switching.

---

# Easy Way to Remember

Imagine a doctor is treating a patient who needs **20 minutes**.

Suddenly, another patient arrives who needs only **2 minutes**.

The doctor pauses the first patient, treats the second patient quickly, and then returns to the first one.

This is exactly how **Shortest Remaining Time First (SRTF)** Scheduling works.
# Priority Scheduling

After studying FCFS, SJF and SRTF, we learned that processes can be selected based on Arrival Time or Burst Time.

But in real life, not every process is equally important.

Some processes are more critical than others.

For example:

- Keyboard Input
- Antivirus
- System Processes
- Emergency Tasks

These processes should get CPU before normal background processes.

To solve this problem, **Priority Scheduling** is used.

---

# What is Priority Scheduling?

Priority Scheduling is a CPU Scheduling Algorithm in which the process having the **highest priority** gets the CPU first.

Instead of comparing Arrival Time or Burst Time, the scheduler compares the **Priority** of processes.

The process with the highest priority is selected for execution.

---

# Important Point

Different operating systems follow different priority numbering systems.

Some systems consider:

```
Priority = 1
Highest Priority
```

Some systems consider:

```
Priority = 10
Highest Priority
```

👉 Therefore, always read the question carefully before solving numerical problems.

---

# Types of Priority Scheduling

There are two types:

1. Non-Preemptive Priority Scheduling
2. Preemptive Priority Scheduling

---

# 1. Non-Preemptive Priority Scheduling

In this scheduling algorithm, once a process gets the CPU, it continues execution until it finishes or enters the Waiting State.

Even if another process with higher priority arrives, the currently running process is **not interrupted**.

### Example

| Process | Arrival | Burst | Priority |
|----------|---------|-------|----------|
| P1 | 0 | 6 | 3 |
| P2 | 2 | 2 | 1 |

(Assume smaller number means higher priority.)

At time 0,

Only P1 is available.

So P1 starts executing.

At time 2,

P2 arrives with higher priority.

But since this is **Non-Preemptive**, P1 continues execution.

After P1 finishes,

P2 gets the CPU.

---

# 2. Preemptive Priority Scheduling

In this scheduling algorithm, the OS continuously checks whether a process with higher priority has arrived.

If yes,

the currently running process is interrupted immediately and the higher priority process gets the CPU.

### Example

Using the same processes:

| Process | Arrival | Burst | Priority |
|----------|---------|-------|----------|
| P1 | 0 | 6 | 3 |
| P2 | 2 | 2 | 1 |

Time = 0

P1 starts execution.

Time = 2

P2 arrives.

Since P2 has higher priority,

the OS pauses P1 and gives CPU to P2.

After P2 finishes,

P1 resumes execution from where it stopped.

This is called **Preemptive Priority Scheduling**.

---

# What happens if two processes have the same priority?

This is a common interview question.

If two processes have equal priority,

the OS generally follows **FCFS (First Come First Serve)**.

Example:

| Process | Priority |
|----------|----------|
| P1 | 2 |
| P2 | 2 |

If P1 arrived first,

P1 will execute before P2.

---

# Advantages of Priority Scheduling

### 1. Important processes execute first.

Critical tasks get CPU immediately.

---

### 2. Suitable for Real-Time Systems.

Processes like:

- Emergency Tasks
- System Services
- Device Drivers

can be assigned higher priority.

---

### 3. Flexible Scheduling.

The OS can assign priorities according to system requirements.

---

# Disadvantages of Priority Scheduling

## 1. Starvation (Most Important)

This is the biggest disadvantage.

Suppose:

```
P1 → Low Priority

P2 → High Priority

P3 → High Priority

P4 → High Priority
```

Every time a high-priority process arrives,

the scheduler selects it.

P1 keeps waiting.

If this continues, P1 may never get the CPU.

This situation is called **Starvation**.

---

# What is Starvation?

Starvation is a situation in which a process keeps waiting indefinitely because higher priority processes continue getting the CPU.

In simple words,

> **A process waits forever and never gets a chance to execute.**

---

# How to solve Starvation?

The solution is **Aging**.

---

# What is Aging?

Aging is a technique used to prevent Starvation.

In Aging, the priority of a waiting process is gradually improved over time.

As the waiting time increases,

its priority also increases.

Eventually,

it becomes high enough to get the CPU.

### Example

Initially,

```
P1 Priority = 10
```

After waiting:

```
10 → 9 → 8 → 7 → 6 → 5 ...
```

Finally,

P1 gets the CPU.

Thus, Starvation is avoided.

---

# Real-Life Analogy

Imagine a hospital.

Emergency patients are treated first.

Normal patients wait.

But if a normal patient has been waiting for a long time,

the doctor eventually treats them.

This gradual increase in importance is similar to **Aging**.

---

# Difference Between Preemptive and Non-Preemptive Priority Scheduling

| Non-Preemptive | Preemptive |
|----------------|------------|
| Running process cannot be interrupted. | Running process can be interrupted. |
| Fewer Context Switches. | More Context Switches. |
| Simpler to implement. | Better response for high-priority processes. |

---

# Difference Between SJF and Priority Scheduling

| SJF | Priority Scheduling |
|-----|----------------------|
| CPU is allocated based on Burst Time. | CPU is allocated based on Priority. |
| Shortest process executes first. | Highest priority process executes first. |
| Starvation may occur. | Starvation may occur. |

---

# Quick Revision

- Priority Scheduling selects the process with the highest priority.
- It can be **Preemptive** or **Non-Preemptive**.
- If two processes have the same priority, FCFS is usually used.
- Biggest disadvantage = **Starvation**.
- Starvation is prevented using **Aging**.

---

# Interview Questions

### What is Priority Scheduling?

Priority Scheduling is a CPU Scheduling Algorithm in which the process with the highest priority gets the CPU first.

---

### What are the two types of Priority Scheduling?

- Non-Preemptive Priority Scheduling
- Preemptive Priority Scheduling

---

### What is Starvation?

Starvation is a situation where a process waits indefinitely because higher-priority processes continuously get the CPU.

---

### How can Starvation be prevented?

By using **Aging**, which gradually increases the priority of waiting processes.

---

### What happens if two processes have the same priority?

The OS generally schedules them using **FCFS**.

---

### Which type gives better response time?

Preemptive Priority Scheduling, because a high-priority process can immediately interrupt the currently running process.

---

# Easy Way to Remember

Think of a hospital.

- Emergency patient → High Priority → Treated first.
- Normal patient → Low Priority → Waits.
- If the normal patient keeps waiting for a long time, the doctor finally treats them.

Emergency treatment = **Priority Scheduling**

Giving a chance to the waiting patient later = **Aging**

This analogy helps remember both **Priority Scheduling** and **Starvation** together.
# Round Robin (RR) Scheduling

After studying FCFS, SJF, SRTF and Priority Scheduling, we learned that some algorithms may cause **Starvation** or poor **Response Time**.

To solve these problems, the Operating System uses **Round Robin (RR) Scheduling**.

It is one of the most commonly used CPU Scheduling algorithms in modern Time-Sharing Operating Systems.

---

# What is Round Robin Scheduling?

Round Robin (RR) is a **Preemptive CPU Scheduling Algorithm**.

In this algorithm, every process gets the CPU for a fixed amount of time called the **Time Quantum (Time Slice).**

If the process finishes within the Time Quantum, it leaves the CPU.

Otherwise, the OS interrupts it and places it at the end of the Ready Queue.

The next process then gets the CPU.

In simple words,

> Every process gets an equal chance to execute for a fixed amount of time.

---

# Why do we need Round Robin?

Suppose three processes are waiting.

| Process | Burst Time |
|----------|------------|
| P1 | 20 |
| P2 | 3 |
| P3 | 2 |

If FCFS is used,

```
P1 → P2 → P3
```

P2 and P3 must wait until P1 finishes.

This gives poor Response Time.

Round Robin solves this problem by giving each process a small amount of CPU time before moving to the next process.

---

# What is Time Quantum?

Time Quantum is the **maximum amount of CPU time** given to a process in one turn.

Example:

```
Time Quantum = 2 ms
```

This means every process can execute for at most **2 ms** before the CPU is assigned to another process.

Time Quantum is the most important concept in Round Robin Scheduling.

---

# Why is Round Robin called Preemptive?

Round Robin is a **Preemptive Scheduling Algorithm** because the OS can interrupt a running process.

When the Time Quantum expires,

the OS immediately takes the CPU away from the running process.

If the process is not completed,

it is placed at the end of the Ready Queue.

The next process then gets the CPU.

---

# How does Round Robin work?

Example:

Time Quantum = **2**

| Process | Arrival Time | Burst Time |
|----------|--------------|------------|
| P1 | 0 | 5 |
| P2 | 0 | 4 |
| P3 | 0 | 2 |

Initially,

Ready Queue:

```
P1 → P2 → P3
```

### Step 1

CPU executes P1 for 2 units.

Remaining Burst Time:

```
5 − 2 = 3
```

P1 is moved to the end of the Ready Queue.

Queue becomes:

```
P2 → P3 → P1
```

---

### Step 2

CPU executes P2 for 2 units.

Remaining Burst Time:

```
4 − 2 = 2
```

P2 moves to the end.

Queue becomes:

```
P3 → P1 → P2
```

---

### Step 3

CPU executes P3.

Burst Time = 2

P3 completes execution.

Queue becomes:

```
P1 → P2
```

---

### Step 4

CPU executes P1 again.

Remaining Burst Time:

```
3 − 2 = 1
```

P1 moves to the end.

Queue becomes:

```
P2 → P1
```

---

### Step 5

CPU executes P2.

Remaining Burst Time:

```
2 − 2 = 0
```

P2 finishes.

Queue becomes:

```
P1
```

---

### Step 6

CPU executes P1.

Remaining Burst Time:

```
1 − 1 = 0
```

P1 also finishes.

---

# Gantt Chart

```
0     2     4     6     8     10    11

| P1 | P2 | P3 | P1 | P2 | P1 |
```

Observe that every process gets the CPU for only **2 units** before the next process gets a turn.

---

# Advantages of Round Robin

### 1. Fair Scheduling

Every process gets an equal opportunity to execute.

No process can occupy the CPU forever.

---

### 2. Better Response Time

Since every process gets CPU quickly,

users feel that all applications are running simultaneously.

This makes Round Robin suitable for interactive systems.

---

### 3. No Starvation

Every process eventually gets CPU time.

No process waits forever.

---

### 4. Suitable for Time-Sharing Systems

Many users can share the CPU efficiently because every process gets a fixed Time Quantum.

---

# Disadvantages of Round Robin

### 1. More Context Switching

Every Time Quantum expiry causes a Context Switch.

Frequent Context Switching increases overhead and reduces CPU efficiency.

---

### 2. Performance depends on Time Quantum

Choosing the correct Time Quantum is very important.

If it is too small or too large,

system performance decreases.

---

# Effect of Time Quantum

## Case 1: Time Quantum is too Small

Example:

```
Time Quantum = 1 ms
```

The CPU switches processes very frequently.

Result:

- More Context Switching
- Higher Overhead
- Lower Performance

---

## Case 2: Time Quantum is too Large

Example:

```
Time Quantum = 1000 ms
```

Most processes finish before the Time Quantum expires.

Round Robin behaves almost like **FCFS**.

Response Time becomes poor.

---

## Ideal Time Quantum

A good Time Quantum should be:

- Not too small
- Not too large

It should provide a balance between:

- Good Response Time
- Less Context Switching
- Better CPU Utilization

---

# Difference Between FCFS and Round Robin

| FCFS | Round Robin |
|------|-------------|
| Non-Preemptive | Preemptive |
| Executes one process completely | Executes each process for a fixed Time Quantum |
| No Time Quantum | Uses Time Quantum |
| Poor Response Time | Better Response Time |
| Simpler | Slightly more complex |

---

# Difference Between SJF and Round Robin

| SJF | Round Robin |
|------|-------------|
| Based on Burst Time | Based on Time Quantum |
| Lower Average Waiting Time | Better Response Time |
| Starvation possible | No Starvation |

---

# Where is Round Robin used?

Round Robin is commonly used in:

- Time-Sharing Operating Systems
- Interactive Systems
- Multi-user Systems

Examples:

- Linux
- UNIX
- Windows (combined with Priority Scheduling)

---

# Quick Revision

- Round Robin = Preemptive Scheduling Algorithm.
- Every process gets CPU for a fixed **Time Quantum**.
- If the process is incomplete, it goes to the end of the Ready Queue.
- Main advantage = Fair Scheduling.
- No Starvation.
- Main disadvantage = High Context Switching Overhead.
- Choosing the correct Time Quantum is very important.

---

# Interview Questions

### What is Round Robin Scheduling?

Round Robin is a Preemptive CPU Scheduling Algorithm in which every process gets CPU for a fixed Time Quantum.

---

### What is Time Quantum?

Time Quantum is the maximum CPU time allocated to a process in one turn.

---

### Why is Round Robin called Preemptive?

Because the OS interrupts the running process after the Time Quantum expires.

---

### What happens if the Time Quantum is too small?

- Too many Context Switches.
- High Overhead.
- Reduced Performance.

---

### What happens if the Time Quantum is too large?

Round Robin behaves almost like FCFS and Response Time becomes poor.

---

### Can Starvation occur in Round Robin?

No.

Every process eventually gets CPU time.

---

### Why is Round Robin suitable for Time-Sharing Systems?

Because every process gets a fair and equal opportunity to execute, providing quick response to all users.

---

# Easy Way to Remember

Imagine four friends sharing one cricket bat.

The rule is:

Each player can bat for **2 minutes**.

After 2 minutes, whether the player is out or not, the bat is passed to the next player.

Later, the first player gets another turn.

This is exactly how **Round Robin Scheduling** works.

Remember:

**Round Robin = Equal Time for Everyone.**