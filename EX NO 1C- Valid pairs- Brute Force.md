
# EX 1C Valid Pairs using Brute Force Approach
## Date:
## Aim:
To write a Java program to for given constraints. Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k. The value of |x| is defined as:
```
x if x >= 0.
-x if x < 0.
```

## Algorithm
1. **Start** the program.
2. **Input** the array size `n`, then read `n` integers into the array, and read the value of `k`.
3. **Initialize** a counter `count = 0` to store the number of valid pairs.
4. **Compare** every pair of elements in the array; if the absolute difference between any two numbers equals `k`, increment `count`.
5. **Print** the final count and **stop** the program.  

## Program:
```
Program to count valid pairs

Developed by: Krithick Vivekananda 
Register Number: 212223240075

import java.util.Scanner;
public class CountPairsWithDifference {
    public static int countKDifference(int[] nums, int k) {
        int count = 0;
        for (int i = 0; i < nums.length; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if (Math.abs(nums[i] - nums[j]) == k) {
                    count++;
                }
            }
        }
        return count;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int result = countKDifference(nums, k);
        System.out.println(result);
        sc.close();
    }
}
```

## Output:
<img width="518" height="294" alt="image" src="https://github.com/user-attachments/assets/7ba133e7-c835-4372-843e-df4a6d369489" />

## Result:
The program was successfully implemented and the expected output is verified.
