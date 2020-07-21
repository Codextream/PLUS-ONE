# PLUS ONE


Given a non-empty array of digits representing a non-negative integer, increment one to the integer.

The digits are stored such that the most significant digit is at the head of the list, and each element in the array contains a single digit.

You may assume the integer does not contain any leading zero, except the number 0 itself.

### Example 1:
<pre>
Input: [1,2,3]
Output: [1,2,4]
Explanation: The array represents the integer 123.
</pre>

### Example 2:
<pre>
Input: [4,3,2,1]
Output: [4,3,2,2]
Explanation: The array represents the integer 4321.
</pre>

### Solution:

```cpp

class Solution {
public:
    vector<int> plusOne(vector<int> &digits) {
        int c = 1;
        for (int i = digits.size() - 1; i >= 0; i--) {
            digits[i] += c;
            c = digits[i] / 10;
            digits[i] = digits[i] % 10;
        }
        if (c > 0) digits.insert(digits.begin(), c);
        return digits;
    }
};

```
