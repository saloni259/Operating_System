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