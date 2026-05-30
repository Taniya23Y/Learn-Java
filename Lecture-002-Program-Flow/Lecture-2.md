# Java: Algorithms, Pseudocode, and Flow Charts

This document covers the foundational topics related to algorithms, including types like brute force and greedy algorithms, pseudocode, and flow charts.

---

## 1. Algorithm

An **algorithm** is a step-by-step procedure for solving a problem or performing a task in a finite amount of time.

### 1.1 Brute Force Algorithm

#### Definition:

The brute force algorithm is the simplest and most straightforward way of solving a problem by trying all possible solutions and selecting the best one.

#### Characteristics:

- Easy to implement.
- Works well for small problem sizes.
- May become inefficient as the input size grows.

#### Example: Finding the Maximum Element in an Array

```java
public class BruteForceExample {
    public static void main(String[] args) {
        int[] numbers = {10, 20, 30, 40, 50};
        int max = numbers[0];

        for (int number : numbers) {
            if (number > max) {
                max = number;
            }
        }

        System.out.println("Maximum value is: " + max);
    }
}
```

### 1.2 Greedy Algorithm

- Definition:
  The greedy algorithm makes the best possible choice at each step, hoping to arrive at the global optimum solution.

- Characteristics:
  Fast and efficient for problems that exhibit the greedy-choice property.
  Does not guarantee the best solution for all problems.
  Example: Coin Change Problem

```java
import java.util.\*;
public class GreedyExample {
public static void main(String[] args) {
int[] coins = {1, 5, 10, 25};
int amount = 63;
List<Integer> result = new ArrayList<>();

        for (int i = coins.length - 1; i >= 0; i--) {
            while (amount >= coins[i]) {
                amount -= coins[i];
                result.add(coins[i]);
            }
        }

        System.out.println("Coins used: " + result);
    }

}

```

---

### 2. Pseudocode

Pseudocode is a high-level description of an algorithm that uses plain language and resembles programming concepts.

Example: Finding the Sum of Two Numbers

```
START

1. Input two numbers: num1, num2
2. Compute the sum: sum = num1 + num2
3. Output the sum
   END

```

```java
Corresponding Java Code

import java.util.Scanner;

public class PseudocodeExample {
public static void main(String[] args) {
Scanner scanner = new Scanner(System.in);
System.out.print("Enter first number: ");
int num1 = scanner.nextInt();
System.out.print("Enter second number: ");
int num2 = scanner.nextInt();
int sum = num1 + num2;
System.out.println("Sum: " + sum);
}
}
```

---

### 3. Flow Chart

A flow chart is a graphical representation of an algorithm using symbols to show steps and their sequence.

- Example: Flow Chart for Finding the Maximum of Two Numbers

```
  Steps:
  Start
  Input two numbers: num1, num2
  Compare num1 and num2
  If num1 > num2, output num1
  Else, output num2
  End
```

- Flow Chart Symbols:
  ```
  Oval: Start/End.
  Parallelogram: Input/Output.
  Rectangle: Process.
  Diamond: Decision.
  Example in Java
  ```

```java
import java.util.Scanner;

public class FlowChartExample {
public static void main(String[] args) {
Scanner scanner = new Scanner(System.in);
System.out.print("Enter first number: ");
int num1 = scanner.nextInt();
System.out.print("Enter second number: ");
int num2 = scanner.nextInt();

     if (num1 > num2) {
         System.out.println("Maximum is: " + num1);
     } else {
         System.out.println("Maximum is: " + num2);
     }

}

}
```

---

### Summary

#### Algorithm:

Brute force algorithms are straightforward but inefficient for large inputs.
Greedy algorithms are faster but not always optimal.

#### Pseudocode:

Provides a clear and simple way to describe algorithms.

#### Flow Chart:

Visualizes the flow of an algorithm, making it easier to understand.
By understanding these concepts, you'll have a solid foundation for designing and implementing efficient algorithms in Java.
