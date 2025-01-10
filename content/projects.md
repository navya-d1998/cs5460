## Potential class projects

### Scalable buffer cache

Study scalability and performance issues in the Linux buffer cache and suggest an alternative, more scalable design. 

### Linux scalability (15 years later)

Fourteen years ago, Linux had a number of scalability issues (some of them documented here): 
[An Analysis of Linux Scalability to Many Cores](https://pdos.csail.mit.edu/papers/linux:osdi10.pdf)

However, what are these issues today? Some researchers argue they still exist, e.g., [NrOS: Effective Replication and Sharing
in an Operating System](https://www.usenix.org/system/files/osdi21-bhardwaj.pdf). 

The project will try to identify scalability issues in the kernel and hopefully address them. 

### A case for core-coherent TLBs

Historically, TLB shootdown is one of the major scalability bottlenecks in modern systems, e.g., see [The Multikernel: A new OS architecture
for scalable multicore systems](https://barrelfish.org/publications/barrelfish_sosp09.pdf), [NrOS: Effective Replication and Sharing
in an Operating System](https://www.usenix.org/system/files/osdi21-bhardwaj.pdf), [Optimizing the TLB Shootdown Algorithm with Page Access Tracking](https://www.usenix.org/system/files/conference/atc17/atc17-amit.pdf), [Don't shoot down TLB shootdowns!](https://nadav.amit.zone/publications/amit2020tlb.pdf) and more. 

The question is: why don't we have core-coherent TLBs? Are they prohibitively expensive (more than one cycle to look up?)? What can be potential performance benefits for hardware supported TLB synchronization? 

### Minimal hypervisor

Security of modern datacenters depends on the size and complexity of modern virtualization solutions. We see a range of hypervisors aimed to reduce the TCB of the hypervisor with the goal to reach stronger isolation guarantees: [https://gvisor.dev/docs/](gVisor), [Firecracker: Lightweight Virtualization
for Serverless Applications](https://www.usenix.org/system/files/nsdi20-paper-agache.pdf). 

The goal of this project is to develop a minimal hypervisor designed for strong isolation and potentially the possibility of verification. 



### User-level interrupts and support for user-level device drivers

Intel user-level interrupts provide hardware support for delivery of interrupts directly to 
user processes [x86 User Interrupts support] (https://lwn.net/Articles/869140/). How does this mechanism affect architecture of the modern kernel? What are the overheads of user-level interrupt delivery? 
Can we implement efficient user-level drivers? 

### Performance analysis of CHERI Morello capabilities

CHERI morello provides a variety of ways for isolating untrusted code. Sometimes, though the costs of these mechanims are somewhat counter-intuitive. The project will study performance overheads of each configuration trying to gain deeper understanding of the isolation mechanisms and their overheads. 

### Linux kernel vulnerabilities vs bug fixes

How many kernel vulnerabilities are really there? I.e., what fraction of Linux bug fixes gets a vulnerability assigned? How can we answer this question? Dig the Linux commit messages.

### C vs Rust

It's known that Rust results in a slightly slower code compared to C. But really, can we 
identify exact reasons why and try to improve?  
