
# EX 1A Print All Numbers 
## Date:
## Aim:
To write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line.

## Algorithm
1. **Start** the program.
2. **Input** an integer value `n` from the user using the scanner.
3. **Set** a loop counter `i = 1`.
4. **Repeat** printing `i` and incrementing it by 1 until `i > n`.
5. **Stop** the program.

## Program:
```
Program to print all numbers

Developed by: Krithick Vivekananda 
Register Number: 212223240075

import java.util.Scanner;
public class PrintNumbers {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int N = scanner.nextInt();
        if (N <= 0) {
            System.out.println("Invalid input. N must be greater than 0.");
        } else {
            for (int i = 1; i <= N; i++) {
                System.out.print(i + " ");
            }
        }
        scanner.close();
    }
}
```

## Output:
<img width="526" height="164" alt="image" src="https://github.com/user-attachments/assets/7edd77b8-ba62-4210-90d3-e465a0081d77" />

## Result:
The program successfully prints all the numbers from 1 to N. 
