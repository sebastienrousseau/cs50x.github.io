---
name: "CS50x Hub"
short_name: "cs50x"
title: "Developer Guides: Valgrind, GDB & Memory Management"
description: "Practical engineering guides on diagnosing segmentation faults, memory leaks, and pointer arithmetic."
keywords: "valgrind guide, GDB tutorial, C pointers memory diagram, Big O cheatsheet"
author: "Sebastien Rousseau"
date: "2026-09-01"
language: "en-GB"
layout: "page"
permalink: "https://cs50x.com/guides/index.html"
logo: "https://cloudcdn.pro/cmn/v1/logos/cmn.svg"
banner: "https://cloudcdn.pro/stocks/images/quantum-computer-room-1200.webp"
banner_alt: "CS50x Hub — Harvard CS50 Complete Companion & Study Guides"
---

# Developer Guides: Debugging & Memory Management

## 1. Mastering Valgrind for Memory Leak Elimination

When working with dynamic heap allocations (`malloc`, `calloc`, `realloc`), memory leaks occur when allocated blocks lose all pointer references before being passed to `free()`.

### Diagnostic Command
```bash
valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes ./speller texts/shakespeare.txt
```

### Common Valgrind Error Types
1. **Invalid read/write of size N:** Attempting to access memory before or after an allocated buffer (buffer overflow/underflow).
2. **Conditional jump or move depends on uninitialised value(s):** Reading a variable before assigning it an initial value.
3. **Definitely lost:** Heap memory that was allocated and never freed with no remaining pointer pointing to it.

---

## 2. Big O Asymptotic Complexity Cheatsheet

<div class="table-responsive my-4">
<table class="table table-dark table-striped">
<thead>
<tr>
<th>Algorithm / Data Structure</th>
<th>Search Time</th>
<th>Insert Time</th>
<th>Space Complexity</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Array (Unsorted)</strong></td>
<td>O(n)</td>
<td>O(1) amortized</td>
<td>O(n)</td>
</tr>
<tr>
<td><strong>Array (Sorted / Binary Search)</strong></td>
<td>O(log n)</td>
<td>O(n)</td>
<td>O(n)</td>
</tr>
<tr>
<td><strong>Linked List</strong></td>
<td>O(n)</td>
<td>O(1)</td>
<td>O(n)</td>
</tr>
<tr>
<td><strong>Hash Table</strong></td>
<td>O(1) average / O(n) worst</td>
<td>O(1) average</td>
<td>O(n)</td>
</tr>
<tr>
<td><strong>Trie (Prefix Tree)</strong></td>
<td>O(k) where k is word length</td>
<td>O(k)</td>
<td>O(k * alphabet_size)</td>
</tr>
</tbody>
</table>
</div>
