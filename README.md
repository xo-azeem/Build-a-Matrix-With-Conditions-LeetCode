# Build a Matrix With Conditions

LeetCode Q # 2392.

You are given a positive integer k. You are also given:

- a 2D integer array rowConditions of size n where rowConditions[i] = [abovei, belowi], and
- a 2D integer array colConditions of size m where colConditions[i] = [lefti, righti].
  
The two arrays contain integers from 1 to k.

You have to build a k x k matrix that contains each of the numbers from 1 to k exactly once. The remaining cells should have the value 0.

The matrix should also satisfy the following conditions:

- The number abovei should appear in a row that is strictly above the row at which the number belowi appears for all i from 0 to n - 1.
- The number lefti should appear in a column that is strictly left of the column at which the number righti appears for all i from 0 to m - 1.
  
Return any matrix that satisfies the conditions. If no answer exists, return an empty matrix.

Example 1:

<div align = "center">

  ![image](https://github.com/user-attachments/assets/23972b4a-84d0-4187-b194-cfd75cfb9329)

</div>

> Input: k = 3, rowConditions = [[1,2],[3,2]], colConditions = [[2,1],[3,2]]</br>
> Output: [[3,0,0],[0,0,1],[0,2,0]]</br>
> Explanation: The diagram above shows a valid example of a matrix that satisfies all the conditions.</br>
> The row conditions are the following:</br>
> - Number 1 is in row 1, and number 2 is in row 2, so 1 is above 2 in the matrix.</br>
> - Number 3 is in row 0, and number 2 is in row 2, so 3 is above 2 in the matrix.</br>
> The column conditions are the following:</br>
> - Number 2 is in column 1, and number 1 is in column 2, so 2 is left of 1 in the matrix.</br>
> - Number 3 is in column 0, and number 2 is in column 1, so 3 is left of 2 in the matrix.</br>
> Note that there may be multiple correct answers.</br>

Example 2:

> Input: k = 3, rowConditions = [[1,2],[2,3],[3,1],[2,3]], colConditions = [[2,1]]</br>
> Output: []</br>
> Explanation: From the first two conditions, 3 has to be below 1 but the third conditions needs 3 to be above 1 to be satisfied.</br>
> No matrix can satisfy all the conditions, so we return the empty matrix.</br>

My Solution Analysis:

<div align = "center">

![image](https://github.com/user-attachments/assets/10c73e24-7365-419a-ba87-df6aa2e0f01a)

  Time complexity: O(n).</br>Space complexity: O(n).
</div>
