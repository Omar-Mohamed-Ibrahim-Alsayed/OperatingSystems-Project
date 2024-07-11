# MINIX3 Enhancements

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
  - [Requirement 1: Overview of Operating System Structures](#requirement-1-overview-of-operating-system-structures)
  - [Requirement 2: Implementing Different Scheduling Algorithms](#requirement-2-implementing-different-scheduling-algorithms)
  - [Requirement 3: Paging in XV6](#requirement-3-paging-in-xv6)
  - [Requirement 4: Adjusting MINIX3 File System to Use Extents](#requirement-4-adjusting-minix3-file-system-to-use-extents)
- [Usage](#usage)
- [Testing](#testing)

## Introduction

This project aims to enhance MINIX3 by implementing various scheduling algorithms, introducing paging in XV6, and adjusting the file system to use user-defined extents. These enhancements are designed to improve the efficiency, flexibility, and usability of the operating system.

## Features

### Requirement 1: Overview of Operating System Structures

This section provides a comprehensive overview of the operating system, discussing its main components and internal structures. It explains different approaches to structuring an operating system, including simple, complex, layered, modular, and microkernel structures, with a focus on MINIX3's microkernel structure.

### Requirement 2: Implementing Different Scheduling Algorithms

This feature allows users to choose from four scheduling algorithms in MINIX3: Round Robin, Shortest Job First, Priority Scheduling, and Multi-Level Feedback Scheduling. The implementation details and testing results for each algorithm are provided.

### Requirement 3: Paging in XV6

Paging is implemented in XV6 to enhance memory management. This section explains paging, the page table structure, paging configuration, hierarchical paging, and page replacement algorithms (FIFO and LRU). Users can choose between FIFO and LRU for page replacement by setting a variable.

### Requirement 4: Adjusting MINIX3 File System to Use Extents

The file system in MINIX3 is adjusted to use extents instead of blocks. Users can define the extent size in the `const.h` file. The allocation and freeing of consecutive blocks are handled automatically.

# Usage
Choosing a Scheduling Algorithm
To choose a scheduling algorithm, modify the algorithm variable in the do_noquantum function.

# Configuring Paging in XV6
To configure paging, access the mmu.h file and modify the PAGEALGORITHM variable to 0 for FIFO or 1 for LRU.

# Setting Extent Size
To set the extent size, edit the EXT2_PREALLOC_BLOCKS constant in the const.h file located in \minix-master\minix\fs\ext2.

# Testing
Testing has been conducted for each feature:

-  Scheduling Algorithms: Tested using C++ simulations for Round Robin, Shortest Job First, Priority, and Multi-Level Feedback.
-  Paging: Tested using FIFO and LRU algorithms.
-  File System Extents: Verified by changing the EXT2_PREALLOC_BLOCKS constant and ensuring proper allocation and freeing of blocks.
