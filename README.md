# Puls Pattern - Java Star Pattern Program

## Overview
This Java program generates a star pattern resembling a pulse symbol using nested loops. The user provides an input size, and the program prints a pattern where a vertical line of stars (`*`) is placed in the center column, and a horizontal line appears in the middle row.

## Features
- Takes user input for the size of the pattern.
- Uses nested loops to print the pattern.
- Implements conditional statements to determine where stars should be placed.
- Uses `Scanner` to take user input dynamically.

## Code Explanation
### 1. Importing Scanner
The `java.util.Scanner` class is imported to take user input from the console.
```java
import java.util.Scanner;
```

### 2. Class and Main Method
The program is encapsulated in a class named `PulsPattern`, with the `main` method serving as the entry point.
```java
public class PulsPattern
{
    public static void main(String[] args)
    {
```

### 3. Scanner Input
A `Scanner` object is created to read user input, which determines the size of the pattern.
```java
        Scanner s = new Scanner(System.in);
        System.out.println("Enter the Size");
        int n = s.nextInt();
```

### 4. Outer Loop - Controlling Rows
The outer loop runs from `0` to `n`, iterating over each row.
```java
        for(int i = 0; i <= n; i++)
        {
```

### 5. Inner Loop - Controlling Columns
The inner loop runs from `1` to `n`, iterating over each column in a row.
```java
            for(int j = 1; j <= n; j++)
            {
```

### 6. Condition for Printing Stars
The program checks two conditions:
- If `j == (n/2) + 1`, it prints `*` to create a vertical line at the center column.
- If `i == n/2`, it prints `*` to form a horizontal line at the middle row.
```java
                if(j == (n/2) + 1 || i == n/2)
                    System.out.print("*");
                else
                    System.out.print(" ");
```

### 7. Printing New Lines
After printing each row, `System.out.println()` is used to move to the next line.
```java
            }
            System.out.println();
        }
```

### 8. Closing the Scanner
The `Scanner` object is closed to prevent resource leaks.
```java
        s.close();
    }
}
```

## Example Output
For `n = 5`, the program prints:
```
  *  
  *  
*****
  *  
  *  
```

## Notes
- The size `n` should be an odd number for proper symmetry.
- For even numbers, the middle row and column placement may vary slightly.

## Conclusion
This program demonstrates basic Java concepts such as loops, conditional statements, and user input handling. It is useful for understanding pattern printing logic and nested loops in Java.

## Clone
```
git clone https://github.com/Ananthadatta02/Java-Plus_Patters.git
```
