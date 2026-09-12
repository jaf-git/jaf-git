<div align="center"><img src="docs/assets/hero-v4.svg" alt="Jawad Abo Fakher — backend engineer, Java and Spring Boot, Cluj-Napoca. 265 REST endpoints, 91 SQL tables, 506 test files, 104 migrations. Graduating 2026, open to backend roles." width="100%"><img src="docs/assets/intro-v4.svg" alt="I write backend services in Java and Spring Boot, and I am comfortable further down the stack than most people who do. Final year at the Technical University of Cluj-Napoca." width="100%"><img src="docs/assets/stack-v4.svg" alt="Stack by layer — languages, backend, data, testing, delivery, frontend." width="100%"><a href="https://github.com/jaf-git/flowops"><img src="docs/assets/flowops-v4.svg" alt="FlowOps — bachelor thesis. Process discovery from chat messages. Java 21, Spring Boot, React, PostgreSQL. 17 bounded contexts, 265 endpoints, 506 test files." width="100%"></a><a href="https://github.com/jaf-git/api-contract-validator"><img src="docs/assets/validator-v4.svg" alt="API Contract Validator — IntelliJ plugin in Kotlin that flags disagreement between controllers and an OpenAPI specification as you type." width="100%"></a><a href="https://github.com/jaf-git/hardware-programming"><img src="docs/assets/mips-v4.svg" alt="MIPS CPU — a 32-bit processor in VHDL, built up from the register file: datapath, control unit, instruction and data memory." width="100%"></a><a href="https://github.com/jaf-git/bank-marketing-neural-network-classifier"><img src="docs/assets/ml-v4.svg" alt="Bank Marketing classifiers — imbalanced classification on 45,211 UCI records. Best result F1 0.4375, ROC-AUC 0.7910." width="100%"></a><img src="docs/assets/algorithms-v4.svg" alt="Algorithms by area — trees, graphs, recursion and dynamic programming, concurrency. Most written twice, in Java and C++." width="100%"><img src="docs/assets/work-v4.svg" alt="How I work — break a test to check it works; rules nobody enforces stop being followed; invariants belong in the schema; comments should explain why." width="100%"><a href="https://github.com/jaf-git/flowops"><img src="docs/assets/cta-v4.svg" alt="Available for backend engineering roles, graduating 2026. Cluj-Napoca, Romania, open to hybrid and remote." width="100%"></a>

<br>

**[email](mailto:YOUR@EMAIL.COM)** · **[linkedin](https://linkedin.com/in/YOUR-HANDLE)** · **[cv](docs/cv.pdf)** · cluj-napoca, romania

![Java](https://img.shields.io/badge/java_21-0A1410?style=flat-square&labelColor=0A1410&color=3BF07A)
![Spring Boot](https://img.shields.io/badge/spring_boot-0A1410?style=flat-square&labelColor=0A1410&color=1C7A43)
![PostgreSQL](https://img.shields.io/badge/postgresql-0A1410?style=flat-square&labelColor=0A1410&color=1C7A43)
![Docker](https://img.shields.io/badge/docker-0A1410?style=flat-square&labelColor=0A1410&color=1C7A43)
![TypeScript](https://img.shields.io/badge/typescript-0A1410?style=flat-square&labelColor=0A1410&color=1C7A43)
![C](https://img.shields.io/badge/c-0A1410?style=flat-square&labelColor=0A1410&color=1C7A43)

</div>

<details>
<summary><code>graphs</code> — shortest paths, spanning trees, traversal</summary>

<br>

| Algorithm | Complexity | Note |
|:--|:--|:--|
| Dijkstra, set-based | `O(E log V)` | A set rather than a heap, so a key can be decreased |
| Kruskal with union-find | `O(E log E)` | Path compression makes the cycle test near-constant |
| Kruskal, naive cycle test | `O(E·V)` | Built first on purpose, to show what union-find buys |
| Prim | `O(E log V)` | The same tree, grown instead of assembled |
| BFS and DFS | `O(V+E)` | Java and C++ |
| Multi-source BFS | `O(V+E)` | Seed the queue with every source; the traversal is unchanged |
| Cycle detection, undirected | `O(V+E)` | The parent check is not the visited check |
| Bipartite check | `O(V+E)` | Two-colouring via DFS |
| Connected components | `O(V²)` | On an adjacency matrix |
| Shortest path in a binary maze | `O(R·C)` | BFS on an implicit graph |

[repository →](https://github.com/jaf-git/graphs-data-structure)

</details>

<details>
<summary><code>trees</code> — traversal, construction, path problems</summary>

<br>

| Algorithm | Complexity | Note |
|:--|:--|:--|
| Morris traversal | `O(n)` time, `O(1)` space | Threading the tree instead of carrying a stack |
| Iterative traversal | `O(n)` | Explicit stack, which is what recursion was doing for you |
| B-tree construction | — | Node splitting and order invariants |
| Lowest common ancestor | `O(n)` | Bottom-up, single pass |
| Maximum path sum | `O(n)` | The value returned upward differs from the value recorded |
| Diameter and height | `O(n)` | One post-order pass returning two things |
| Rebuild from in-order and pre-order | `O(n)` | Why that pair is sufficient |
| Rebuild from in-order and post-order | `O(n)` | The mirror argument |
| Children-sum property | `O(n)` | Mutating a tree to satisfy an invariant |
| Identical-tree check | `O(n)` | Structural equality |

[repository →](https://github.com/jaf-git/Trees-Data-Structure)

</details>

<details>
<summary><code>recursion &amp; dp</code> — the full progression</summary>

<br>

Each problem appears first as plain recursion, then memoised, then tabulated, because the route
between them is the lesson.

```
recursion  ──▶  memoise  ──▶  tabulate  ──▶  shrink the table
exponential     top-down      bottom-up      O(1) space
```

| Problem | Technique |
|:--|:--|
| Fibonacci | The canonical progression, exponential to constant space |
| Frog jump | First problem where the recurrence isn't obvious from the statement |
| Subsequence generation | Take or skip, the shape underneath most subset DP |
| Target-sum subsets | The same recursion with a pruning condition |
| Sorting algorithms | C++ |

[recursion →](https://github.com/jaf-git/recursive-algorithms) · [dynamic programming →](https://github.com/jaf-git/Dynamic-Programming)

</details>

<details>
<summary><code>concurrency</code> — threads, synchronisation, coordination</summary>

<br>

| Problem | What it demonstrates |
|:--|:--|
| Dining philosophers | Deadlock comes from an ordering, not from a bug in any one thread |
| Recursive filesystem search | Fan-out where you don't know the fan-out in advance |
| The same, with wait groups | Knowing when work that spawns work has actually finished |
| Parallel page fetching | I/O-bound parallelism, where threads genuinely pay |
| Queue management simulation | Correctness that has to be measured rather than asserted |
| POSIX threads and mutexes | Against the C API directly |

[multithreading →](https://github.com/jaf-git/Multithreading-Space) · [queue simulation →](https://github.com/jaf-git/queues-management-app-using-threads) · [linux →](https://github.com/jaf-git/Linux-OS-Space)

</details>

<details>
<summary><code>coursework</code> — B.Eng. Automation and Computer Science, UTCN</summary>

<br>

| Area | Repository | Language |
|:--|:--|:--|
| Operating systems | [Linux-OS-Space](https://github.com/jaf-git/Linux-OS-Space) | C, Python |
| Computer architecture | [hardware-programming](https://github.com/jaf-git/hardware-programming) | VHDL |
| Computer graphics | [Computer-Graphics](https://github.com/jaf-git/Computer-Graphics) | C, C++ |
| Software design | [polynomial-calculator](https://github.com/jaf-git/polynomial-calculator) · [Orders-Management](https://github.com/jaf-git/Orders-Management-application) | Java |
| Full-stack | [JBank](https://github.com/jaf-git/JBank-Repository) | Java, TypeScript |
| Intelligent systems | [classical](https://github.com/jaf-git/bank-marketing-term-deposit-subscription-prediction) · [neural](https://github.com/jaf-git/bank-marketing-neural-network-classifier) | Python |

Working languages: Arabic (native), English (professional), Romanian (professional).

</details>
