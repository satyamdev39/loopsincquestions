# Do While Loop Practice Questions in C

## Introduction

The `do while` loop is used to execute a block of code at least once, even if the condition is false.

### Syntax

```c
do {
    // Statements
} while(condition);
```

**Important:** A semicolon (`;`) is required after the `while` condition.

---

# Basic Level

### Q1. Print a message 5 times using a do while loop.

**Solution:**

```c
#include <stdio.h>

int main() {
    int i = 1;

    do {
        printf("Hello World\n");
        i++;
    } while(i <= 5);

    return 0;
}
```

**Output:**

```text
Hello World
Hello World
Hello World
Hello World
Hello World
```

---

### Q2. Print numbers from 50 to 60.

**Solution:**

```c
#include <stdio.h>

int main() {
    int i = 50;

    do {
        printf("%d ", i);
        i++;
    } while(i <= 60);

    return 0;
}
```

**Output:**

```text
50 51 52 53 54 55 56 57 58 59 60
```

---

### Q3. Print numbers from 100 to 90 in reverse order.

**Solution:**

```c
#include <stdio.h>

int main() {
    int i = 100;

    do {
        printf("%d ", i);
        i--;
    } while(i >= 90);

    return 0;
}
```

**Output:**

```text
100 99 98 97 96 95 94 93 92 91 90
```

---

### Q4. Print multiples of 7 from 1 to 70.

**Solution:**

```c
#include <stdio.h>

int main() {
    int i = 7;

    do {
        printf("%d ", i);
        i += 7;
    } while(i <= 70);

    return 0;
}
```

**Output:**

```text
7 14 21 28 35 42 49 56 63 70
```

---

### Q5. Print numbers divisible by both 3 and 5 from 1 to 150.

**Solution:**

```c
#include <stdio.h>

int main() {
    int i = 1;

    do {
        if(i % 3 == 0 && i % 5 == 0) {
            printf("%d ", i);
        }
        i++;
    } while(i <= 150);

    return 0;
}
```

**Output:**

```text
15 30 45 60 75 90 105 120 135 150
```

---

### Q6. Print the first 10 multiples of a user-entered number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, i = 1;

    printf("Enter a number: ");
    scanf("%d", &n);

    do {
        printf("%d x %d = %d\n", n, i, n * i);
        i++;
    } while(i <= 10);

    return 0;
}
```

**Example Output:**

```text
Enter a number: 5
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
...
5 x 10 = 50
```

---

# Intermediate Level

### Q7. Find the sum of squares of numbers from 1 to N.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, i = 1;
    int sum = 0;

    printf("Enter N: ");
    scanf("%d", &n);

    do {
        sum += i * i;
        i++;
    } while(i <= n);

    printf("Sum of squares = %d", sum);

    return 0;
}
```

**Example Output:**

```text
Enter N: 5
Sum of squares = 55
```

---

### Q8. Find the sum of cubes of numbers from 1 to N.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, i = 1;
    int sum = 0;

    printf("Enter N: ");
    scanf("%d", &n);

    do {
        sum += i * i * i;
        i++;
    } while(i <= n);

    printf("Sum of cubes = %d", sum);

    return 0;
}
```

**Example Output:**

```text
Enter N: 3
Sum of cubes = 36
```

---

### Q9. Count how many times a number can be divided by 2 before becoming zero.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, count = 0;

    printf("Enter a positive number: ");
    scanf("%d", &n);

    if(n <= 0) {
        printf("Enter a positive number.");
        return 0;
    }

    do {
        n = n / 2;
        count++;
    } while(n > 0);

    printf("Number of divisions = %d", count);

    return 0;
}
```

**Example Output:**

```text
Enter a positive number: 20
Number of divisions = 5
```

---

### Q10. Find the sum of numbers entered by the user until zero is entered.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, sum = 0;

    do {
        printf("Enter a number (0 to stop): ");
        scanf("%d", &n);

        sum += n;

    } while(n != 0);

    printf("Total sum = %d", sum);

    return 0;
}
```

**Example Output:**

```text
Enter a number (0 to stop): 10
Enter a number (0 to stop): 20
Enter a number (0 to stop): 30
Enter a number (0 to stop): 0
Total sum = 60
```

---

### Q11. Find the average of positive numbers entered by the user. Stop when zero or a negative number is entered.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, count = 0;
    float sum = 0, average;

    do {
        printf("Enter a positive number (0 or negative to stop): ");
        scanf("%d", &n);

        if(n > 0) {
            sum += n;
            count++;
        }

    } while(n > 0);

    if(count > 0) {
        average = sum / count;
        printf("Average = %.2f", average);
    } else {
        printf("No positive numbers entered.");
    }

    return 0;
}
```

**Example Output:**

```text
Enter a positive number (0 or negative to stop): 10
Enter a positive number (0 or negative to stop): 20
Enter a positive number (0 or negative to stop): 30
Enter a positive number (0 or negative to stop): 0
Average = 20.00
```

---

### Q12. Find the power of a number without using the pow() function.

**Solution:**

```c
#include <stdio.h>

int main() {
    int base, exponent, i = 1;
    long long result = 1;

    printf("Enter base: ");
    scanf("%d", &base);

    printf("Enter exponent (non-negative): ");
    scanf("%d", &exponent);

    if(exponent < 0) {
        printf("Negative exponent is not supported.");
        return 0;
    }

    do {
        if(i > exponent) {
            break;
        }

        result *= base;
        i++;

    } while(i <= exponent);

    printf("Result = %lld", result);

    return 0;
}
```

**Example Output:**

```text
Enter base: 2
Enter exponent (non-negative): 5
Result = 32
```

---

### Q13. Find the HCF of two positive numbers using repeated subtraction.

**Solution:**

```c
#include <stdio.h>

int main() {
    int a, b;

    printf("Enter two positive numbers: ");
    scanf("%d %d", &a, &b);

    if(a <= 0 || b <= 0) {
        printf("Enter positive numbers only.");
        return 0;
    }

    do {
        if(a > b) {
            a = a - b;
        } else if(b > a) {
            b = b - a;
        }
    } while(a != b);

    printf("HCF = %d", a);

    return 0;
}
```

**Example Output:**

```text
Enter two positive numbers: 24 18
HCF = 6
```

---

### Q14. Check whether a number is a strong number.

A strong number is a number whose sum of the factorials of its digits equals the original number.

Example: 145 = 1! + 4! + 5! = 145.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, original, digit;
    int sum = 0, fact, i;

    printf("Enter a number: ");
    scanf("%d", &n);

    if(n < 0) {
        printf("Negative numbers are not supported.");
        return 0;
    }

    original = n;

    do {
        digit = n % 10;
        fact = 1;
        i = 1;

        do {
            if(i > digit) {
                break;
            }

            fact *= i;
            i++;

        } while(i <= digit);

        sum += fact;
        n /= 10;

    } while(n > 0);

    if(sum == original) {
        printf("%d is a Strong Number.", original);
    } else {
        printf("%d is not a Strong Number.", original);
    }

    return 0;
}
```

**Example Output:**

```text
Enter a number: 145
145 is a Strong Number.
```

---

# Advanced Level

### Q15. Create a menu-driven calculator using do while.

**Solution:**

```c
#include <stdio.h>

int main() {
    int choice;
    float a, b;

    do {
        printf("\n--- Calculator Menu ---\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Exit\n");

        printf("Enter your choice: ");
        scanf("%d", &choice);

        if(choice >= 1 && choice <= 4) {
            printf("Enter two numbers: ");
            scanf("%f %f", &a, &b);
        }

        switch(choice) {
            case 1:
                printf("Result = %.2f\n", a + b);
                break;

            case 2:
                printf("Result = %.2f\n", a - b);
                break;

            case 3:
                printf("Result = %.2f\n", a * b);
                break;

            case 4:
                if(b != 0) {
                    printf("Result = %.2f\n", a / b);
                } else {
                    printf("Division by zero is not allowed.\n");
                }
                break;

            case 5:
                printf("Calculator closed.\n");
                break;

            default:
                printf("Invalid choice.\n");
        }

    } while(choice != 5);

    return 0;
}
```

---

### Q16. Create a number guessing game.

The user must guess a fixed secret number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int secret = 25;
    int guess;

    do {
        printf("Guess the number (1-50): ");
        scanf("%d", &guess);

        if(guess < secret) {
            printf("Too low! Try again.\n");
        } else if(guess > secret) {
            printf("Too high! Try again.\n");
        } else {
            printf("Correct! You guessed it.\n");
        }

    } while(guess != secret);

    return 0;
}
```

**Example Output:**

```text
Guess the number (1-50): 10
Too low! Try again.
Guess the number (1-50): 40
Too high! Try again.
Guess the number (1-50): 25
Correct! You guessed it.
```

---

### Q17. Create a login system with a maximum of 3 attempts.

**Solution:**

```c
#include <stdio.h>

int main() {
    int password = 1234;
    int entered, attempts = 0;

    do {
        printf("Enter password: ");
        scanf("%d", &entered);

        attempts++;

        if(entered == password) {
            printf("Login successful!\n");
            break;
        } else {
            printf("Incorrect password.\n");
        }

    } while(attempts < 3);

    if(entered != password) {
        printf("Account locked!\n");
    }

    return 0;
}
```

**Example Output:**

```text
Enter password: 1111
Incorrect password.
Enter password: 2222
Incorrect password.
Enter password: 1234
Login successful!
```

---

### Q18. Create a simple ATM menu.

**Solution:**

```c
#include <stdio.h>

int main() {
    int choice;
    float balance = 5000, amount;

    do {
        printf("\n--- ATM MENU ---\n");
        printf("1. Check Balance\n");
        printf("2. Deposit Money\n");
        printf("3. Withdraw Money\n");
        printf("4. Exit\n");

        printf("Enter choice: ");
        scanf("%d", &choice);

        switch(choice) {
            case 1:
                printf("Balance = %.2f\n", balance);
                break;

            case 2:
                printf("Enter deposit amount: ");
                scanf("%f", &amount);

                if(amount > 0) {
                    balance += amount;
                    printf("Money deposited successfully.\n");
                } else {
                    printf("Invalid amount.\n");
                }
                break;

            case 3:
                printf("Enter withdrawal amount: ");
                scanf("%f", &amount);

                if(amount > 0 && amount <= balance) {
                    balance -= amount;
                    printf("Please collect your money.\n");
                } else {
                    printf("Invalid amount or insufficient balance.\n");
                }
                break;

            case 4:
                printf("Thank you for using ATM.\n");
                break;

            default:
                printf("Invalid choice.\n");
        }

    } while(choice != 4);

    return 0;
}
```

---

### Q19. Generate a Fibonacci sequence until the user chooses to stop.

**Solution:**

```c
#include <stdio.h>

int main() {
    int a = 0, b = 1, c;
    int n, i = 1;

    printf("How many terms? ");
    scanf("%d", &n);

    if(n <= 0) {
        printf("Enter a positive number.");
        return 0;
    }

    do {
        printf("%d ", a);

        c = a + b;
        a = b;
        b = c;

        i++;

    } while(i <= n);

    return 0;
}
```

**Example Output:**

```text
How many terms? 7
0 1 1 2 3 5 8
```

---

### Q20. Make a quiz program that asks questions until the user chooses to exit.

**Solution:**

```c
#include <stdio.h>

int main() {
    int choice;
    int score = 0;

    do {
        printf("\n--- Simple Quiz ---\n");
        printf("1. What is 5 + 5?\n");
        printf("2. What is 10 * 2?\n");
        printf("3. What is 20 / 4?\n");
        printf("4. Exit Quiz\n");

        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch(choice) {
            case 1:
                score++;
                printf("Correct! Score = %d\n", score);
                break;

            case 2:
                score++;
                printf("Correct! Score = %d\n", score);
                break;

            case 3:
                score++;
                printf("Correct! Score = %d\n", score);
                break;

            case 4:
                printf("Quiz finished. Final score = %d\n", score);
                break;

            default:
                printf("Invalid choice.\n");
        }

    } while(choice != 4);

    return 0;
}
```

---

# Important Do While Loop Concepts

| Concept | Description |
|---|---|
| `do` | Starts the loop body |
| `while` | Checks the condition |
| Semicolon (`;`) | Required after the while condition |
| `break` | Terminates the loop |
| `continue` | Skips the remaining statements in the current iteration |
| Nested do while | A do while loop inside another do while loop |

---


## Difference Between While and Do While

| While Loop | Do While Loop |
|---|---|
| Entry-controlled loop | Exit-controlled loop |
| Checks condition before execution | Checks condition after execution |
| May execute zero times | Executes at least once |
| No semicolon after condition | Semicolon required after condition |

