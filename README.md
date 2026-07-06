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