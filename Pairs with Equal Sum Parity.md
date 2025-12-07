**Pairs with Equal Sum Parity**

**Concept:**  
 Basic counting/combinatorics, using frequencies of even/odd numbers.

#### **Problem Statement**

You are given an array of nnn integers. A pair of indices (i,j)(i, j)(i,j) (with 1≤i\<j≤n1 \\le i \< j \\le n1≤i\<j≤n) is called **good** if the sum ai+aja\_i \+ a\_jai​+aj​ is **even**.

Find the **number of good pairs**.

#### **Input Format**

* First line: integer ttt – number of test cases.

* For each test case:

  * First line: integer nnn – number of elements.

  * Second line: nnn integers a1,a2,…,ana\_1, a\_2, \\dots, a\_na1​,a2​,…,an​.

#### **Output Format**

For each test case, print a single integer — the number of good pairs.

#### **Constraints**

* 1 ≤ t ≤ 10^4 

* 1≤n≤2⋅10^5

* ∣ai∣ ≤ 10^9

* Sum of n over all test cases ≤ 2⋅10^5

#### **Sample Input**

2

4

1 2 3 4

5

2 2 2 3 3

#### **Sample Output**

`2`

`4`

#### **Explanation**

* Test 1: Array \= \[1, 2, 3, 4\]  
   Even numbers: 2, 4 → 2 numbers  
   Odd numbers: 1, 3 → 2 numbers  
   Good pairs: (1,3), (2,4) → 2 pairs.

* Test 2: Array \= \[2,2,2,3,3\]  
   Even count \= 3 → C(3,2) \= 3 pairs  
   Odd count \= 2 → C(2,2) \= 1 pair  
   Total \= 4\.

#### **Hints** 

* Sum is even if:

  * even \+ even, or

  * odd \+ odd.

* Let `even` \= \# of even numbers, `odd` \= \# of odd numbers.

* Number of ways to choose 2 even numbers: `even * (even - 1) / 2`.

* Similarly for odd.

* Answer \= C(even,2) \+ C(odd,2).  
   No need for O(n²) pair checking.

