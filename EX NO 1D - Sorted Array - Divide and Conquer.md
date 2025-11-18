
# EX 1D Sorted Array using Divide and Conquer Approach
## Date:
## Aim:
To write a Java program to for given constraints. Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.
The overall run time complexity should be O(log(m+n)).

## Algorithm
1. **Start** the program and input the sizes of the two arrays, then read the sorted elements into `nums1` and `nums2`.
2. **Initialize** two pointers (`p1` and `p2`) to track the current positions in both arrays.
3. **Extract** the smaller value between the current elements of both arrays using the `getMin()` method, which also moves the corresponding pointer forward.
4. **Repeat** the extraction process until reaching the middle of the combined sorted array; compute the median depending on whether the total number of elements is even or odd.
5. **Print** the calculated median and **stop** the program. 

## Program:
```
Program to find median of two sorted arrays

Developed by: Krithick Vivekananda 
Register Number: 212223240075

import java.util.Scanner;

public class Solution {
    private int p1 = 0, p2 = 0;

    // Get the smaller value between nums1[p1] and nums2[p2], and move the pointer forward
    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; // Should not reach here if input is valid
    }

    // Main logic to find median of two sorted arrays
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
        int m = nums1.length, n = nums2.length;
        int total = m + n;

        if (total % 2 == 0) {
            for (int i = 0; i < total / 2 - 1; ++i) {
                getMin(nums1, nums2);
            }
            return (double) (getMin(nums1, nums2) + getMin(nums1, nums2)) / 2;
        } else {
            for (int i = 0; i < total / 2; ++i) {
                getMin(nums1, nums2);
            }
            return getMin(nums1, nums2);
        }
    }

    // Main method with user input
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        // Input for nums1
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }

        // Input for nums2
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        // Find and display the median
        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
} 
```

## Output:
<img width="905" height="340" alt="image" src="https://github.com/user-attachments/assets/1bbcc91f-b8e5-44bf-b3d4-7272828291f2" />

## Result:
The program was successfully implemented and the expected output is verified.
