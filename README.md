# 2023 Google Summer of Code (GSoC) Overview

Parallel programming has advanced many of today's scientific computing projects to a new level.
However, writing a program that utilizes parallel and heterogeneous computing resources
is not easy because you often need to deal with a lot of technical details,
such as load balancing, programming complexity, and concurrency control.
[Taskflow](https://taskflow.github.io/) streamlines this process and helps you quickly create 
high-performance computing (HPC) applications with programming productivity.

As the user community of Taskflow continues to grow (e.g., over 1.5M downloads),
we have identified an important project to enhance Taskflow's library infrastructure,
described below:

## Project: Create Parallel Algorithm Primitives

The goal of this project is to establish a comprehensive set of task-parallel algorithm primitives
atop Taskflow and to strike a balance among programming productivity, performance, and portability.

### Rationale

Parallel algorithm primitives, such as scan, reduce, sorting, and so on, 
are very common for most parallel applications. 
Programmers can leverage these primitives to quickly parallelize fundamental algorithms without the need
to rewrite these algorithms, manage the details, and tune the performance, all of which are known difficult
to program correctly.
However, the current version of Taskflow supports only a few sets of [parallel algorithm primitives](https://taskflow.github.io/taskflow/Algorithms.html) 
that are not sufficient for the need of our users.
This project aims to overcome this challenge by completing a full set of parallel algorithm primitives
based on the newest C++17 parallel algorithm standards.

### Approach

1. Implement a full set of parallel algorithm primitives atop Taskflow based on [C++17 standards](https://en.cppreference.com/w/cpp/algorithm)
2. Integrate the solution into the mainstream LLVM and GCC toolchains as a 3rd-party for parallel algorithm implementation
3. Compare the solution quality with the existing implementation of Intel TBB

### Expected Outcome

We will merge the solution to the main Taskflow parallel algorithm library. 
Our handbook will contain comprehensive instructions for reproducing the results and benchmarking the performance with Intel TBB.
We will also encourage participants to publis these results in related parallel computing conferences
or arXiv journals and to present our findings in leading C++ communities (e.g., CppCon, CppNow).

### Skills Required/Preferred

Participants should have decent C++14/17 programming experience. 
Basic knowledge about parallelism is preferred.

### Mentors

The [Taskflow Team](https://taskflow.github.io/taskflow/team.html) will mentor this project throughout the course of summer code.
Participants should expect weekly project meeting to sync up the progress.

### Expected Size of Project

We expect a *large size* (350 hours) for this project because it spans multiple activities, such as implementing algorithms, benchmarking the solutions, and deploying solutions to real use cases.

### Difficulty Level

We rate this project an *medium* level of difficulty. This project primarily focuses on 
*using* Taskflow to implement parallel algorithms and applications, rather than developing
the Taskflow core functionalities. 
Participants in this project will gain much practical and hands-on experience 
of parallel programming and underatand the pros and cons of mainstream parallel programming tools.

### Contact

Feel free to reach out the tsung-wei.huang at utah.edu for any questions.
