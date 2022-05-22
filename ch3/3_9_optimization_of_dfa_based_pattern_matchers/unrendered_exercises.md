# Optimization of DFA-based Pattern Matchers

## 3.9.1

Extend the table of Fig. 3.58 to include the operators (a)? and (b)+.

| Node *n*                    | *nullable(n)* | *firstpos(n)* |
| --------------------------- | ------------- | ------------- |
| A zero-or-one node n = (a)? | true          | firstpos(a)   |
| A one-or-more node n = (b)+ | nullable(b)   | firstpos(b)   |

## 3.9.2

Use Algorithm 3.36 to convert the regular expressions of Exercise 3.7.3
directly to deterministic finite automata.

a) $$(a | b)^*$$

There is [a good solution](https://github.com/fool2fish/dragon-book-exercise-answers/blob/master/ch03/3.9/3.9.md#392).

b) $$(a^* | b^*)^*$$

This is equivalent to the above one.

c) $$((\epsilon | a) b^*)^*$$

This is also equivalent to the first one.

d) $$(a | b)^*abb(a | b)^*$$

| Position n | followpos(n)  |
| ---------- | ------------- |
| 1          | {1, 2, 3}     |
| 2          | {1, 2, 3}     |
| 3          | {4}           |
| 4          | {5}           |
| 5          | {6, 7, 8}     |
| 6          | {6, 7, 8}     |
| 7          | {6, 7, 8}     |
| 8          | $$\emptyset$$ |

| State                 | a                     | b                     |
| --------------------- | --------------------- | --------------------- |
| {1, 2, 3}             | {1, 2, 3, 4}          | {1, 2, 3}             |
| {1, 2, 3, 4}          | {1, 2, 3, 4}          | {1, 2, 3, 5}          |
| {1, 2, 3, 5}          | {1, 2, 3, 4}          | {1, 2, 3, 6, 7, 8}    |
| {1, 2, 3, 6, 7, 8}    | {1, 2, 3, 4, 6, 7, 8} | {1, 2, 3, 6, 7, 8}    |
| {1, 2, 3, 4, 6, 7, 8} | {1, 2, 3, 4, 6, 7, 8} | {1, 2, 3, 5, 6, 7, 8} |
| {1, 2, 3, 5, 6, 7, 8} | {1, 2, 3, 4, 6, 7, 8} | {1, 2, 3, 6, 7, 8}    |
