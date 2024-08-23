# Fibonacci
The **Fibonacci sequence** is a  mathematical pattern that appears a lot in art and biology. 

- The sequence starts with **1, 1** (or sometimes **0, 1**), and each subsequent number is the **sum of the two preceding ones**.
- So it goes like this: **1, 1, 2, 3, 5, 8, 13, 21, ...**
- These numbers are called **Fibonacci numbers** (often denoted as $$F_n$$).
- The sequence pops up in nature (think sunflower spirals, pinecones, and seashells) and even in financial markets.
- The **golden ratio** (approximately 1.618) emerges from the ratios between successive Fibonacci terms.

1. $$F_0 = 0$$
2. $$F_1 = 1$$
3. $$F_2 = 1$$
4. $$F_3 = 2$$
5. $$F_4 = 3$$
6. $$F_5 = 5$$
7. $$F_6 = 8$$
8. $$F_7 = 13$$
9. $$F_8 = 21$$
10. $$F_9 = 34$$
11. $$F_{10} = 55$$
12. $$F_{11} = 89$$
13. $$F_{12} = 144$$
14. $$F_{13} = 233$$
15. $$F_{14} = 377$$
16. $$F_{15} = 610$$
---

```js
function fibonacci(num) {
    let num1 = 0;
    let num2 = 1;
    let sum;

    if (num === 1) {
        return [num1];
    } else if (num === 2) {
        return [num1, num2];
    } else {
        const fibonacciSeries = [num1, num2];
        for (let i = 3; i <= num; i++) {
            sum = num1 + num2;
            num1 = num2;
            num2 = sum;
            fibonacciSeries.push(sum);
        }
        return fibonacciSeries;
    }
}

console.log(fibonacci(10)); // Example: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]

```
---

```js
function fibonacciRecursive(num) {
    if (num === 0) {
        return 0;
    } else if (num === 1) {
        return 1;
    } else {
        return fibonacciRecursive(num - 1) + fibonacciRecursive(num - 2);
    }
}

// Example usage:
const termIndex = 10; // Change this to the desired term index
for (let i = 0; i <= termIndex; i++) {
    console.log(`Fibonacci(${i}) = ${fibonacciRecursive(i)}`);
}

```
---

```js
function fibonacciIterative(num) {
    if (num === 0) {
        return [0];
    } else if (num === 1) {
        return [0, 1];
    }

    const fibonacciSeries = [0, 1];
    let i = 2;

    while (i <= num) {
        const nextTerm = fibonacciSeries[i - 1] + fibonacciSeries[i - 2];
        fibonacciSeries.push(nextTerm);
        i++;
    }

    return fibonacciSeries;
}

console.log(fibonacciIterative(10)); // Example: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]

```