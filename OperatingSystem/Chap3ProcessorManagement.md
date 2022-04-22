# C3 Processor Management

# How Does Processor Manager Allocate CPU to Jobs
- Processor Manager performs
    - Job Scheduling
    - Process Scheduling
    - Interrupt Management
- Single user systems
    - Processor busy only when user executing a job
    - Other time is idle
    - Processor management is simple
- Multiprogramming environment
    - Processor must be allocated to each job in a fair and efficient manner
    - Requires scheduling policy (preemptive vs non-preemptive)
    - Requires a scheduling algorithm (FCFS, SRTF etc)
    - Allow execution of more than 1 program, the processor can switch rapidly between them
    - Requires sufficient memory
- Active Multiprogramming
    - Time-sharing (multi tasking) system
    - Allows each program to use a preset slice of each CPU time
    - When time expires, the job is interrupted and another job is allowed to begin
    - More control over interrupts
    - Maximize CPU utilisation
    - Context switching with preemption
- Passive Multiprogramming
    - Allows each program to be serviced in turn
    - One program is serviced after another with an interrupt
    - Ties up CPU time and all other jobs have to wait
    - Without preemptive

# Job Scheduling & Process Scheduling & misc
- Processor Manager has 2 sub-managers
    - Job Scheduler
    - Process Scheduler

### Job Scheduler
- In charge of job scheduling
- High level / long term scheduler
- Selects jobs from a queue of incoming jobs
- Places them in a ready queue (batch(rmb batch system?) or interactive(more I/O operations)), based on each job's characteristics
- Goal: 
    - To put jobs in a sequence that uses all system's resources as fuly as possible
    - Provide a balanced mix of jobs (I/O bound vs processor bound)
    - Tries to keep most system components busy most of time
        - Controls degree of multiprogramming

### Process Scheduler
- In charge of process scheduling
- Low level scheduler / dispatcher
- Assigns the CPU to execute processes of those jobs placed on the ready queue by the job scheduler
- Determines which process will get CPU, when and how long
- Decides when a process should be interrupted
- Determines which queue the process should be moved to during execution
- Recognizes when a process has finished and should be terminated

### CPU Cycles and I/O Cycles
- Process Scheduler uses common trait among most computer programs: alternates between CPU cycles and I/O cycles
- I/O bound jobs
    - Such a printing a series of documents
    - Many brief CPU cycles and long I/O cycles
- CPU bound jobs
    - Such as finding the first 300 prime numbers
    - Have long CPU cycles and shorter I/O cycles

### Middle Level Scheduler
- Also called **swapper**
- Usually found in a highly interactive environment (Time sharing environment)
- Removes active jobs from memory to reduce degree of multiprogramming and allows jobs to be completed faster
- In charge of handling the swapped out processes
- Purpose of swapping
    - Reduce degree of multiprogramming
        - Degree of multiprogramming -> number of processes in the ready queue
    - Improve Mix - jobs completed faster
- Thrashing
    - A problem of swapping
    - Happens when a process is busy swapping pages in and out
    - The page fault rate is high if there is not sufficient physical memory
    - Leads to low CPU utilization

# Process State
- Scheduler dispatch the selected job from the ready queue and send it to the CPU run
- Interrupt is used to force CPU and save PCB(Process Control Block) and put it in ready queue (context switching)

### Job status
- New/Hold: Process is being created
- Ready: Process is waiting to be assigned to a process (waiting for CPU)
- Running: Instructions are executed
- Waiting: The process is waiting for some event to occur (wait for I/O)
- Finish: The process has finished execution

### Process Control Block (PCB)
- Each process in the OS is represented by a PCB repository for information that vary from process to other process
- Contains
    - Process state
    - Program Counter
    - CPU Registers
    - CPU Scheduling Information
    - Memory Management Information
    - Accounting Information
    - I/O Status Information

### PCB and Queuing
- PCB of a job is when Job Scheduler accepts it (PCB is stored in queue)
- The Queues use PCBs to track jobs

### Process Scheduling Queues
- Job Queue
    - Set of all processes in the system
- Ready Queue
    - Set of all processes residing in main memory
    - Generally stored as a linked list with a header node containing pointers to the first and last PCBs
- Device Queue
    - Set of processes waiting for an I/O device
    - Each device has its own device queue

# Interrupt Types
- Page Interrupt (Memory Manager)
    - Accomodate job requests
- Time Quantum
    - Expiration interrupt
- I/O Interrupt
    - Emitted when a READ or WRITE command is issued
    - Have to be emitted as there shouldn't be more than one program opening the same file at once
- Internal Interrupt (synchronous interrupt)
    - Emitted for arithmetic operation or job instruction
- Illegal Arithmetic Operation Interrupt
    - Dividing by zero
    - Bad floating point operation generating an overflow or underflow
- Illegal Job Instruction Interrupt
    - Protected or non-existent storage access attempt
    - Attempts to make system changes
        - Trying to change the size of time quantum

### Interrupt handler
- Controls program
    - Handles interruption event sequence
- Interrupt handler sequence
    - Interrupt type described and stored (passed to user as an error message)
    - Interrupted process state saved (value of the program counter and contents of all registers)
    - Interrupt is processed
        - Non-recoverable interrupt
            - Job processing is terminated
            - Resources allocated to the job are released
            - Error message sent to user
        - Recoverable
            - I/O interrupt: Job moved to the I/O queue
            - Time Quantum Interrupt: Job moved to Ready Queue
            - Processor resumes normal operation

# Process Scheduling Policies
- Three limitations of system must be resolved before operating system can schedule all jobs in a multiprogramming environment
    - Finite number of resources (such as disk drives, printers and tape drivers)
    - Some resources can't be shared once they are allocated (like printers)
    - Some resources require operator intervention (such as tape drives)

### Good Scheduling Policy
- Maximize throughput by running as many jobs as possible in a given amount of time (Batch System)
- Maximize CPU efficiency by keeping CPU busy 100% at all times
- Ensure fairness for all jobs by giving everyone an equal amount of CPU and I/O time
- Minimize response time by quickly turning around interactive requests (Interactive Systems)
- Minimize turnaround time by moving entire jobs in/out of system quickly
- Minimize waiting time by moving jobs out of READY queue as quickly as possible

```
WAITING TIME
= finishTime - arrivalTime - cpuCycle

Turnaround Time
= finishTime - arrivalTime
```

### Preemptive schedling Policy
- Interrupts the processing of a job and transfers the CPU to another job
- Arrival process will interrupt current process
- Algorithms
    - SRT (Shortest Remaining Time First)
    - RR (Round Robin)
    - PS (Priority Scheduling)

### Non-preemptive scheduling policy
- Functions without external interrupts
- Once a job captures the processor and begins execution, it remains RUNNING
- Jobs remain uninterrupted until it issues an I/O request (natural wait) or until it finishes (except for infinite loops)
- Algorithms
    - FCFS (First Come First Served)
    - SJN (Shortest Job Next)

# Process Scheduling Algorithms

### Categories
- Non-preemptive
    - First Come First Serve
    - Shortest Job Next
- Preemptive
    - Round Robin
    - Shortest Remaining Time First
- Priority Scheduling
    - Can be preemptive
    - Can be non preemptive
