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
# Multilevel Queue (MLQ) Scheduling

After learning FCFS, SJF, SRTF, Priority Scheduling and Round Robin, we know that all these algorithms assume that every process is present in a single Ready Queue.

But in a real operating system, different types of processes have different requirements.

For example:

- Keyboard Input
- Mouse Events
- System Processes
- Browser
- Music Player
- Background Backup
- Antivirus Scan

All these processes should not be treated equally.

To solve this problem, the Operating System uses **Multilevel Queue (MLQ) Scheduling**.

---

# What is Multilevel Queue Scheduling?

Multilevel Queue (MLQ) Scheduling is a CPU Scheduling Algorithm in which the **Ready Queue is divided into multiple separate queues**.

Each queue contains a different category of processes.

Each queue can also use a different scheduling algorithm.

In simple words,

> Instead of keeping every process in one queue, the OS divides similar processes into different queues.

---

# Why do we need MLQ?

Suppose there is only one Ready Queue.

```
Ready Queue

Chrome

Keyboard Input

Video Rendering

Backup

Antivirus
```

If a long process starts executing,

important processes like Keyboard Input may have to wait.

This reduces system responsiveness.

So the OS creates separate queues.

Example:

```
Ready Queue

│

├── System Queue

├── Interactive Queue

└── Batch Queue
```

Now similar processes are grouped together.

---

# Types of Queues

A typical MLQ Scheduling system may have:

### 1. System Queue

Contains important system processes.

Examples:

- Device Drivers
- Operating System Services
- Interrupt Handling

Scheduling Algorithm:

Usually Priority Scheduling.

---

### 2. Interactive Queue

Contains applications that require quick response.

Examples:

- Chrome
- VS Code
- Calculator
- Browser

Scheduling Algorithm:

Usually Round Robin.

---

### 3. Batch Queue

Contains background jobs.

Examples:

- Backup
- Video Rendering
- File Compression
- Large Data Processing

Scheduling Algorithm:

Usually FCFS.

---

# How does MLQ Scheduling work?

The scheduler performs scheduling in two steps.

### Step 1

Select which queue should get the CPU.

### Step 2

Apply that queue's scheduling algorithm.

Example:

Suppose the Interactive Queue gets the CPU.

If the Interactive Queue uses Round Robin,

then Round Robin Scheduling is applied only to the processes inside that queue.

---

# CPU Allocation Between Queues

There are two common methods.

---

# 1. Fixed Priority Scheduling

Each queue is assigned a priority.

Example:

```
Queue 1 → Highest Priority

Queue 2 → Medium Priority

Queue 3 → Lowest Priority
```

The scheduler first checks Queue 1.

If Queue 1 has any process,

it gets the CPU.

Only when Queue 1 becomes empty does Queue 2 get CPU.

Similarly,

Queue 3 gets CPU only when both higher-priority queues are empty.

### Example

```
Queue 1

Keyboard Input
```

```
Queue 2

Chrome

VS Code
```

```
Queue 3

Backup
```

The CPU first executes Keyboard Input.

Chrome and Backup have to wait.

---

# Problem with Fixed Priority

If Queue 1 always contains processes,

Queue 2 and Queue 3 may never get CPU time.

This causes **Starvation**.

---

# 2. Time Slice Between Queues

Instead of always giving priority,

CPU time is divided among queues.

Example:

```
System Queue → 50%

Interactive Queue → 30%

Batch Queue → 20%
```

Every queue gets some CPU time.

This reduces the possibility of Starvation.

---

# Can a Process Move Between Queues?

This is one of the most important interview questions.

**No.**

Once a process enters a queue,

it remains in that queue until it finishes execution.

Example:

Chrome enters the Interactive Queue.

It cannot later move to the Batch Queue.

Queue assignment is fixed.

---

# Advantages of MLQ Scheduling

### 1. Better Organization

Processes are grouped according to their type.

This makes scheduling easier.

---

### 2. Different Scheduling Algorithms

Each queue can use the most suitable scheduling algorithm.

Example:

- Interactive → Round Robin
- Batch → FCFS
- System → Priority Scheduling

---

### 3. Fast Response for Important Processes

Interactive and system processes receive CPU quickly.

This improves user experience.

---

### 4. Efficient Process Management

Different categories of processes are managed independently.

---

# Disadvantages of MLQ Scheduling

### 1. Starvation

If Fixed Priority Scheduling is used,

lower-priority queues may never receive CPU time.

---

### 2. Fixed Queue Assignment

Once assigned,

a process cannot move to another queue.

Even if its behavior changes,

its queue remains the same.

---

### 3. Complex Implementation

Maintaining multiple queues is more complicated than maintaining a single Ready Queue.

---

# Difference Between MLQ and Round Robin

| Round Robin | Multilevel Queue |
|--------------|------------------|
| One Ready Queue | Multiple Ready Queues |
| Same scheduling algorithm for all processes | Different scheduling algorithms for different queues |
| Every process treated equally | Processes divided according to category |

---

# Difference Between Priority Scheduling and MLQ

| Priority Scheduling | Multilevel Queue |
|----------------------|------------------|
| One Ready Queue | Multiple Ready Queues |
| Priority among processes | Priority among queues and processes |
| Usually one scheduling algorithm | Different scheduling algorithm for each queue |

---

# Real-Life Analogy

Imagine a bank.

There are different counters:

- VIP Counter
- Regular Counter
- Business Counter

Every customer joins the appropriate counter.

VIP customers stay in the VIP queue.

Regular customers stay in the Regular queue.

Customers cannot switch between counters.

Each counter may have different service rules.

This is exactly how **Multilevel Queue Scheduling** works.

---

# Quick Revision

- MLQ divides the Ready Queue into multiple queues.
- Each queue contains a different category of processes.
- Different queues can use different scheduling algorithms.
- A process cannot move from one queue to another.
- CPU can be allocated using:
  - Fixed Priority
  - Time Slice
- Biggest disadvantage = Starvation (when Fixed Priority is used).

---

# Interview Questions

### What is Multilevel Queue Scheduling?

MLQ is a CPU Scheduling Algorithm in which the Ready Queue is divided into multiple queues based on process type or priority.

---

### Can different queues use different scheduling algorithms?

Yes.

Each queue can use its own scheduling algorithm.

Example:

- System → Priority Scheduling
- Interactive → Round Robin
- Batch → FCFS

---

### Can a process move from one queue to another?

No.

Once assigned, the process remains in the same queue until completion.

---

### What is the biggest disadvantage of MLQ?

Starvation of lower-priority queues and fixed queue assignment.

---

### How is CPU allocated between queues?

CPU can be allocated using:

- Fixed Priority Scheduling
- Time Slice Scheduling

---

# Easy Way to Remember

Think of an airport.

Passengers are divided into different queues:

- Business Class
- Economy Class
- Staff

Each queue follows different rules.

Passengers stay in their assigned queue.

Similarly,

**MLQ divides processes into different queues based on their category, and each queue can have its own scheduling algorithm.**
# Multilevel Feedback Queue (MLFQ) Scheduling

After studying Multilevel Queue (MLQ), we learned that the Ready Queue is divided into multiple queues.

However, MLQ has one major drawback.

Once a process enters a queue, it can **never move to another queue**, even if its behavior changes.

To solve this problem, the Operating System uses **Multilevel Feedback Queue (MLFQ) Scheduling**.

---

# What is Multilevel Feedback Queue (MLFQ)?

MLFQ is an advanced CPU Scheduling Algorithm in which the Ready Queue is divided into multiple queues.

Unlike MLQ,

**a process can move from one queue to another depending on its behavior.**

This movement of processes between queues is called **Feedback**.

In simple words,

> MLFQ continuously observes a process and changes its priority by moving it to different queues.

---

# Why is it called "Feedback Queue"?

The scheduler continuously watches the behavior of every process.

If a process uses the CPU for a long time,

its priority is reduced.

If a process waits for a long time,

its priority is increased.

This continuous observation and adjustment is called **Feedback**.

Hence the name **Multilevel Feedback Queue**.

---

# Structure of MLFQ

Suppose the Operating System creates three queues.

```
Queue 1 (Highest Priority)
Time Quantum = 2 ms

↓

Queue 2 (Medium Priority)
Time Quantum = 4 ms

↓

Queue 3 (Lowest Priority)
FCFS
```

Notice that:

- Higher-priority queues usually have smaller Time Quantum.
- Lower-priority queues have larger Time Quantum or may use FCFS.

---

# How does MLFQ work?

Suppose a new process P1 arrives.

Initially,

every new process enters the **highest-priority queue (Queue 1).**

### Step 1

P1 starts executing in Queue 1.

Time Quantum = 2 ms.

Suppose Burst Time = 8 ms.

After 2 ms,

P1 is still not completed.

Therefore,

P1 is moved (demoted) to Queue 2.

---

### Step 2

Queue 2 has Time Quantum = 4 ms.

P1 executes for another 4 ms.

Remaining Burst Time becomes:

```
8 − 2 − 4 = 2 ms
```

Since P1 is still incomplete,

it is moved to Queue 3.

---

### Step 3

Queue 3 uses FCFS.

P1 completes its remaining execution here.

---

# Process Movement

```
Queue 1
     │
     ▼
Queue 2
     │
     ▼
Queue 3
```

Unlike MLQ,

processes are allowed to move between queues.

This is the biggest feature of MLFQ.

---

# Promotion in MLFQ

Suppose a process waits for a very long time in Queue 3.

The scheduler increases its priority.

The process is promoted.

Example:

```
Queue 3

↓

Queue 2

↓

Queue 1
```

This promotion helps prevent **Starvation**.

---

# Demotion in MLFQ

If a process keeps using the CPU for a long time,

the scheduler assumes that it is a CPU-intensive process.

Its priority is reduced,

and it is moved to a lower-priority queue.

This allows short and interactive processes to get CPU quickly.

---

# Why is MLFQ considered intelligent?

MLFQ automatically identifies the type of process based on its behavior.

### Interactive Processes

Examples:

- Chrome
- Calculator
- VS Code
- Text Editor

These usually finish quickly.

Therefore,

they remain in higher-priority queues.

---

### CPU-Intensive Processes

Examples:

- Video Rendering
- File Compression
- Scientific Computation

These require CPU for a long time.

Therefore,

they gradually move to lower-priority queues.

---

# Advantages of MLFQ

### 1. Better Response Time

Interactive processes get CPU quickly.

---

### 2. Prevents Starvation

Processes waiting for a long time are promoted using Aging.

---

### 3. Adaptive Scheduling

Processes can change queues depending on their behavior.

Unlike MLQ,

queue assignment is not fixed.

---

### 4. Suitable for Mixed Workloads

MLFQ handles both:

- Interactive Processes
- CPU-intensive Processes

efficiently.

---

# Disadvantages of MLFQ

### 1. Complex Algorithm

MLFQ is much more complicated than FCFS, SJF or Round Robin.

---

### 2. Difficult to Configure

The Operating System has to decide:

- Number of Queues
- Time Quantum for each Queue
- Promotion Rules
- Demotion Rules

Choosing these values correctly is difficult.

---

### 3. More Scheduling Overhead

Maintaining multiple queues and frequently moving processes between them increases scheduling overhead.

---

# Difference Between MLQ and MLFQ

| MLQ | MLFQ |
|------|------|
| Fixed Queue Assignment | Dynamic Queue Assignment |
| Process cannot move between queues | Process can move between queues |
| Simpler | More complex |
| Higher chance of Starvation | Starvation is greatly reduced |
| No Feedback | Uses Feedback based on process behavior |

---

# Difference Between Round Robin and MLFQ

| Round Robin | MLFQ |
|--------------|------|
| Single Ready Queue | Multiple Ready Queues |
| Same Time Quantum for all processes | Different Time Quantum for different queues |
| No priority levels | Multiple priority levels |
| No queue movement | Processes move between queues |

---

# Real-Life Analogy

Imagine a school.

Students are divided into three classes:

- Advanced
- Intermediate
- Beginner

If a student performs poorly,

they move to a lower class.

If a student improves,

they move back to a higher class.

The teacher keeps changing their class based on their performance.

This is exactly how **Multilevel Feedback Queue Scheduling** works.

---

# Quick Revision

- MLFQ = Multilevel Feedback Queue Scheduling.
- Ready Queue is divided into multiple queues.
- Processes can move between queues.
- New processes always enter the highest-priority queue.
- Long-running processes move to lower-priority queues.
- Waiting processes may move to higher-priority queues using Aging.
- Better Response Time.
- Starvation is greatly reduced.
- More complex than MLQ.

---

# Interview Questions

### What is Multilevel Feedback Queue Scheduling?

MLFQ is a CPU Scheduling Algorithm in which multiple queues are used and processes can move between queues depending on their behavior.

---

### Why is it called Feedback Queue?

Because the scheduler continuously observes process behavior and changes its queue accordingly.

---

### What is the biggest difference between MLQ and MLFQ?

**MLQ:** Processes cannot move between queues.

**MLFQ:** Processes can move between queues based on feedback.

---

### How does MLFQ reduce Starvation?

By promoting processes that have been waiting for a long time using Aging.

---

### Why are new processes placed in the highest-priority queue?

Because most new processes are short or interactive, giving them higher priority improves response time.

---

# Easy Way to Remember

Think of a school.

Students are promoted or demoted based on their performance.

Similarly,

MLFQ promotes or demotes processes based on how they behave while using the CPU.

Remember:

**MLQ = Fixed Queue**

**MLFQ = Moving Queue (Feedback)**
# Introduction to Concurrency & Process Synchronization

After completing CPU Scheduling, the next important topic is **Process Synchronization**.

Before learning Mutex, Semaphore, Critical Section, Producer-Consumer Problem, etc., we first need to understand **Concurrency**.

Without understanding Concurrency, the remaining synchronization topics become difficult.

---

# Why do we need Concurrency?

Nowadays, a computer performs many tasks simultaneously.

Example:

- Chrome is downloading a file.
- Spotify is playing music.
- VS Code is compiling code.
- Gmail is receiving emails.
- Antivirus is scanning files.

As a user, it looks like everything is running at the same time.

This ability of the Operating System to handle multiple tasks together is called **Concurrency**.

---

# What is Concurrency?

Concurrency is the ability of an Operating System to manage multiple processes or threads so that they **make progress during the same period of time**.

Important point:

**Concurrency does not always mean that multiple processes execute at the exact same instant.**

Instead, the Operating System rapidly switches the CPU between processes using **Context Switching**.

Because this switching is very fast, users feel that all programs are running together.

In simple words,

> **Concurrency means multiple tasks are in progress at the same time.**

---

# Example of Concurrency

Suppose there is only one CPU.

Three processes are ready.

```
P1

P2

P3
```

The CPU executes them like this:

```
P1

↓

P2

↓

P3

↓

P1

↓

P2

↓

P3
```

Only one process is running at any instant.

However,

all processes continue making progress.

This is called **Concurrency**.

---

# What is Parallelism?

Parallelism means executing multiple processes **at the exact same time**.

This is possible only when the computer has multiple CPU cores.

Example:

Suppose a computer has four CPU cores.

```
Core 1 → Chrome

Core 2 → VS Code

Core 3 → Spotify

Core 4 → Antivirus
```

All four processes execute simultaneously.

This is called **Parallelism**.

---

# Difference Between Concurrency and Parallelism

| Concurrency | Parallelism |
|--------------|-------------|
| Multiple tasks make progress together. | Multiple tasks execute at the exact same time. |
| Achieved using Context Switching. | Achieved using multiple CPU cores. |
| Possible even on a Single-Core CPU. | Requires Multi-Core CPU. |
| Focuses on task management. | Focuses on simultaneous execution. |

---

# Concurrency on Single-Core CPU

A Single-Core CPU can execute only one process at a time.

So the Operating System quickly switches between processes.

Example:

```
Time →

P1 → P2 → P3 → P1 → P2 → P3
```

Because Context Switching is very fast,

the user feels that all programs are running together.

---

# Parallelism on Multi-Core CPU

Suppose the computer has four CPU cores.

```
Core 1 → P1

Core 2 → P2

Core 3 → P3

Core 4 → P4
```

Each process executes simultaneously.

This is **Parallelism**.

---

# Why is Concurrency Important?

### 1. Better CPU Utilization

If one process is waiting for I/O,

the CPU can execute another process.

Thus, CPU remains busy.

---

### 2. Better User Experience

Users can perform multiple tasks without waiting.

Example:

- Watching YouTube
- Downloading Files
- Browsing Internet

at the same time.

---

### 3. Better Throughput

More work can be completed in less time.

---

### 4. Better Resource Sharing

Multiple processes can efficiently use shared hardware resources.

Example:

- Printer
- Memory
- Files
- Database

---

# Problem with Concurrency

Suppose two students are editing the same Google Docs file.

Student A writes:

```
Operating System
```

Student B writes:

```
Computer Networks
```

If both save their changes at the same time,

the final data may become incorrect.

Similarly,

if multiple processes access the same shared resource simultaneously,

incorrect results may occur.

To solve this problem,

the Operating System uses **Process Synchronization**.

---

# What is Process Synchronization?

Process Synchronization is the technique used by the Operating System to coordinate multiple processes or threads that access shared resources.

Its main purpose is to ensure:

- Correct execution.
- Correct data.
- No interference between processes.
- Safe access to shared resources.

---

# What is a Shared Resource?

A Shared Resource is any resource that can be accessed by more than one process or thread.

Examples:

- Shared Variable
- Shared Memory
- Printer
- File
- Database
- Network Connection

Since multiple processes use these resources,

proper synchronization becomes necessary.

---

# Advantages of Concurrency

### 1. Better CPU Utilization

CPU does not remain idle while one process waits for I/O.

---

### 2. Better Throughput

More processes complete in less time.

---

### 3. Better Responsiveness

Interactive applications respond faster.

---

### 4. Efficient Resource Sharing

Multiple processes can share system resources efficiently.

---

# Problems Caused by Concurrency

### 1. Race Condition

Multiple processes modify shared data simultaneously, causing incorrect results.

---

### 2. Deadlock

Processes keep waiting for each other forever.

---

### 3. Starvation

Some processes may never get the required resource.

---

### 4. Complex Programming

Concurrent programs are more difficult to design and debug.

---

# Real-Life Analogy

Imagine one chef preparing three dishes.

He first chops vegetables for Dish A,

then stirs Dish B,

then checks Dish C,

and keeps switching between them.

All dishes continue progressing.

This is **Concurrency**.

Now imagine three chefs,

each preparing one dish simultaneously.

This is **Parallelism**.

---

# Quick Revision

- Concurrency = Multiple processes make progress during the same time period.
- Parallelism = Multiple processes execute simultaneously.
- Concurrency is possible even on a Single-Core CPU.
- Parallelism requires Multiple CPU Cores.
- Concurrency is achieved using Context Switching.
- Shared Resources require Process Synchronization.
- Synchronization ensures correct and safe access to shared resources.

---

# Interview Questions

### What is Concurrency?

Concurrency is the ability of an Operating System to manage multiple processes or threads so that they make progress during the same period of time.

---

### What is Parallelism?

Parallelism is the simultaneous execution of multiple processes using multiple CPU cores.

---

### What is the difference between Concurrency and Parallelism?

Concurrency means multiple tasks make progress together.

Parallelism means multiple tasks execute at the exact same time.

---

### Can Concurrency exist without Parallelism?

Yes.

A Single-Core CPU achieves Concurrency using Context Switching.

---

### Why is Process Synchronization required?

Because multiple processes may access shared resources simultaneously, leading to incorrect results if not coordinated properly.

---

### What is a Shared Resource?

A resource that can be accessed by multiple processes or threads.

Examples:

Memory, Printer, File, Database, Shared Variable.

---

# Easy Way to Remember

**One Chef → Three Dishes → Concurrency**

The chef switches between dishes, so all of them make progress.

**Three Chefs → Three Dishes → Parallelism**

Each chef cooks one dish at the same time.

Remember:

**Concurrency = Switching**

**Parallelism = Simultaneous Execution**
# Race Condition

After learning about Concurrency, we know that multiple processes or threads can run at the same time.

Now imagine that two processes are trying to access the same data simultaneously.

If they modify the data together without proper coordination, the final result may become incorrect.

This problem is called a **Race Condition**.

---

# What is a Race Condition?

A Race Condition is a situation where **two or more processes (or threads) access the same shared resource at the same time, and at least one of them modifies it.**

As a result, the final output depends on the order in which the processes execute.

In simple words,

> Multiple processes "race" to access the same shared resource, so the final result becomes unpredictable.

---

# Why does a Race Condition occur?

A Race Condition occurs when the following three conditions are true:

### 1. Shared Resource

Multiple processes are accessing the same resource.

Examples:

- Shared Variable
- Shared Memory
- File
- Database
- Printer

---

### 2. At least one process modifies the resource

If every process is only reading the data,

there is no Race Condition.

The problem occurs only when at least one process writes or modifies the shared resource.

---

### 3. Concurrent Execution

The processes execute at the same time (or overlap because of Context Switching).

Without concurrent execution, there is no Race Condition.

---

# Example 1 : Counter Variable

Suppose,

```
count = 5
```

Two processes execute simultaneously.

### Process P1

```cpp
count++;
```

### Process P2

```cpp
count++;
```

Expected Answer:

```
5

↓

6

↓

7
```

Final value should be:

```
count = 7
```

---

### What actually happens?

Both processes first read:

```
count = 5
```

Then,

Both calculate:

```
5 + 1 = 6
```

Finally,

Both write:

```
count = 6
```

Final Answer:

```
count = 6
```

instead of

```
count = 7
```

This incorrect result is called a **Race Condition**.

---

# Why does this happen?

Many students think

```cpp
count++;
```

is one CPU instruction.

Actually, it happens in three steps.

```
Read count

↓

Increase by 1

↓

Write count
```

Suppose,

Process P1 reads the value.

Before it writes the new value,

the CPU switches to Process P2.

Now P2 also reads the old value.

Both processes write the same updated value.

Therefore,

one update is lost.

This is called a **Lost Update Problem**, which is a type of Race Condition.

---

# Example 2 : Bank Account

Suppose,

Current Balance:

```
₹1000
```

Two transactions happen simultaneously.

### Process P1

Deposit ₹500

Expected Balance:

```
₹1500
```

### Process P2

Withdraw ₹300

Expected Balance:

```
₹700
```

Correct Final Balance should be:

```
₹1200
```

But if both processes read the balance at the same time,

both read:

```
₹1000
```

P1 writes:

```
₹1500
```

Immediately after,

P2 writes:

```
₹700
```

Final Balance becomes:

```
₹700
```

instead of

```
₹1200
```

Again,

this is a Race Condition.

---

# Real-Life Analogy

Imagine two friends are editing the same Google Docs document.

Friend A writes:

```
Operating System
```

Friend B writes:

```
Computer Networks
```

Both press **Save** at the same time.

Sometimes,

Friend A's changes are saved.

Sometimes,

Friend B's changes are saved.

The final document depends on who saves last.

This unpredictable result is exactly like a **Race Condition**.

---

# Why is Race Condition dangerous?

Race Conditions may cause:

- Incorrect calculations.
- Wrong bank balance.
- Corrupted files.
- Database inconsistency.
- Software crashes.
- Unexpected program behavior.

This is why Race Conditions must be prevented.

---

# How can we prevent Race Condition?

The Operating System should allow **only one process at a time** to access the shared resource.

This is done using synchronization techniques such as:

- Critical Section
- Mutex
- Semaphore
- Monitor

We will study each of these topics next.

---

# When does Race Condition NOT occur?

Suppose two processes execute:

```cpp
cout << count;
```

Both are only reading the value.

No process modifies it.

Therefore,

**Race Condition does not occur.**

---

# When does Race Condition occur?

Suppose two processes execute:

```cpp
count++;
```

or

```cpp
count = count + 10;
```

Here,

the shared variable is being modified.

Therefore,

Race Condition can occur.

---

# Real Operating System Examples

Race Conditions are common in:

- ATM Transactions
- Online Banking
- Railway Reservation Systems
- Flight Booking Systems
- Shared Databases
- Multi-threaded Applications

---

# Advantages of preventing Race Condition

If Race Conditions are prevented:

- Data remains correct.
- Shared resources are accessed safely.
- Programs become reliable.
- System consistency is maintained.
- Unexpected errors are avoided.

---

# Quick Revision

- Race Condition occurs when multiple processes access the same shared resource simultaneously.
- At least one process must modify the shared resource.
- The final result depends on the execution order.
- Reading only → Safe.
- Writing/Modifying → Race Condition may occur.
- `count++` is **not** a single instruction.
- It consists of:
  - Read
  - Modify
  - Write
- Race Condition is prevented using:
  - Critical Section
  - Mutex
  - Semaphore

---

# Interview Questions

### What is a Race Condition?

A Race Condition is a situation where multiple processes or threads access and modify the same shared resource simultaneously, resulting in unpredictable or incorrect output.

---

### Why does Race Condition occur?

Because multiple processes modify shared data concurrently without proper synchronization.

---

### Can Race Condition occur if all processes only read the data?

No.

If every process only reads the data, the shared resource is not modified, so Race Condition does not occur.

---

### Why is `count++` not an atomic operation?

Because it is performed in three steps:

1. Read
2. Modify
3. Write

If another process interrupts between these steps, incorrect results may occur.

---

### Give a real-life example of Race Condition.

Examples:

- ATM Transactions
- Online Banking
- Google Docs editing
- Railway Reservation System

---

### How can Race Condition be prevented?

Using synchronization mechanisms like:

- Critical Section
- Mutex
- Semaphore
- Monitor

---

# Easy Way to Remember

Think of **two people editing the same Google Docs file**.

Both save their changes at the same time.

The final document depends on **who saves last**.

Similarly,

when two processes modify the same shared data simultaneously, the final result becomes unpredictable.

This is called a **Race Condition**.

---

# One-Line Interview Answer

**Race Condition is a situation where multiple processes or threads access and modify the same shared resource simultaneously, causing unpredictable or incorrect results due to the lack of proper synchronization.**
# Critical Section Problem

After learning about Race Condition, we know that problems occur when multiple processes access the same shared resource at the same time.

The Operating System solves this problem using the concept of the **Critical Section**.

This is one of the most important concepts in Process Synchronization because almost every synchronization technique (Mutex, Semaphore, Monitor, etc.) is based on it.

---

# What is a Critical Section?

A **Critical Section** is the part of a program where a process accesses or modifies a **shared resource**.

Examples of shared resources:

- Shared Variable
- Shared Memory
- File
- Printer
- Database
- Counter

Since these resources are shared by multiple processes, only one process should access them at a time.

In simple words,

> A Critical Section is the part of a program where shared data is used and therefore needs protection.

---

# Why do we need a Critical Section?

Suppose two processes execute:

```cpp
count++;
```

Both processes use the same shared variable `count`.

If both execute this statement simultaneously,

the final value of `count` may become incorrect.

This is called a **Race Condition**.

To avoid this,

the Operating System allows only one process at a time to execute the Critical Section.

---

# Real-Life Analogy

Imagine there is only **one ATM machine**.

Two customers arrive together.

Customer A wants to withdraw money.

Customer B wants to deposit money.

If both use the ATM at the same time,

the bank balance may become incorrect.

Therefore,

the bank allows only **one customer inside the ATM room** at a time.

Here,

- ATM Room → Critical Section
- Bank Account → Shared Resource
- Customers → Processes

---

# Structure of a Process

Every process can be divided into four sections.

```
+----------------------+
| Entry Section        |
+----------------------+
| Critical Section     |
+----------------------+
| Exit Section         |
+----------------------+
| Remainder Section    |
+----------------------+
```

---

# 1. Entry Section

Before entering the Critical Section,

the process requests permission from the Operating System.

If the shared resource is free,

the process enters.

Otherwise,

it waits until the resource becomes available.

Example:

A process wants to use the printer.

It first checks whether another process is already using it.

---

# 2. Critical Section

This is the part where the process actually accesses the shared resource.

Examples:

```cpp
count++;
```

```cpp
balance = balance + 500;
```

```cpp
file.write(data);
```

Only **one process** is allowed inside the Critical Section at any time.

---

# 3. Exit Section

After completing the Critical Section,

the process informs the Operating System that it has finished using the shared resource.

Now another waiting process can enter the Critical Section.

---

# 4. Remainder Section

This contains the remaining part of the program.

No shared resources are accessed here.

Examples:

```cpp
printf("Hello");
```

```cpp
int x = 10;
```

Multiple processes can execute the Remainder Section simultaneously because it does not affect shared data.

---

# Example Program

```cpp
while(true)
{
    // Entry Section

    // Critical Section
    count++;

    // Exit Section

    // Remainder Section
    printf("Working...");
}
```

Only the statement

```cpp
count++;
```

needs protection because it modifies shared data.

---

# What is the Critical Section Problem?

The Critical Section Problem is the problem of designing a system that allows multiple processes to share resources **safely** without causing a Race Condition.

The Operating System must ensure that:

- Shared data remains correct.
- Race Conditions do not occur.
- Every process gets a fair chance to execute.

---

# Requirements of a Good Critical Section Solution

A correct solution must satisfy **three conditions**.

These are among the most frequently asked interview questions.

---

# 1. Mutual Exclusion (Most Important)

Mutual Exclusion means:

> If one process is executing inside the Critical Section, no other process can enter it at the same time.

Example:

Suppose P1 enters the Critical Section.

```
P1 → Inside Critical Section

P2 → Waiting
```

Only after P1 leaves,

P2 is allowed to enter.

This prevents Race Conditions.

---

# Real-Life Example of Mutual Exclusion

There is only one washroom with one key.

Only one person can use it at a time.

Others must wait outside.

---

# 2. Progress

Progress means:

If no process is inside the Critical Section,

and one or more processes want to enter,

the Operating System should select one of them **without unnecessary delay**.

Processes that are not interested in entering the Critical Section should not block the decision.

Example:

P1 is doing some normal calculation.

P2 wants to access the printer.

Since P1 is not using the printer,

P2 should be allowed to enter immediately.

---

# 3. Bounded Waiting

Bounded Waiting means:

Every process waiting for the Critical Section should eventually get a chance.

No process should wait forever.

This prevents **Starvation**.

Example:

Three processes:

```
P1 (Waiting)

P2

P3
```

Correct order:

```
P2

↓

P3

↓

P1
```

Wrong order:

```
P2

↓

P3

↓

P2

↓

P3

↓

P2

↓

P3
```

Here,

P1 never gets a chance.

This violates the Bounded Waiting condition.

---

# Why is the Critical Section important?

Without protecting the Critical Section,

the following problems may occur:

- Race Condition
- Incorrect Calculations
- Corrupted Files
- Wrong Bank Balance
- Database Errors
- Unpredictable Program Output

Therefore,

every Operating System protects the Critical Section using synchronization techniques.

---

# How is the Critical Section protected?

The Operating System uses synchronization mechanisms such as:

- Peterson's Algorithm
- Mutex
- Semaphore
- Monitor

These techniques ensure that only one process enters the Critical Section at a time.

---

# Difference Between Race Condition and Critical Section

| Race Condition | Critical Section |
|----------------|------------------|
| It is a problem. | It is a part of a program. |
| Occurs due to simultaneous access to shared data. | Contains code that accesses shared resources. |
| Produces incorrect results. | Needs protection to prevent Race Condition. |

---

# Quick Revision

- Critical Section = Part of the program that accesses shared resources.
- Only one process should execute the Critical Section at a time.
- Critical Section Problem = How to allow safe access to shared resources.
- A correct solution must satisfy:
  - Mutual Exclusion
  - Progress
  - Bounded Waiting
- Race Condition occurs if the Critical Section is not protected.

---

# Interview Questions

### What is a Critical Section?

A Critical Section is the part of a program where shared resources are accessed or modified.

---

### What is the Critical Section Problem?

It is the problem of designing a synchronization mechanism that allows safe access to shared resources while preventing Race Conditions.

---

### What are the three requirements of a good Critical Section solution?

1. Mutual Exclusion
2. Progress
3. Bounded Waiting

---

### What is Mutual Exclusion?

It ensures that only one process can execute the Critical Section at a time.

---

### What is Progress?

If the Critical Section is free, one of the waiting processes should be allowed to enter without unnecessary delay.

---

### What is Bounded Waiting?

Every waiting process should get a chance to enter the Critical Section after a limited number of turns, preventing Starvation.

---

### What is the difference between Race Condition and Critical Section?

Race Condition is the problem caused by simultaneous access to shared data.

Critical Section is the part of the program where shared data is accessed.

---

# Easy Way to Remember

Think of a **public washroom with only one key**.

- Washroom → Critical Section
- Key → Permission to enter
- One person inside → Mutual Exclusion
- If the washroom is empty, the next person should get the key immediately → Progress
- Everyone waiting in line should eventually get the key → Bounded Waiting

Remember this line:

**Critical Section is the place where Race Condition can occur, and Mutual Exclusion is the rule that prevents it.**
# Peterson's Algorithm

After learning about the Critical Section Problem, we know that the Operating System must ensure that only one process enters the Critical Section at a time.

One of the earliest software solutions to solve this problem is **Peterson's Algorithm**.

Although modern operating systems do not use Peterson's Algorithm directly, it is very important because it explains the basic concept of Process Synchronization.

---

# What is Peterson's Algorithm?

Peterson's Algorithm is a **software-based solution** for the Critical Section Problem.

It prevents Race Conditions by ensuring that only one process enters the Critical Section at a time.

It satisfies all three conditions of a good Critical Section solution:

- Mutual Exclusion
- Progress
- Bounded Waiting

**Important:**

Peterson's Algorithm works only for **two processes**.

---

# Why do we need Peterson's Algorithm?

Suppose two processes want to access the same shared variable.

Example:

```cpp
count++;
```

If both execute this statement simultaneously,

the final value of `count` may become incorrect because of a Race Condition.

Peterson's Algorithm coordinates both processes so that only one process enters the Critical Section at a time.

---

# Variables used in Peterson's Algorithm

Peterson's Algorithm uses only two shared variables.

## 1. flag[ ]

```cpp
bool flag[2];
```

This variable tells whether a process wants to enter the Critical Section.

Initially,

```cpp
flag[0] = false;
flag[1] = false;
```

Meaning:

Neither process wants to enter.

If

```cpp
flag[0] = true;
```

it means

```
Process P0 wants to enter the Critical Section.
```

Similarly,

```cpp
flag[1] = true;
```

means

```
Process P1 wants to enter the Critical Section.
```

---

## 2. turn

```cpp
int turn;
```

This variable decides whose turn it is to enter the Critical Section when both processes want to enter simultaneously.

Example:

```cpp
turn = 0;
```

means

```
Give preference to Process P0.
```

```cpp
turn = 1;
```

means

```
Give preference to Process P1.
```

---

# Peterson's Algorithm

## Code for Process P0

```cpp
flag[0] = true;
turn = 1;

while(flag[1] && turn == 1);

/* Critical Section */

flag[0] = false;

/* Remainder Section */
```

---

## Code for Process P1

```cpp
flag[1] = true;
turn = 0;

while(flag[0] && turn == 0);

/* Critical Section */

flag[1] = false;

/* Remainder Section */
```

---

# Step-by-Step Working

Suppose Process P0 wants to enter the Critical Section.

### Step 1

```cpp
flag[0] = true;
```

Meaning:

```
P0 informs the Operating System:

"I want to enter the Critical Section."
```

---

### Step 2

```cpp
turn = 1;
```

Meaning:

```
"If both of us want to enter together,

I am giving Process P1 the first chance."
```

---

### Step 3

```cpp
while(flag[1] && turn == 1);
```

The process checks two conditions.

### Condition 1

Is P1 interested?

```
flag[1] == true
```

### Condition 2

Is it P1's turn?

```
turn == 1
```

If both conditions are true,

P0 waits.

Otherwise,

P0 enters the Critical Section.

---

### Step 4

P0 executes the Critical Section.

During this time,

P1 cannot enter.

---

### Step 5

After finishing,

```cpp
flag[0] = false;
```

Meaning:

```
P0 says,

"I have finished.

Now another process can enter."
```

---

# Example 1

Initially,

```cpp
flag[0] = false;
flag[1] = false;
```

Only P0 wants to enter.

P0 executes

```cpp
flag[0] = true;
turn = 1;
```

Since

```cpp
flag[1] = false;
```

the while condition becomes false.

Therefore,

P0 enters the Critical Section immediately.

---

# Example 2

Suppose both processes want to enter at the same time.

```
flag[0] = true

flag[1] = true
```

P0 sets

```
turn = 1
```

P1 sets

```
turn = 0
```

Whichever process updates `turn` last decides who gets the CPU first.

Suppose finally

```
turn = 0
```

Then,

P0 enters the Critical Section.

P1 waits.

After P0 exits,

P1 enters.

Thus,

only one process is inside the Critical Section at any time.

---

# Why does Peterson's Algorithm work?

Because it satisfies all three conditions.

---

## 1. Mutual Exclusion

Only one process can enter the Critical Section at a time.

Therefore,

Race Condition does not occur.

---

## 2. Progress

If the Critical Section is empty,

one of the waiting processes enters immediately.

No unnecessary waiting occurs.

---

## 3. Bounded Waiting

Every process eventually gets a chance to enter.

No process waits forever.

Hence,

Starvation does not occur.

---

# Advantages

### 1. Simple to understand

Only two variables are used.

---

### 2. Prevents Race Condition

Only one process enters the Critical Section.

---

### 3. Satisfies all three Critical Section requirements

- Mutual Exclusion
- Progress
- Bounded Waiting

---

### 4. Pure Software Solution

No special hardware support is required.

---

# Disadvantages

### 1. Works only for Two Processes

This is the biggest limitation.

Modern Operating Systems execute thousands of processes.

---

### 2. Busy Waiting

The waiting process continuously executes

```cpp
while(flag[1] && turn == 1);
```

This wastes CPU time.

---

### 3. Not used in Modern Operating Systems

Modern systems use

- Mutex
- Semaphore
- Spinlock
- Atomic Hardware Instructions

instead of Peterson's Algorithm.

---

# Real-Life Analogy

Imagine two students want to enter the principal's office.

Both raise their hands.

Both say,

"I want to go."

If both want to enter together,

they decide:

"You go first."

One student enters.

The other waits.

After the first student comes out,

the second student enters.

This is exactly how Peterson's Algorithm works.

---

# Difference Between Peterson's Algorithm and Mutex

| Peterson's Algorithm | Mutex |
|----------------------|-------|
| Software Solution | OS/Hardware Supported Mechanism |
| Works only for 2 Processes | Works for Multiple Processes/Threads |
| Uses `flag` and `turn` | Uses Lock and Unlock Operations |
| Mainly used for learning | Used in real Operating Systems |

---

# Quick Revision

- Peterson's Algorithm is a software solution for the Critical Section Problem.
- It works only for **two processes**.
- It uses two shared variables:
  - `flag[]`
  - `turn`
- `flag[]` tells whether a process wants to enter the Critical Section.
- `turn` decides which process gets priority when both want to enter simultaneously.
- It satisfies:
  - Mutual Exclusion
  - Progress
  - Bounded Waiting
- Main disadvantages:
  - Only two processes
  - Busy Waiting
  - Not used in modern operating systems

---

# Interview Questions

### What is Peterson's Algorithm?

Peterson's Algorithm is a software solution to the Critical Section Problem that allows only one of two processes to enter the Critical Section at a time.

---

### Which variables are used in Peterson's Algorithm?

- `flag[]`
- `turn`

---

### What is the purpose of `flag[]`?

It indicates whether a process wants to enter the Critical Section.

---

### What is the purpose of `turn`?

It decides which process gets priority if both processes want to enter the Critical Section simultaneously.

---

### Does Peterson's Algorithm satisfy all three Critical Section requirements?

Yes.

It satisfies:

- Mutual Exclusion
- Progress
- Bounded Waiting

---

### What is the biggest limitation of Peterson's Algorithm?

It works only for **two processes** and uses **Busy Waiting**, so it is not suitable for modern operating systems.

---

# Easy Way to Remember

Think of **two friends standing outside a room**.

- `flag[]` = "I want to enter."
- `turn` = "You go first."
- One friend enters.
- The other waits.
- After the first friend comes out, the second friend enters.

Remember:

**flag → Interest**

**turn → Priority**

Together, they prevent both processes from entering the Critical Section at the same time.
# Mutex (Mutual Exclusion)

After learning Peterson's Algorithm, we know that it can solve the Critical Section Problem.

However, Peterson's Algorithm works only for **two processes** and is mainly used for understanding synchronization concepts.

Modern Operating Systems use **Mutex** to protect shared resources.

Mutex is one of the most commonly used synchronization mechanisms in Linux, Windows, Java, C++, Android, etc.

---

# What is Mutex?

Mutex stands for **Mutual Exclusion**.

It is a synchronization mechanism that allows **only one process or thread to enter the Critical Section at a time.**

It works like a **lock**.

If a process acquires the lock,

it can enter the Critical Section.

If another process tries to enter while the lock is already held,

it must wait until the lock is released.

In simple words,

> **Mutex is a lock that protects shared resources from being accessed by multiple processes simultaneously.**

---

# Why do we need Mutex?

Suppose two processes execute:

```cpp
count++;
```

Both processes modify the same shared variable.

If both execute simultaneously,

a Race Condition occurs,

and the final value of `count` becomes incorrect.

Mutex solves this problem by allowing only one process to modify the shared resource at a time.

---

# Why is it called Mutual Exclusion?

Mutual Exclusion means:

> **Only one process is allowed inside the Critical Section at any time.**

All other processes are excluded until the current process finishes.

This prevents Race Conditions.

---

# Real-Life Analogy

Imagine there is only **one bathroom with one key**.

Anyone who wants to use the bathroom must first take the key.

If someone already has the key,

everyone else waits.

After finishing,

the person returns the key.

Now another person can use the bathroom.

Here,

- Bathroom → Critical Section
- Key → Mutex
- People → Processes

---

# How does Mutex work?

Mutex has only two basic operations.

---

## 1. lock()

Before entering the Critical Section,

a process executes:

```cpp
lock();
```

Meaning:

```
"I want to use the shared resource."
```

If the Mutex is free,

the process acquires the lock and enters.

If another process already owns the lock,

the process waits.

---

## 2. unlock()

After finishing the Critical Section,

the process executes:

```cpp
unlock();
```

Meaning:

```
"I have finished using the shared resource."
```

The lock becomes free,

and another waiting process can now acquire it.

---

# Program Structure

```cpp
lock();

/* Critical Section */

unlock();

/* Remainder Section */
```

Only the Critical Section is protected.

The Remainder Section can be executed freely.

---

# Example

Suppose two processes want to increment the same variable.

### Process P1

```cpp
lock();

count++;

unlock();
```

### Process P2

```cpp
lock();

count++;

unlock();
```

Initially,

Mutex is free.

P1 executes:

```cpp
lock();
```

P1 acquires the lock.

Now,

Mutex becomes **Locked**.

P1 enters the Critical Section.

Meanwhile,

P2 executes:

```cpp
lock();
```

But the Mutex is already locked.

Therefore,

P2 waits.

After P1 finishes,

it executes:

```cpp
unlock();
```

Mutex becomes free.

Now,

P2 acquires the lock and enters the Critical Section.

Thus,

only one process accesses the shared variable at a time.

Race Condition is prevented.

---

# States of a Mutex

A Mutex has only two states.

## 1. Locked

```
Mutex = Locked
```

A process is using the shared resource.

Other processes must wait.

---

## 2. Unlocked

```
Mutex = Unlocked
```

No process is using the shared resource.

Any waiting process can acquire the lock.

---

# Ownership of Mutex

This is one of the most common interview questions.

When a process successfully executes

```cpp
lock();
```

it becomes the **owner** of the Mutex.

Only the owner is allowed to execute

```cpp
unlock();
```

Example:

P1 executes

```cpp
lock();
```

Now P1 owns the Mutex.

Only P1 can execute

```cpp
unlock();
```

P2 cannot release P1's lock.

This is called **Mutex Ownership**.

---

# Why is Ownership important?

Imagine you lock your house.

Should another person unlock your house?

No.

Similarly,

only the process that locked the Mutex should unlock it.

This prevents incorrect synchronization.

---

# Advantages of Mutex

### 1. Prevents Race Condition

Only one process accesses the shared resource at a time.

---

### 2. Ensures Mutual Exclusion

Critical Section remains protected.

---

### 3. Simple to use

Only two operations:

- lock()
- unlock()

---

### 4. Used in Real Operating Systems

Unlike Peterson's Algorithm,

Mutex is widely used in Linux, Windows, Java, POSIX Threads and many other systems.

---

# Disadvantages of Mutex

### 1. Deadlock

Suppose,

P1 locks Resource A.

P2 locks Resource B.

Now,

P1 waits for Resource B.

P2 waits for Resource A.

Neither can continue.

This situation is called **Deadlock**.

---

### 2. Starvation

If scheduling is unfair,

a process may wait for a long time before getting the lock.

---

### 3. Forgetting to Unlock

If a process forgets to execute

```cpp
unlock();
```

the Mutex remains locked forever.

Other processes remain blocked.

---

# Difference Between Peterson's Algorithm and Mutex

| Peterson's Algorithm | Mutex |
|----------------------|-------|
| Software solution | Practical synchronization mechanism |
| Works only for two processes | Works for multiple processes and threads |
| Uses `flag[]` and `turn` | Uses `lock()` and `unlock()` |
| Mainly for learning | Used in real Operating Systems |

---

# Difference Between Mutex and Binary Semaphore

| Mutex | Binary Semaphore |
|--------|------------------|
| Has ownership | No ownership |
| Only owner can unlock | Any process can perform `signal()` |
| Mainly used for Mutual Exclusion | Used for Synchronization and Mutual Exclusion |

(We will study Binary Semaphore in the next topic.)

---

# Real-Life Examples

Mutex is commonly used in:

- Printer Access
- Shared File Access
- Database Transactions
- Banking Applications
- Multi-threaded Programs
- Shared Memory

---

# Quick Revision

- Mutex stands for **Mutual Exclusion**.
- It is a synchronization mechanism used to protect the Critical Section.
- Only one process can access the shared resource at a time.
- Two operations:
  - `lock()`
  - `unlock()`
- A Mutex has two states:
  - Locked
  - Unlocked
- Only the owner can unlock the Mutex.
- Main advantage:
  - Prevents Race Condition.
- Main disadvantages:
  - Deadlock
  - Starvation
  - Forgetting to unlock.

---

# Interview Questions

### What is Mutex?

Mutex is a synchronization mechanism that ensures only one process or thread accesses the Critical Section at a time.

---

### Why is Mutex used?

To prevent Race Conditions and ensure Mutual Exclusion.

---

### What are the two operations of Mutex?

- `lock()`
- `unlock()`

---

### What is Mutex Ownership?

The process that acquires the Mutex becomes its owner.

Only the owner is allowed to release the Mutex.

---

### Can one thread unlock another thread's Mutex?

No.

Only the thread that locked the Mutex can unlock it.

---

### What happens if a process forgets to unlock the Mutex?

The Mutex remains locked.

Other waiting processes cannot enter the Critical Section.

This may lead to Deadlock or indefinite waiting.

---

# Easy Way to Remember

Think of a **library study room** with only **one key**.

- Whoever takes the key enters the room.
- Others wait outside.
- After finishing, the person returns the key.
- The next person can now enter.

Remember:

**Mutex = One Key → One Person → One Critical Section**
# Semaphore

After learning Mutex, we know that only one process can enter the Critical Section at a time.

But what if multiple identical resources are available?

For example,

- 5 printers
- 10 database connections
- 20 parking spaces

Here, allowing only one process is inefficient.

To solve this problem, the Operating System uses **Semaphore**.

---

# What is a Semaphore?

A Semaphore is a synchronization mechanism used to control access to shared resources.

It uses an **integer variable** to keep track of the number of available resources.

Unlike Mutex, Semaphore can allow one or more processes to access resources depending on the available count.

In simple words,

> **Semaphore is an integer variable that controls how many processes can access a shared resource at the same time.**

---

# Why do we need Semaphore?

Suppose a computer lab has **5 printers**.

If Mutex is used,

only one student can print at a time,

even though 5 printers are available.

This wastes resources.

Semaphore solves this by allowing up to **5 students** to print simultaneously.

---

# Why is it called Semaphore?

The word "Semaphore" comes from railway signaling.

Think of a railway signal.

🟢 Green Signal → Train can move.

🔴 Red Signal → Train must stop.

Similarly,

Semaphore tells a process:

- Resource available → Enter.
- Resource unavailable → Wait.

---

# Semaphore Variable

Semaphore is simply an integer.

Example:

```cpp
Semaphore S = 3;
```

Meaning,

Three identical resources are available.

Example:

- 3 Printers
- 3 Parking Slots
- 3 Database Connections

Whenever a process acquires a resource,

the semaphore value decreases.

Whenever a process releases the resource,

the semaphore value increases.

---

# Operations of Semaphore

Semaphore mainly uses two operations.

## 1. wait() Operation

Also called:

- P()
- Down()
- Acquire()

Purpose:

To request or acquire a resource.

Pseudo Code:

```cpp
wait(S)
{
    while(S <= 0);

    S--;
}
```

Meaning:

If a resource is available,

the process enters,

and the semaphore value decreases.

Otherwise,

the process waits.

---

### Example

Initially,

```
S = 3
```

P1 executes

```
wait(S)
```

Semaphore becomes

```
3 → 2
```

P2 executes

```
wait(S)
```

Semaphore becomes

```
2 → 1
```

P3 executes

```
wait(S)
```

Semaphore becomes

```
1 → 0
```

P4 executes

```
wait(S)
```

Since

```
S = 0
```

P4 must wait until a resource becomes available.

---

## 2. signal() Operation

Also called:

- V()
- Up()
- Release()

Purpose:

To release a resource.

Pseudo Code:

```cpp
signal(S)
{
    S++;
}
```

Meaning:

The semaphore value increases,

allowing another waiting process to enter.

---

### Example

Suppose,

```
S = 0
```

P1 finishes its work.

It executes

```
signal(S)
```

Semaphore becomes

```
0 → 1
```

Now one waiting process can enter.

---

# How Semaphore Works

Suppose there are **2 printers**.

Initially,

```
Semaphore = 2
```

Processes:

```
P1

P2

P3
```

### Step 1

P1 executes

```
wait()
```

Semaphore:

```
2 → 1
```

P1 starts printing.

---

### Step 2

P2 executes

```
wait()
```

Semaphore:

```
1 → 0
```

P2 starts printing.

---

### Step 3

P3 executes

```
wait()
```

Semaphore is 0.

Therefore,

P3 waits.

---

### Step 4

P1 finishes printing.

It executes

```
signal()
```

Semaphore:

```
0 → 1
```

Now,

P3 acquires the printer and starts printing.

---

# Types of Semaphore

There are two types.

---

# 1. Binary Semaphore

Binary means only **two possible values**.

```
0

or

1
```

Example:

```cpp
Semaphore S = 1;
```

Only one process can enter the Critical Section.

It behaves similarly to Mutex.

---

### Example

Initially,

```
S = 1
```

P1 executes

```
wait()
```

Semaphore becomes

```
1 → 0
```

P2 executes

```
wait()
```

P2 waits because the semaphore value is 0.

Only one process can execute.

---

# 2. Counting Semaphore

Counting Semaphore can store any non-negative integer.

Example:

```cpp
Semaphore S = 5;
```

Meaning,

Five identical resources are available.

Up to five processes can use the resources simultaneously.

---

### Example

Parking Lot

Suppose there are 50 parking spaces.

Initially,

```
Semaphore = 50
```

Whenever a car enters,

```
wait()
```

Semaphore decreases.

Whenever a car leaves,

```
signal()
```

Semaphore increases.

Thus,

the semaphore always represents the number of available parking spaces.

---

# Difference Between Binary Semaphore and Counting Semaphore

| Binary Semaphore | Counting Semaphore |
|------------------|--------------------|
| Values are 0 or 1 | Values can be 0,1,2,3... |
| Controls one resource | Controls multiple resources |
| Similar to Mutex | Used for managing identical resources |

---

# Difference Between Mutex and Semaphore

| Mutex | Semaphore |
|--------|-----------|
| Only one process enters | One or more processes may enter |
| Uses `lock()` and `unlock()` | Uses `wait()` and `signal()` |
| Has ownership | No ownership |
| Only owner unlocks | Any process can execute `signal()` |
| Mainly used for Mutual Exclusion | Used for Synchronization and Resource Management |

---

# Advantages of Semaphore

### 1. Prevents Race Condition

Shared resources are accessed safely.

---

### 2. Supports Multiple Resources

Unlike Mutex,

Semaphore can manage multiple identical resources.

---

### 3. Used to solve Synchronization Problems

Semaphore is used in:

- Producer-Consumer Problem
- Reader-Writer Problem
- Dining Philosophers Problem

---

### 4. Better Resource Utilization

Allows multiple processes to use available resources efficiently.

---

# Disadvantages of Semaphore

### 1. Difficult to Implement

Incorrect use of `wait()` and `signal()` may cause synchronization errors.

---

### 2. Deadlock

Improper ordering of resource requests may lead to Deadlock.

---

### 3. Starvation

Some processes may wait for a long time if scheduling is unfair.

---

# Real-Life Examples

Semaphore is used in:

- Printer Management
- Database Connection Pool
- Parking Lot Management
- Thread Synchronization
- Resource Allocation

---

# Quick Revision

- Semaphore is a synchronization mechanism.
- It uses an integer variable.
- It controls access to shared resources.
- Main operations:
  - `wait()`
  - `signal()`
- `wait()` decreases the semaphore value.
- `signal()` increases the semaphore value.
- Two types:
  - Binary Semaphore
  - Counting Semaphore
- Binary Semaphore → One resource.
- Counting Semaphore → Multiple resources.
- Semaphore does not have ownership.
- Used in Producer-Consumer, Reader-Writer and Dining Philosophers.

---

# Interview Questions

### What is a Semaphore?

Semaphore is a synchronization mechanism that uses an integer variable to control access to shared resources.

---

### What are the two operations of Semaphore?

- `wait()` (Acquire)
- `signal()` (Release)

---

### What is the difference between Binary Semaphore and Counting Semaphore?

Binary Semaphore stores only 0 or 1.

Counting Semaphore stores any non-negative integer and manages multiple resources.

---

### What is the difference between Mutex and Semaphore?

Mutex has ownership and only one process can enter the Critical Section.

Semaphore has no ownership and can manage one or multiple resources depending on its value.

---

### Why is Semaphore better than Mutex?

Semaphore can manage multiple identical resources, while Mutex only protects one Critical Section at a time.

---

# Easy Way to Remember

Think of a **parking lot**.

- Number of empty parking spaces = Semaphore value.
- Car enters → `wait()` → Empty spaces decrease.
- Car leaves → `signal()` → Empty spaces increase.

Remember:

**Mutex = One Key 🔑**

**Binary Semaphore = One Signal 🚦**

**Counting Semaphore = Many Tickets 🎫**
# Producer-Consumer Problem (Bounded Buffer Problem)

After learning Semaphore, we now study one of its most important applications: the **Producer-Consumer Problem**.

This is a classic synchronization problem that explains how Producers and Consumers safely share a common buffer.

It is also called the **Bounded Buffer Problem** because the shared buffer has a fixed size.

---

# What is the Producer-Consumer Problem?

The Producer-Consumer Problem is a synchronization problem in which:

- A **Producer** creates data and stores it in a shared buffer.
- A **Consumer** removes data from the same shared buffer.

Since both processes access the same buffer,

proper synchronization is required to avoid errors.

The Operating System must ensure that:

- Producer should not insert data if the buffer is full.
- Consumer should not remove data if the buffer is empty.
- Producer and Consumer should not access the buffer simultaneously.

---

# What is a Buffer?

A Buffer is a temporary storage area where data is stored before it is processed.

Examples:

- Printer Queue
- Keyboard Buffer
- Network Buffer
- Video Streaming Buffer

Think of it as a temporary waiting area for data.

---

# What is a Bounded Buffer?

A Bounded Buffer is a buffer with a **fixed capacity**.

Example:

```
Buffer Size = 5
```

```
+----+----+----+----+----+
|    |    |    |    |    |
+----+----+----+----+----+
```

Only five items can be stored.

If all five positions are occupied,

the Producer must wait.

---

# Components of the Producer-Consumer Problem

## 1. Producer

A Producer creates or generates data.

Examples:

- Keyboard generating characters.
- Camera producing images.
- Sensor generating readings.
- User uploading files.

---

## 2. Consumer

A Consumer uses or processes the data.

Examples:

- Printer printing documents.
- Video Player displaying frames.
- Database storing records.
- Application reading user input.

---

## 3. Shared Buffer

The Producer stores data here,

and the Consumer removes data from here.

Since both access the same buffer,

it becomes a **shared resource**.

Therefore,

Synchronization is necessary.

---

# Problems Without Synchronization

### 1. Buffer Overflow

Suppose,

```
Buffer Size = 5
```

Current Buffer:

```
★★★★★
```

The Producer tries to insert another item.

There is no free space.

Result:

**Buffer Overflow**

---

### 2. Buffer Underflow

Suppose,

```
Buffer = Empty
```

The Consumer tries to remove an item.

No data is available.

Result:

**Buffer Underflow**

---

### 3. Race Condition

If Producer and Consumer access the buffer simultaneously,

the data inside the buffer may become inconsistent.

---

# Solution Using Semaphore

Three synchronization variables are used.

## 1. Mutex

```
mutex = 1
```

Purpose:

Protects the Critical Section.

Only one process can access the shared buffer at a time.

---

## 2. Empty Semaphore

```
empty = Buffer Size
```

Example:

```
Buffer Size = 5

empty = 5
```

Purpose:

Stores the number of empty slots in the buffer.

If

```
empty = 0
```

the Producer must wait.

---

## 3. Full Semaphore

```
full = 0
```

Purpose:

Stores the number of filled slots.

Initially,

the buffer is empty.

Therefore,

```
full = 0
```

If

```
full = 0
```

the Consumer must wait.

---

# Initial Values

For a buffer of size **N**,

```
mutex = 1

empty = N

full = 0
```

This is a very common interview question.

---

# Producer Algorithm

```cpp
wait(empty);

wait(mutex);

/* Insert Item */

signal(mutex);

signal(full);
```

### Step-by-Step

### Step 1

```cpp
wait(empty);
```

Checks whether an empty slot is available.

If no empty slot exists,

the Producer waits.

---

### Step 2

```cpp
wait(mutex);
```

Acquires the lock.

Now only one process can access the buffer.

---

### Step 3

Insert the new item into the buffer.

---

### Step 4

```cpp
signal(mutex);
```

Release the lock.

Another process may now access the buffer.

---

### Step 5

```cpp
signal(full);
```

Increase the number of filled slots.

Consumer can now consume an item.

---

# Consumer Algorithm

```cpp
wait(full);

wait(mutex);

/* Remove Item */

signal(mutex);

signal(empty);
```

### Step-by-Step

### Step 1

```cpp
wait(full);
```

Checks whether any item is available.

If the buffer is empty,

the Consumer waits.

---

### Step 2

```cpp
wait(mutex);
```

Acquires the lock.

---

### Step 3

Remove one item from the buffer.

---

### Step 4

```cpp
signal(mutex);
```

Release the lock.

---

### Step 5

```cpp
signal(empty);
```

Increase the number of empty slots.

Producer can now insert another item.

---

# Example

Suppose,

```
Buffer Size = 3
```

Initially,

```
Buffer = [ _ _ _ ]

empty = 3

full = 0
```

---

Producer inserts A.

```
Buffer = [ A _ _ ]

empty = 2

full = 1
```

---

Producer inserts B.

```
Buffer = [ A B _ ]

empty = 1

full = 2
```

---

Consumer removes A.

```
Buffer = [ _ B _ ]

empty = 2

full = 1
```

Notice:

- Empty slots increase after consuming.
- Filled slots increase after producing.

Semaphore values always represent the current state of the buffer.

---

# Why are Three Semaphores Required?

### Mutex

Protects the Critical Section.

Without Mutex,

Producer and Consumer may access the buffer simultaneously.

---

### Empty

Stops the Producer when the buffer becomes full.

Prevents **Buffer Overflow**.

---

### Full

Stops the Consumer when the buffer becomes empty.

Prevents **Buffer Underflow**.

---

# Advantages

### 1. Prevents Race Condition

Only one process accesses the shared buffer at a time.

---

### 2. Prevents Buffer Overflow

Producer waits when the buffer is full.

---

### 3. Prevents Buffer Underflow

Consumer waits when the buffer is empty.

---

### 4. Efficient Resource Sharing

Producer and Consumer can work independently without corrupting shared data.

---

# Real-Life Examples

Producer-Consumer is used in:

- Printer Spooling
- Keyboard Buffer
- Video Streaming
- Network Packet Buffers
- Message Queues
- Data Pipelines

---

# Difference Between Producer and Consumer

| Producer | Consumer |
|----------|----------|
| Produces data | Consumes data |
| Inserts data into the buffer | Removes data from the buffer |
| Waits if the buffer is full | Waits if the buffer is empty |

---

# Quick Revision

- Producer creates data.
- Consumer uses data.
- Shared Buffer stores data temporarily.
- Buffer has a fixed size (Bounded Buffer).
- Three semaphores are used:
  - `mutex = 1`
  - `empty = Buffer Size`
  - `full = 0`
- Producer waits if the buffer is full.
- Consumer waits if the buffer is empty.
- Mutex protects the Critical Section.
- Empty prevents Buffer Overflow.
- Full prevents Buffer Underflow.

---

# Interview Questions

### What is the Producer-Consumer Problem?

It is a synchronization problem where Producers generate data and Consumers use that data through a shared buffer.

---

### Why is Mutex required?

To ensure only one process accesses the shared buffer at a time.

---

### Why is the `empty` semaphore used?

To prevent the Producer from inserting items when the buffer is full.

---

### Why is the `full` semaphore used?

To prevent the Consumer from removing items when the buffer is empty.

---

### What are the initial values of the semaphores?

For a buffer of size **N**:

```
mutex = 1

empty = N

full = 0
```

---

### Why is it called the Bounded Buffer Problem?

Because the buffer has a fixed size and cannot store unlimited data.

---

# Easy Way to Remember

Think of a **restaurant**.

- 👨‍🍳 Chef = Producer
- 🍽️ Customer = Consumer
- 🪑 Dining Table = Buffer

If all tables are occupied,

the Chef cannot serve more food.

If there is no food on the tables,

Customers cannot eat.

The waiter (Mutex) ensures that serving happens in an organized way.

Remember:

- **Mutex → One person accesses the buffer at a time.**
- **Empty → Free spaces in the buffer.**
- **Full → Filled spaces in the buffer.**
# Reader-Writer Problem

After learning the Producer-Consumer Problem, we now study another classic synchronization problem called the **Reader-Writer Problem**.

In this problem, multiple processes share the same data.

Some processes only **read** the data,

while others **modify** it.

The Operating System must synchronize them so that data remains correct and consistent.

---

# What is the Reader-Writer Problem?

The Reader-Writer Problem is a synchronization problem in which multiple processes access the same shared resource.

There are two types of processes:

- Reader → Reads the data.
- Writer → Modifies or updates the data.

The Operating System must ensure:

- Multiple Readers can read simultaneously.
- Only one Writer can write at a time.
- No Reader is allowed to read while a Writer is writing.

---

# Why do we need the Reader-Writer Problem?

Suppose a college database stores students' marks.

Many students are viewing their marks.

At the same time,

the administrator updates one student's marks.

If students read the database while it is being updated,

they may get incorrect or partially updated information.

Therefore,

proper synchronization is required.

---

# Who is a Reader?

A Reader is a process that **only reads** the shared data.

It never changes the data.

Examples:

- Viewing bank balance.
- Reading student marks.
- Opening a PDF.
- Searching a database.

Since reading does not modify the data,

multiple Readers can work simultaneously.

---

# Who is a Writer?

A Writer is a process that **modifies** the shared data.

Examples:

- Updating marks.
- Editing a document.
- Depositing money into a bank account.
- Updating a database.

Since writing changes the data,

only one Writer is allowed at a time.

---

# Rules of the Reader-Writer Problem

### Rule 1

Multiple Readers can read simultaneously.

Example:

```
Reader 1 → Reading

Reader 2 → Reading

Reader 3 → Reading
```

This is safe because no one is changing the data.

---

### Rule 2

Only one Writer can write at a time.

Example:

```
Writer 1 → Writing

Writer 2 → Waiting
```

Two Writers cannot update the same data together.

---

### Rule 3

Readers and Writers cannot access the shared data simultaneously.

Example:

```
Reader → Reading

Writer → Writing
```

This is **not allowed** because Readers may see inconsistent or partially updated data.

---

# Why are multiple Readers allowed?

Suppose three students are reading the same book.

Nobody is writing or changing the book.

All three students can read together without any problem.

Similarly,

multiple Readers can access shared data together because reading does not modify the data.

---

# Why is only one Writer allowed?

Suppose two teachers update the same student's marks.

Teacher A writes:

```
80
```

Teacher B writes:

```
90
```

If both update the marks simultaneously,

the final result becomes unpredictable.

This causes a Race Condition.

Therefore,

only one Writer is allowed.

---

# Why can't Readers read while a Writer is writing?

Suppose the database contains:

```
Balance = ₹1000
```

The Writer starts updating it to:

```
Balance = ₹1500
```

Before the update is completed,

a Reader reads the balance.

The Reader may get:

- Old value
- New value
- Incomplete or inconsistent data

Therefore,

Readers must wait while a Writer is writing.

---

# Solution Using Semaphore

The solution uses three shared variables.

## 1. mutex

```
mutex = 1
```

Purpose:

Protects the variable `readCount`.

Only one Reader can update `readCount` at a time.

---

## 2. wrt (Write Semaphore)

```
wrt = 1
```

Purpose:

Allows only one Writer to access the shared data.

It also blocks Readers while writing is in progress.

---

## 3. readCount

```
readCount = 0
```

Purpose:

Stores the number of Readers currently reading.

Initially,

```
readCount = 0
```

because no Reader is reading.

---

# Initial Values

Initially,

```
mutex = 1

wrt = 1

readCount = 0
```

This is a common interview question.

---

# Reader Algorithm

```cpp
wait(mutex);

readCount++;

if(readCount == 1)
    wait(wrt);

signal(mutex);

/* Reading */

wait(mutex);

readCount--;

if(readCount == 0)
    signal(wrt);

signal(mutex);
```

---

# Step-by-Step Working of Reader

### Step 1

Acquire `mutex`.

This protects `readCount`.

---

### Step 2

Increase

```cpp
readCount++;
```

---

### Step 3

If this is the first Reader,

lock `wrt`.

This prevents Writers from entering.

---

### Step 4

Reader starts reading.

Other Readers can also enter simultaneously.

---

### Step 5

After reading,

decrease

```cpp
readCount--;
```

---

### Step 6

If this is the last Reader,

release `wrt`.

Now Writers are allowed to write.

---

# Writer Algorithm

```cpp
wait(wrt);

/* Writing */

signal(wrt);
```

The Writer first acquires the write semaphore.

Now,

no other Writer or Reader can access the shared data.

After writing,

the Writer releases the semaphore.

---

# Example

Initially,

```
readCount = 0
```

Reader 1 arrives.

```
readCount = 1
```

Since this is the first Reader,

`wrt` is locked.

---

Reader 2 arrives.

```
readCount = 2
```

Reader 2 also starts reading.

Both Readers read together.

---

Now,

a Writer arrives.

Since `wrt` is locked,

the Writer waits.

---

Reader 1 finishes.

```
readCount = 1
```

Writer still waits.

---

Reader 2 finishes.

```
readCount = 0
```

Now,

`wrt` is released.

The Writer starts writing.

---

# Types of Reader-Writer Problem

## 1. First Reader-Writer Problem

Readers get higher priority.

Readers never wait unless a Writer is already writing.

Disadvantage:

Writer Starvation may occur.

---

## 2. Second Reader-Writer Problem

Writers get higher priority.

If a Writer is waiting,

new Readers are also forced to wait.

Disadvantage:

Readers may wait longer.

---

## 3. Fair Reader-Writer Problem

Both Readers and Writers get fair opportunities.

Neither Readers nor Writers suffer from Starvation.

This approach is preferred in modern systems.

---

# Advantages

### 1. Better Performance

Multiple Readers can work simultaneously.

---

### 2. Efficient Resource Sharing

Reading operations do not block each other.

---

### 3. Data Consistency

Writers always get exclusive access while modifying data.

---

### 4. Prevents Race Condition

Readers never read partially updated data.

---

# Disadvantages

### 1. Starvation

Depending on the implementation,

Readers or Writers may wait for a long time.

---

### 2. Complex Synchronization

More complicated than Producer-Consumer because different rules exist for Readers and Writers.

---

# Real-Life Examples

Reader-Writer synchronization is used in:

- Database Systems
- Banking Applications
- Library Management Systems
- Cloud Storage
- Shared Files
- Configuration Files

---

# Difference Between Reader and Writer

| Reader | Writer |
|---------|---------|
| Reads data | Modifies data |
| Multiple Readers allowed together | Only one Writer allowed |
| Does not change shared data | Changes shared data |

---

# Quick Revision

- Reader only reads the shared data.
- Writer modifies the shared data.
- Multiple Readers can read simultaneously.
- Only one Writer can write at a time.
- Readers and Writers cannot access shared data together.
- Three shared variables are used:
  - `mutex`
  - `wrt`
  - `readCount`
- First Reader locks `wrt`.
- Last Reader unlocks `wrt`.

---

# Interview Questions

### What is the Reader-Writer Problem?

It is a synchronization problem where multiple Readers can read shared data simultaneously, but Writers require exclusive access.

---

### Can multiple Readers read simultaneously?

Yes.

Reading does not modify shared data.

---

### Can multiple Writers write simultaneously?

No.

Only one Writer is allowed to modify shared data at a time.

---

### Can a Reader read while a Writer is writing?

No.

The Reader may read inconsistent or partially updated data.

---

### Why is `readCount` required?

It keeps track of the number of active Readers.

The first Reader blocks Writers,

and the last Reader allows Writers to proceed.

---

### What are the initial values?

```
mutex = 1

wrt = 1

readCount = 0
```

---

# Easy Way to Remember

Think of a **library**.

📚 Students = Readers

✍️ Librarian updating records = Writer

- Many students can read books together.
- Only one librarian updates records.
- While the librarian is updating, students must wait.

Remember:

**Many Readers ✔️**

**One Writer ✔️**

**Reader + Writer Together ❌**
# Dining Philosophers Problem

After learning the Producer-Consumer Problem and Reader-Writer Problem, we now study the last classic synchronization problem called the **Dining Philosophers Problem**.

This problem explains how multiple processes compete for shared resources and how this competition can lead to **Deadlock** and **Starvation**.

It is mainly used to understand resource allocation and synchronization.

---

# What is the Dining Philosophers Problem?

The Dining Philosophers Problem is a synchronization problem in which several philosophers sit around a circular table.

Each philosopher performs only two activities:

- Thinking 🤔
- Eating 🍝

Between every two philosophers, there is one fork.

To eat, every philosopher needs **two forks**:

- Left Fork
- Right Fork

If a philosopher gets only one fork, they cannot eat and must wait.

---

# Why do we study this problem?

The main purpose of this problem is to understand:

- Resource Allocation
- Deadlock
- Starvation
- Mutual Exclusion
- Synchronization

Instead of philosophers and forks, think of them as processes and shared resources.

---

# Representation

Suppose there are:

```
5 Philosophers

5 Forks
```

Arrangement:

```
          P0
      F0      F1

   P4            P1

      F4      F2

          P3
           |
          F3
           |
          P2
```

Each philosopher needs:

```
Left Fork

+

Right Fork
```

to start eating.

---

# What do Philosophers and Forks represent?

| Dining Philosophers Problem | Operating System |
|-----------------------------|------------------|
| Philosopher | Process / Thread |
| Fork | Shared Resource |
| Eating | Using Resource |
| Thinking | Normal Execution |

So,

this problem actually represents multiple processes competing for shared resources.

---

# Working of the Problem

Initially,

all philosophers are thinking.

```
Thinking

Thinking

Thinking

Thinking

Thinking
```

Now,

all philosophers become hungry at the same time.

Each philosopher picks up the **left fork**.

```
P0 → Left Fork

P1 → Left Fork

P2 → Left Fork

P3 → Left Fork

P4 → Left Fork
```

Now everyone waits for the **right fork**.

But,

every right fork is already held by another philosopher.

Result:

No philosopher can continue.

Everyone waits forever.

This situation is called **Deadlock**.

---

# Deadlock in Dining Philosophers Problem

Suppose,

```
P0 waits for P1

P1 waits for P2

P2 waits for P3

P3 waits for P4

P4 waits for P0
```

Every philosopher is waiting for another philosopher.

Nobody releases the fork.

Nobody can eat.

This is called **Deadlock**.

---

# Why does Deadlock occur?

Deadlock occurs because:

- Every philosopher holds one fork.
- Every philosopher waits for another fork.
- No philosopher releases the fork.

This creates a circular waiting chain.

Later, in the Deadlock chapter, we will learn the four Coffman Conditions responsible for Deadlock.

---

# Can Starvation occur?

Yes.

Suppose,

every time Philosopher P0 wants to eat,

other philosophers always get the forks first.

P0 keeps waiting forever.

Other philosophers continue eating.

This situation is called **Starvation**.

---

# Difference Between Deadlock and Starvation

| Deadlock | Starvation |
|-----------|------------|
| Everyone waits forever. | One (or a few) processes wait forever. |
| No process makes progress. | Other processes continue to make progress. |
| Entire system becomes blocked. | Only some processes suffer indefinite waiting. |

---

# Problems in Dining Philosophers Problem

### 1. Deadlock

All philosophers wait forever.

No one can eat.

---

### 2. Starvation

One philosopher never gets a chance to eat,

while others continue eating.

---

### 3. Resource Contention

Many philosophers compete for the same forks.

---

# Solutions to the Dining Philosophers Problem

Several methods can prevent Deadlock.

---

## Solution 1: Allow Only Four Philosophers

Suppose there are:

```
5 Philosophers

5 Forks
```

Allow only **4 philosophers** to try eating simultaneously.

At least one philosopher keeps thinking.

Therefore,

at least one fork remains free.

Deadlock is avoided.

---

## Solution 2: Pick Forks in Different Order

Normally,

every philosopher picks:

```
Left Fork

↓

Right Fork
```

Instead,

make one philosopher pick:

```
Right Fork

↓

Left Fork
```

This breaks the circular waiting condition.

Deadlock is prevented.

---

## Solution 3: Use Semaphore

Before picking up forks,

every philosopher executes:

```cpp
wait(semaphore);
```

After finishing,

```cpp
signal(semaphore);
```

Semaphore controls how many philosophers can attempt to eat at the same time.

---

## Solution 4: Use Monitor

Modern Operating Systems often use **Monitors**.

A Monitor automatically synchronizes access to shared resources and helps prevent Deadlock.

---

# Real-Life Examples

The Dining Philosophers Problem represents many real-world situations.

Examples:

- Multiple printers shared by users.
- Threads competing for files.
- Database locks.
- Cloud resource allocation.
- Multiple network connections.

---

# Advantages of Studying this Problem

It helps us understand:

- Deadlock
- Starvation
- Resource Allocation
- Mutual Exclusion
- Process Synchronization

---

# Quick Revision

- Philosophers represent Processes or Threads.
- Forks represent Shared Resources.
- Every philosopher needs two forks to eat.
- If everyone picks one fork and waits for another,
  Deadlock occurs.
- Starvation occurs when one philosopher never gets a chance to eat.
- Deadlock can be prevented by:
  - Allowing only four philosophers.
  - Changing the order of picking forks.
  - Using Semaphore.
  - Using Monitor.

---

# Interview Questions

### What is the Dining Philosophers Problem?

It is a synchronization problem where multiple philosophers compete for shared forks, demonstrating Deadlock and Starvation.

---

### What does a philosopher represent?

A Process or Thread.

---

### What does a fork represent?

A Shared Resource.

---

### Why does Deadlock occur?

Because every philosopher holds one fork and waits for another, creating a circular waiting condition.

---

### How can Deadlock be prevented?

- Allow only four philosophers.
- Pick forks in different order.
- Use Semaphore.
- Use Monitor.

---

### What is the difference between Deadlock and Starvation?

Deadlock means all processes wait forever.

Starvation means one or a few processes wait forever while others continue executing.

---

# Easy Way to Remember

Imagine **five friends** sitting around a table with **five spoons**.

Each friend needs **two spoons** to eat.

Everyone picks up one spoon first.

Now everyone waits for the second spoon.

Nobody can eat.

Nobody puts the spoon down.

Everyone waits forever.

This is **Deadlock**.

If one friend never gets both spoons because others always take them first,

that is **Starvation**.

Remember:

**Philosopher = Process**

**Fork = Resource**

**Eating = Using Resource**

**Waiting Forever = Deadlock**
# Introduction to Deadlock

After completing Process Synchronization, we now study another very important Operating System topic called **Deadlock**.

Deadlock is one of the most frequently asked interview topics because it explains what happens when multiple processes compete for shared resources.

Understanding Deadlock is necessary before learning Deadlock Prevention, Avoidance, Detection and Recovery.

---

# What is Deadlock?

A **Deadlock** is a situation where **two or more processes are permanently blocked because each process is waiting for a resource that is held by another process.**

As a result,

none of the processes can continue,

and they keep waiting forever.

In simple words,

> **Deadlock occurs when every process waits for another process, and no process can proceed.**

---

# Why does Deadlock occur?

Deadlock occurs when multiple processes need the same shared resources.

Suppose,

Process P1 needs:

- Printer
- Scanner

Process P2 also needs:

- Printer
- Scanner

If both processes acquire one resource each and wait for the other,

neither process can continue.

This creates a Deadlock.

---

# Example

Suppose,

### Process P1

Already has:

```
Printer
```

Needs:

```
Scanner
```

---

### Process P2

Already has:

```
Scanner
```

Needs:

```
Printer
```

Current situation:

```
P1 → Holds Printer → Waiting for Scanner

P2 → Holds Scanner → Waiting for Printer
```

Both processes are waiting.

Neither releases its resource.

Neither process can continue.

This situation is called **Deadlock**.

---

# Resource Allocation Diagram

```
Printer --------> P1

P1 -------------> Scanner

Scanner --------> P2

P2 -------------> Printer
```

Notice that a circular waiting chain is formed.

Every process is waiting for another process.

---

# Step-by-Step Working

### Step 1

P1 acquires the Printer.

---

### Step 2

P2 acquires the Scanner.

---

### Step 3

P1 requests the Scanner.

But,

the Scanner is already with P2.

Therefore,

P1 waits.

---

### Step 4

P2 requests the Printer.

But,

the Printer is already with P1.

Therefore,

P2 also waits.

---

### Final Situation

```
P1 waits for P2

↓

P2 waits for P1
```

No process can continue.

No resource is released.

This is Deadlock.

---

# Real-Life Analogy

Imagine two friends.

Friend A has a **Pen**.

Friend B has a **Notebook**.

Friend A says,

"I'll give you my pen after you give me your notebook."

Friend B says,

"I'll give you my notebook after you give me your pen."

Both keep waiting.

Neither gives up their resource.

This is exactly a Deadlock.

---

# Another Real-Life Example

Imagine a traffic intersection.

Four cars enter from four directions.

Each car blocks the next one.

Nobody can move.

Everyone keeps waiting.

This is a Deadlock.

---

# Why is Deadlock dangerous?

Deadlock creates many problems.

- Processes stop executing.
- Resources remain occupied forever.
- CPU utilization decreases.
- System performance becomes poor.
- Applications may stop responding.
- Users experience system hang or freeze.

---

# Characteristics of Deadlock

A Deadlock usually has these characteristics:

### 1. Processes already hold some resources.

Example:

P1 holds Printer.

P2 holds Scanner.

---

### 2. Processes request additional resources.

Example:

P1 requests Scanner.

P2 requests Printer.

---

### 3. Resources are not released.

Processes continue holding their resources while waiting.

---

### 4. No process makes progress.

Everyone waits forever.

---

# Deadlock vs Starvation

| Deadlock | Starvation |
|-----------|------------|
| All involved processes wait forever. | One or a few processes wait for a very long time. |
| No process makes progress. | Other processes continue executing. |
| Usually caused by circular waiting. | Usually caused by unfair scheduling or resource allocation. |
| Entire group of waiting processes is blocked. | Only some processes are affected. |

---

# Real-Life Examples of Deadlock

### 1. Traffic Junction

Four vehicles block each other.

Nobody can move.

---

### 2. Database Transactions

Transaction T1 locks Table A and requests Table B.

Transaction T2 locks Table B and requests Table A.

Both wait forever.

---

### 3. File Sharing

Process P1 locks File A.

Process P2 locks File B.

Each process waits for the other file.

Deadlock occurs.

---

# Can Deadlock be prevented?

Yes.

Operating Systems use four techniques.

- Deadlock Prevention
- Deadlock Avoidance
- Deadlock Detection
- Deadlock Recovery

These topics will be studied later in this chapter.

---

# Important Terms

### Process

A program that is currently executing.

---

### Resource

Anything required by a process to complete its work.

Examples:

- CPU
- Memory
- Printer
- Scanner
- File
- Database

---

### Waiting

A process cannot continue because the required resource is unavailable.

---

### Resource Allocation

The Operating System assigns available resources to processes.

---

# Quick Revision

- Deadlock occurs when two or more processes wait forever for resources held by each other.
- No process can continue.
- Resources remain occupied.
- System performance decreases.
- Deadlock is different from Starvation.
- Deadlock can be handled using:
  - Prevention
  - Avoidance
  - Detection
  - Recovery

---

# Interview Questions

### What is Deadlock?

Deadlock is a situation where two or more processes wait indefinitely for resources held by each other, so none of them can continue.

---

### Why does Deadlock occur?

Deadlock occurs because each process holds one resource while waiting for another resource that is already allocated to another process.

---

### Give a real-life example of Deadlock.

Two friends each hold one item and refuse to give it until they receive the other person's item.

Example:

One has a pen.

The other has a notebook.

Both wait forever.

---

### What is the difference between Deadlock and Starvation?

Deadlock blocks all involved processes permanently.

Starvation affects one or a few processes, while other processes continue executing.

---

### Can Deadlock be solved?

Yes.

Using:

- Deadlock Prevention
- Deadlock Avoidance
- Deadlock Detection
- Deadlock Recovery

---

# Easy Way to Remember

Imagine **two children exchanging toys**.

Child A has a toy car and wants a robot.

Child B has a robot and wants the toy car.

Neither gives up their toy first.

Both wait forever.

This is **Deadlock**.

Remember:

**"Hold One Resource + Wait for Another = Deadlock."**
# Necessary Conditions for Deadlock (Coffman Conditions)

After learning what Deadlock is, the next question is:

**Can Deadlock occur anytime?**

The answer is **No**.

Deadlock occurs **only when four specific conditions are present at the same time**.

These four conditions are called the **Necessary Conditions for Deadlock** or **Coffman Conditions**.

If **even one condition is removed**, Deadlock cannot occur.

---

# What are Coffman Conditions?

The four necessary conditions for Deadlock are:

1. Mutual Exclusion
2. Hold and Wait
3. No Preemption
4. Circular Wait

All four conditions must exist simultaneously for Deadlock to occur.

---

# Easy Trick to Remember

Remember the word:

```
MHNC

M → Mutual Exclusion

H → Hold and Wait

N → No Preemption

C → Circular Wait
```

---

# 1. Mutual Exclusion

### Definition

At least one resource must be **non-shareable**.

Only one process can use that resource at a time.

If another process requests the same resource,

it must wait.

---

### Example

Suppose there is only one Printer.

P1 is printing.

P2 also wants the Printer.

```
Printer

↓

P1 (Using)

↓

P2 (Waiting)
```

Since the Printer cannot be shared,

P2 must wait.

This satisfies **Mutual Exclusion**.

---

### Real-Life Example

One bathroom.

Only one person can use it at a time.

Others must wait.

---

# 2. Hold and Wait

### Definition

A process already holds one or more resources while waiting for additional resources.

---

### Example

Suppose,

P1 already has:

```
Printer
```

Now P1 requests:

```
Scanner
```

Current situation:

```
P1

Holding → Printer

Waiting → Scanner
```

P1 does not release the Printer while waiting.

This is **Hold and Wait**.

---

### Real-Life Example

A student reserves one computer in the lab.

Now the student also wants the projector.

Instead of releasing the computer,

the student keeps it while waiting for the projector.

---

# 3. No Preemption

### Definition

A resource cannot be taken away forcefully from a process.

The process must release the resource voluntarily after completing its work.

---

### Example

P1 is using the Printer.

The Operating System cannot suddenly take the Printer away and give it to P2.

P1 must finish printing first and then release the Printer.

---

### Real-Life Example

A person is driving a car.

You cannot forcefully take the car away while the person is driving.

The driver must stop and hand it over voluntarily.

---

# 4. Circular Wait

### Definition

A circular chain of waiting exists.

Each process waits for a resource held by another process in the chain.

---

### Example

```
P1 waits for P2

↓

P2 waits for P3

↓

P3 waits for P1
```

This forms a circle.

No process can continue.

This is **Circular Wait**.

---

### Real-Life Example

Three friends decide:

Friend A waits for Friend B.

Friend B waits for Friend C.

Friend C waits for Friend A.

Everyone keeps waiting forever.

---

# Complete Example

Suppose,

```
P1 holds Printer

Needs Scanner
```

```
P2 holds Scanner

Needs Printer
```

Now check all four conditions.

### Mutual Exclusion

Printer and Scanner are non-shareable.

✅ Present

---

### Hold and Wait

P1 holds Printer while waiting for Scanner.

P2 holds Scanner while waiting for Printer.

✅ Present

---

### No Preemption

Resources cannot be taken away forcefully.

✅ Present

---

### Circular Wait

```
P1

↓

Waiting for Scanner

↓

P2

↓

Waiting for Printer

↓

P1
```

✅ Present

Since **all four conditions are present**, Deadlock occurs.

---

# Important Point

If **any one** of these four conditions is removed,

Deadlock **cannot occur**.

For example,

if resources become shareable,

Mutual Exclusion disappears,

so Deadlock is impossible.

This is the basic idea behind **Deadlock Prevention**.

---

# How Operating Systems Prevent Deadlock

The Operating System prevents Deadlock by breaking **at least one** Coffman Condition.

Examples:

- Remove Mutual Exclusion (make resources shareable whenever possible).
- Remove Hold and Wait.
- Allow Preemption.
- Break Circular Wait by assigning an order to resources.

We will study these methods in the next topic.

---

# Summary Table

| Condition | Meaning |
|-----------|---------|
| Mutual Exclusion | Only one process can use a resource at a time. |
| Hold and Wait | A process holds one resource while waiting for another. |
| No Preemption | Resources cannot be taken away forcefully. |
| Circular Wait | Processes wait for each other in a circular chain. |

---

# Why are Coffman Conditions Important?

- Explain why Deadlock occurs.
- Help in Deadlock Prevention.
- Frequently asked in interviews.
- Used as the foundation for Deadlock Avoidance and Banker's Algorithm.

---

# Quick Revision

- Deadlock requires **all four Coffman Conditions**.
- The four conditions are:
  - Mutual Exclusion
  - Hold and Wait
  - No Preemption
  - Circular Wait
- If even one condition is removed,
  Deadlock cannot occur.
- Deadlock Prevention works by breaking one of these conditions.

---

# Interview Questions

### What are Coffman Conditions?

The four necessary conditions for Deadlock are:

- Mutual Exclusion
- Hold and Wait
- No Preemption
- Circular Wait

---

### Is Deadlock possible if one condition is missing?

No.

Deadlock can occur only when all four conditions are satisfied simultaneously.

---

### What is Mutual Exclusion?

Only one process can use a non-shareable resource at a time.

---

### What is Hold and Wait?

A process holds one resource while waiting for another resource.

---

### What is No Preemption?

Resources cannot be taken away forcefully; they must be released voluntarily.

---

### What is Circular Wait?

Processes form a circular chain where each waits for a resource held by the next process.

---

# Easy Way to Remember

Think of **four locks on a door**.

Only if **all four locks are closed**, the door is completely locked.

If even **one lock is opened**,

the door can be opened.

Similarly,

Deadlock occurs only when **all four Coffman Conditions** are present together.

Remember the shortcut:

```
MHNC

M → Mutual Exclusion

H → Hold and Wait

N → No Preemption

C → Circular Wait
```

**Golden Rule:**

**All 4 Conditions Present → Deadlock Possible**

**Any 1 Condition Removed → Deadlock Impossible**
# Resource Allocation Graph (RAG)

After learning the four Coffman Conditions for Deadlock, we now study a graphical method to represent resource allocation called the **Resource Allocation Graph (RAG)**.

A Resource Allocation Graph helps us understand:

- Which process is using which resource.
- Which process is waiting for which resource.
- Whether the system may enter a Deadlock state.

It is one of the most important topics in the Deadlock chapter.

---

# What is a Resource Allocation Graph?

A **Resource Allocation Graph (RAG)** is a directed graph used to represent the relationship between **processes** and **resources**.

It shows:

- Resource allocation.
- Resource requests.
- Possible Deadlock situations.

In simple words,

> **RAG is a graphical representation of how resources are allocated to processes and which resources are being requested.**

---

# Why do we need RAG?

Suppose a system has many processes and many resources.

Keeping track of them using tables becomes difficult.

A Resource Allocation Graph provides a simple visual representation that makes Deadlock analysis easier.

---

# Components of a Resource Allocation Graph

A RAG consists of three components.

---

# 1. Process

Processes are represented using **circles**.

Example:

```
(P1)

(P2)

(P3)
```

Each circle represents one process.

---

# 2. Resource

Resources are represented using **rectangles (or squares)**.

Example:

```
[Printer]

[Scanner]

[File]
```

Each rectangle represents one resource.

If a resource has multiple instances,

multiple small dots are shown inside the rectangle.

Example:

```
+---------+
| •   •   |
| Printer |
+---------+
```

This means the printer has **2 instances**.

---

# 3. Edges

Edges show the relationship between processes and resources.

There are two types of edges.

---

## Request Edge

A Request Edge means:

A process is requesting a resource.

Direction:

```
Process → Resource
```

Example:

```
(P1) ---------> [Printer]
```

Meaning:

P1 wants the Printer.

The Printer has not yet been allocated.

---

## Assignment Edge

An Assignment Edge means:

A resource has already been allocated to a process.

Direction:

```
Resource → Process
```

Example:

```
[Printer] ---------> (P1)
```

Meaning:

The Printer is currently allocated to P1.

---

# Example 1 (No Deadlock)

Suppose,

Printer is allocated to P1.

P2 is waiting for the Printer.

Graph:

```
[Printer] -------> (P1)

(P2) -----------> [Printer]
```

Meaning:

- P1 is using the Printer.
- P2 is waiting.
- Once P1 finishes and releases the Printer,
  P2 can use it.

Therefore,

**No Deadlock exists.**

---

# Example 2 (Deadlock)

Suppose,

P1 holds the Printer and needs the Scanner.

P2 holds the Scanner and needs the Printer.

Graph:

```
[Printer] -------> (P1)

(P1) -----------> [Scanner]

[Scanner] -------> (P2)

(P2) -----------> [Printer]
```

This creates the cycle:

```
P1

↓

Scanner

↓

P2

↓

Printer

↓

P1
```

Both processes wait forever.

This is **Deadlock** (when each resource has only one instance).

---

# How to Analyze a RAG

### Step 1

Identify all Processes (Circles).

---

### Step 2

Identify all Resources (Rectangles).

---

### Step 3

Check Assignment Edges.

These show which process currently owns which resource.

---

### Step 4

Check Request Edges.

These show which process is waiting for a resource.

---

### Step 5

Look for Cycles.

Cycles help identify possible Deadlock.

---

# Does a Cycle Always Mean Deadlock?

This is one of the most common interview questions.

### Case 1

If every resource has only **one instance**,

then

```
Cycle = Deadlock
```

Example:

```
Printer → P1

P1 → Scanner

Scanner → P2

P2 → Printer
```

A cycle exists.

Deadlock exists.

---

### Case 2

If one or more resources have **multiple instances**,

then

```
Cycle ≠ Always Deadlock
```

A cycle only indicates that Deadlock **may** occur.

The system may still continue if another free resource instance is available.

---

# Example of Multiple Instances

Suppose,

Printer has **2 instances**.

One Printer is allocated to P1.

Another Printer is still free.

P2 requests a Printer.

Since another Printer is available,

P2 gets it immediately.

Therefore,

no Deadlock occurs,

even if a cycle appears.

---

# Advantages of Resource Allocation Graph

### 1. Easy Visualization

Shows processes and resources clearly.

---

### 2. Helps Detect Deadlock

Cycles help identify Deadlock situations.

---

### 3. Easy to Understand

More intuitive than complex resource allocation tables.

---

# Limitations of Resource Allocation Graph

### 1. Large Systems

For systems with many processes and resources,

the graph becomes difficult to read.

---

### 2. Multiple Resource Instances

A cycle does not always indicate Deadlock.

Further analysis is required.

---

# Real-Life Analogy

Imagine a library.

Students = Processes

Books = Resources

If

Student A has Book 1 and wants Book 2,

Student B has Book 2 and wants Book 1,

both wait forever.

Drawing arrows between students and books gives a Resource Allocation Graph.

---

# Quick Revision

- RAG = Graphical representation of Processes and Resources.
- Circle → Process.
- Rectangle → Resource.
- Process → Resource = Request Edge.
- Resource → Process = Assignment Edge.
- Cycle with single-instance resources = Deadlock.
- Cycle with multiple-instance resources = Deadlock may or may not occur.

---

# Interview Questions

### What is a Resource Allocation Graph?

A Resource Allocation Graph is a directed graph that represents processes, resources, resource allocation and resource requests.

---

### What does a circle represent?

A Process.

---

### What does a rectangle represent?

A Resource.

---

### What is a Request Edge?

A directed edge from a Process to a Resource, showing that the process is requesting the resource.

---

### What is an Assignment Edge?

A directed edge from a Resource to a Process, showing that the resource has been allocated to the process.

---

### Does a cycle always indicate Deadlock?

No.

- If every resource has only one instance, a cycle indicates Deadlock.
- If resources have multiple instances, a cycle only indicates the possibility of Deadlock.

---

# Easy Way to Remember

Think of a **library**.

📚 Books = Resources

👨‍🎓 Students = Processes

- Student → Book = Wants the book.
- Book → Student = Book is already issued.

Remember:

**Process → Resource = Request**

**Resource → Process = Allocation**

And remember the golden interview rule:

**Single Instance + Cycle = Deadlock**

**Multiple Instances + Cycle = Deadlock may or may not occur**