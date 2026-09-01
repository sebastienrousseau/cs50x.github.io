---
name: "CS50x Hub"
short_name: "cs50x"
title: "Problem Set Guidance & Conceptual Strategies"
description: "Conceptual strategies, algorithmic pseudocode, and debugging approaches for CS50x problem sets."
keywords: "CS50 problem sets, Tideman strategy, Speller hash table, Filter image processing"
author: "Sebastien Rousseau"
date: "2026-09-01"
language: "en-GB"
layout: "page"
permalink: "https://cs50x.com/problem-sets/index.html"
logo: "https://cloudcdn.pro/cmn/v1/logos/cmn.svg"
banner: "https://cloudcdn.pro/stocks/images/quantum-computer-room-1200.webp"
banner_alt: "CS50x Hub — Harvard CS50 Complete Companion & Study Guides"
---

# Problem Set Strategies & Conceptual Models

Mastering the most challenging assignments in the CS50x curriculum.

## 1. Tideman (Week 3: Ranked Pairs Voting)
- **Concept:** Graph theory, directed acyclic graphs (DAG), cycle detection using Depth-First Search (DFS).
- **Key Strategy:** Before locking an edge `[winner -> loser]`, run a recursive check to see if `loser` can already reach `winner`. If a path exists, adding the edge creates a cycle and must be skipped.

## 2. Filter (Week 4: Image Processing in C)
- **Concept:** 2D pixel arrays, RGB triplets, edge detection with Sobel kernels.
- **Key Strategy:** Always allocate a temporary buffer when applying blur or edge filters so modified adjacent pixel values do not corrupt subsequent calculations in the same pass.

## 3. Speller (Week 5: Dictionary Spell Checker)
- **Concept:** Hash tables, collision resolution via linked lists, memory leak elimination with `valgrind`.
- **Key Strategy:** Design a fast, uniform hash function (e.g. polynomial rolling hash or DJB2) to minimize bucket chain length. Ensure every allocated `node` is freed recursively in `unload()`.

## 4. C$50 Finance (Week 9: Full-Stack Stock Portfolio)
- **Concept:** SQL transactions, session authentication, real-time stock API quote lookups, CSRF protection.
- **Key Strategy:** Enforce atomicity when executing buy/sell operations: balance updates and transaction ledger inserts must occur within a single database transaction block.
