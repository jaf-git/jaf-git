<img src="docs/assets/00-boot.svg" alt="Booting jawad-abo-fakher.jar — Spring Boot startup log: 104 migrations applied, 17 bounded contexts bootstrapped, 265 endpoint handlers mapped, started in 2.418 seconds. Welcome. Jawad Abo Fakher, backend engineer, Java, Spring Boot, PostgreSQL. Available for backend roles 2026, Cluj-Napoca, Romania." width="100%">

<img src="docs/assets/01-whoami.svg" alt="Who am I — Jawad Abo Fakher, backend engineer. B.Eng Automation and Computer Science, UTCN Cluj-Napoca, graduating 2026. Available for backend roles, hybrid or remote. Arabic, English, Romanian." width="100%">

<a href="mailto:abofakherjawad@gmail.com"><img src="docs/assets/cta.svg" alt="Let's create something awesome together — mail abofakherjawad@gmail.com" width="100%"></a>

<img src="docs/assets/02-stack.svg" alt="Tech stack — backend Java 21, Spring Boot 3.5, Security, Data JPA, Flyway. Data PostgreSQL 16. Testing JUnit 5, Testcontainers, ArchUnit, Vitest, Playwright. Systems C, POSIX threads, Linux syscalls, VHDL. Delivery Docker, GitHub Actions, Semgrep, OWASP. ML Python, scikit-learn, Keras. Frontend React 19, TypeScript." width="100%">

<a href="mailto:abofakherjawad@gmail.com"><img src="docs/assets/cta.svg" alt="Let's create something awesome together — mail abofakherjawad@gmail.com" width="100%"></a>

<img src="docs/assets/03-projects.svg" alt="Projects — 4 shown, 16 public repositories." width="100%">

<a href="https://github.com/jaf-git/flowops"><img src="docs/assets/03a-flowops.svg" alt="FlowOps — bachelor thesis. Java 21, Spring Boot 3.5, React 19, PostgreSQL 16. Recovers business processes from the chat people already send. 17 bounded contexts, 265 endpoints, 104 migrations, 506 test files. Hexagonal, ArchUnit, Testcontainers, Flyway." width="100%"></a>

<a href="https://github.com/jaf-git/api-contract-validator"><img src="docs/assets/03b-validator.svg" alt="Validator — IntelliJ Platform plugin in Kotlin. Flags where your controllers and your OpenAPI spec disagree as you type. Runs incrementally on partial files without blocking the event dispatch thread. PSI, Codecov, UI tests in CI." width="100%"></a>

<a href="https://github.com/jaf-git/hardware-programming"><img src="docs/assets/03c-mips.svg" alt="MIPS CPU — digital design in VHDL on FPGA. A 32-bit processor built up from the register file: datapath, control unit, instruction and data memory. Five-stage, waveform-debugged." width="100%"></a>

<a href="https://github.com/jaf-git/bank-marketing-neural-network-classifier"><img src="docs/assets/03d-classifiers.svg" alt="Classifiers — intelligent systems in Python, scikit-learn and Keras. 45,211 records, 11.7 percent positive. Duration dropped as leakage. Best F1 0.4375, ROC-AUC 0.7910 across 9 models compared." width="100%"></a>

<a href="mailto:abofakherjawad@gmail.com"><img src="docs/assets/cta.svg" alt="Let's create something awesome together — mail abofakherjawad@gmail.com" width="100%"></a>

<br>

<details>
<summary><b>Graphs</b> — 10 implementations, Java and C++</summary>

<br>

| Algorithm | Complexity | Note |
|:--|:--|:--|
| Dijkstra, set-based | `O(E log V)` | A set rather than a heap, so a key can be decreased |
| Kruskal with union-find | `O(E log E)` | Path compression makes the cycle test near-constant |
| Kruskal, naive cycle test | `O(E·V)` | Built first on purpose, to show what union-find buys |
| Prim | `O(E log V)` | The same tree, grown instead of assembled |
| BFS and DFS | `O(V+E)` | Written in both languages |
| Multi-source BFS | `O(V+E)` | Seed the queue with every source; the traversal is unchanged |
| Cycle detection, undirected | `O(V+E)` | The parent check is not the visited check |
| Bipartite check | `O(V+E)` | Two-colouring via DFS |
| Connected components | `O(V²)` | On an adjacency matrix |
| Shortest path, binary maze | `O(R·C)` | BFS on an implicit graph |

[graphs-data-structure →](https://github.com/jaf-git/graphs-data-structure)

</details>

<details>
<summary><b>Trees</b> — 10 implementations</summary>

<br>

| Algorithm | Complexity | Note |
|:--|:--|:--|
| Morris traversal | `O(n)` time, `O(1)` space | Threading the tree instead of carrying a stack |
| Iterative traversal | `O(n)` | Explicit stack, which is what recursion was doing for you |
| B-tree construction | — | Node splitting and order invariants |
| Lowest common ancestor | `O(n)` | Bottom-up, single pass |
| Maximum path sum | `O(n)` | The value returned upward differs from the value recorded |
| Diameter and height | `O(n)` | One post-order pass returning two things |
| Rebuild from in-order + pre-order | `O(n)` | Why that pair is sufficient |
| Rebuild from in-order + post-order | `O(n)` | The mirror argument |
| Children-sum property | `O(n)` | Mutating a tree to satisfy an invariant |
| Identical-tree check | `O(n)` | Structural equality |

[Trees-Data-Structure →](https://github.com/jaf-git/Trees-Data-Structure)

</details>

<details>
<summary><b>Recursion, dynamic programming and concurrency</b> — 11 implementations</summary>

<br>

Each problem appears first as plain recursion, then memoised, then tabulated. The route between
them is the lesson.

```
recursion  ──▶  memoise  ──▶  tabulate  ──▶  shrink the table
exponential     top-down      bottom-up      O(1) space
```

| Problem | What it demonstrates |
|:--|:--|
| Fibonacci | The canonical progression, exponential to constant space |
| Frog jump | First problem where the recurrence isn't obvious from the statement |
| Subsequence generation | Take or skip, the shape underneath most subset DP |
| Target-sum subsets | The same recursion with a pruning condition |
| Sorting algorithms | Implemented in C++ |
| Dining philosophers | Deadlock comes from an ordering, not a bug in any one thread |
| Recursive filesystem search | Fan-out where you don't know the fan-out in advance |
| The same, with wait groups | Knowing when work that spawns work has actually finished |
| Parallel page fetching | I/O-bound parallelism, where threads genuinely pay |
| Queue management simulation | Correctness that has to be measured rather than asserted |
| POSIX threads and mutexes | Against the C API directly |

[recursive-algorithms →](https://github.com/jaf-git/recursive-algorithms) · [Dynamic-Programming →](https://github.com/jaf-git/Dynamic-Programming) · [Multithreading-Space →](https://github.com/jaf-git/Multithreading-Space) · [queues-management →](https://github.com/jaf-git/queues-management-app-using-threads)

</details>

<details>
<summary><b>Coursework</b> — B.Eng. Automation and Computer Science, UTCN</summary>

<br>

| Area | Repository | Language |
|:--|:--|:--|
| Operating systems | [Linux-OS-Space](https://github.com/jaf-git/Linux-OS-Space) | C, Python |
| Computer architecture | [hardware-programming](https://github.com/jaf-git/hardware-programming) | VHDL |
| Computer graphics | [Computer-Graphics](https://github.com/jaf-git/Computer-Graphics) | C, C++ |
| Software design | [polynomial-calculator](https://github.com/jaf-git/polynomial-calculator) · [Orders-Management](https://github.com/jaf-git/Orders-Management-application) | Java |
| Full-stack | [JBank](https://github.com/jaf-git/JBank-Repository) | Java, TypeScript |
| Intelligent systems | [classical models](https://github.com/jaf-git/bank-marketing-term-deposit-subscription-prediction) · [neural network](https://github.com/jaf-git/bank-marketing-neural-network-classifier) | Python |

Arabic (native) · English (C1) · Romanian (C1) · German (A2)

</details>

<br>

<div align="center">

**[abofakherjawad@gmail.com](mailto:abofakherjawad@gmail.com)** &nbsp;·&nbsp; **[LinkedIn](https://linkedin.com/in/jawadabofakher)** &nbsp;·&nbsp; Cluj-Napoca, Romania

</div>
