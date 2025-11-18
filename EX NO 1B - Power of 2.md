
# EX 1B Power of 2
## Date:
## Aim:
To write a Java program to for given constraints. Given an integer n, return true if it is a power of two. Otherwise, return false. An integer n is a power of two, if there exists an integer x such that n == 2x.

## Algorithm
1. **Start** the program.
2. **Read** the integer input `n` from the user.
3. **Check** whether `n` is less than or equal to 0; if yes, conclude it is **not** a power of two.
4. **Evaluate** the condition `(n & (n - 1)) == 0` to determine if `n` is a power of two.
5. **Print** the result (true/false) and **stop** the program. 

## Program:
```
Program to implement power of 2

Developed by: Krithick Vivekananda 
Register Number: 212223240075

import java.util.Scanner;

public class Solution {

    public boolean isPowerOfTwo(int n) {
        if (n <= 0) return false;
        return (n & (n - 1)) == 0;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();

        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}
```

## Output:
<img width="435" height="204" alt="image" src="https://github.com/user-attachments/assets/b5c3692e-b0f5-40c2-8975-c40fecfeb6a8" />

## Result:
The program was successfully implemented and the expected output is verified.
