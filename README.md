# LeetCode 123 – Best Time to Buy and Sell Stock III

## Problem

You are given an array `prices` where `prices[i]` represents the price of a stock on the `i`th day.

You may complete **at most two transactions**.

A transaction consists of buying one stock and selling it. You must sell the stock before buying again.

Return the maximum profit that can be achieved.

## Example 1

**Input:**

```text
prices = [3,3,5,0,0,3,1,4]
```

**Output:**

```text
6
```

One optimal choice is:

```text
Buy at 0 → Sell at 3 = 3
Buy at 1 → Sell at 4 = 3
```

Total profit:

```text
3 + 3 = 6
```

## Example 2

**Input:**

```text
prices = [1,2,3,4,5]
```

**Output:**

```text
4
```

Only one transaction is needed:

```text
Buy at 1 → Sell at 5 = 4
```

## Example 3

**Input:**

```text
prices = [7,6,4,3,1]
```

**Output:**

```text
0
```

No profitable transaction is possible.

## Approach

Since at most two transactions are allowed, we can track four important states:

1. First buy
2. First sell
3. Second buy
4. Second sell

As we scan the array, these values are updated to represent the best possible profit at each stage.

The final value after the second sell represents the maximum profit.

## Algorithm

* Initialize the four transaction states.
* For every stock price:

  * Update the best price/profit for the first purchase.
  * Update the profit after the first sale.
  * Update the second purchase using the first transaction's profit.
  * Update the profit after the second sale.
* Return the profit after the second sale.

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(1)`

Only a constant number of variables are maintained.

## Key Learning

This problem introduces **state-based Dynamic Programming** for stock trading.

Instead of considering every possible combination of transactions, we maintain the best result after each transaction stage.

## LeetCode Details

* **Problem Number:** 123
* **Problem Name:** Best Time to Buy and Sell Stock III
* **Difficulty:** Hard
* **Language:** Python 3
* **File:** `solution.py`

## Topics

* Array
* Dynamic Programming

## Author

T.Nandhini
