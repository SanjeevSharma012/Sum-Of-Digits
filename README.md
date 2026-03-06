# Sum of Digits

## Problem Description
Given an integer `n`, calculate the **sum of its digits**.

The task is to repeatedly extract the last digit of the number and add it to a running sum until the number becomes `0`.

---

## Approach
1. Initialize a variable `sum = 0`.
2. Use a `while` loop until `n` becomes `0`.
3. Extract the last digit using `n % 10`.
4. Add it to `sum`.
5. Remove the last digit using `n /= 10`.
6. Return the final `sum`.

---

## Java Implementation

```java
class Solution {
    static int sumOfDigits(int n) {
        int sum = 0;
        
        while (n != 0) {
            sum += n % 10; // get last digit
            n /= 10;       // remove last digit
        }
        
        return sum;
    }
}
Complexity Analysis

Time Complexity:
O(d)
Where d is the number of digits in n.

Space Complexity:
O(1) (constant space)

Author
Sanjeev Sharma
