# LC-edit_distance
LeetCode 72 - Edit Distance
Problem
Convert word1 into word2 using minimum operations.

We can:
Insert a character
Delete a character
Replace a character

Example
word1 = "horse"
word2 = "ros"
Output = 3
Approach
I used Dynamic Programming.
dp[i][j] means the minimum operations needed to convert the first i characters of word1 into the first j characters of word2.
If characters are same:

dp[i][j] = dp[i-1][j-1];

If characters are different, we choose the minimum from:

Insert
Delete
Replace
dp[i][j] = 1 + Math.min(
    dp[i][j-1],
    Math.min(dp[i-1][j], dp[i-1][j-1])
);
Complexity
Time: O(m × n)
Space: O(m × n)
