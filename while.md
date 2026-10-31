# While Loop Practice Questions in C

## Introduction

Practice C programming questions using the `while` loop.

A `while` loop executes a block of code repeatedly as long as the given condition is true. 

### Syntax

```c
initialization;

while (condition) {
    // Statements
    // Increment or decrement
}
```

---

# Basic Level

### Q1. Print numbers from 1 to 10.

**Concept:** Basic while loop

**Solution:**

```c
#include <stdio.h>

int main() {
    int i = 1;

    while (i <= 10) {
        printf("%d\n", i);
        i++;
    }

    return 0;
}
```

**Output:**

```text
1
2
3
4
5
6
7
8
9
10
```

### Q2. Print numbers from 10 to 1.

**Solution:**

```c
#include <stdio.h>

int main() {
    int i = 10;

    while (i >= 1) {
        printf("%d\n", i);
        i--;
    }

    return 0;
}
```

**Output:**

```text
10
9
8
7
6
5
4
3
2
1
```

### Q3. Print even numbers from 1 to 50.

**Solution:**

```c
#include <stdio.h>

int main() {
    int i = 2;

    while (i <= 50) {
        printf("%d\n", i);
        i += 2;
    }

    return 0;
}
```

**Output:**

```text
2
4
6
8
10
...
48
50
```

### Q4. Print odd numbers from 1 to 50.

**Solution:**

```c
#include <stdio.h>

int main() {
    int i = 1;

    while (i <= 50) {
        printf("%d\n", i);
        i += 2;
    }

    return 0;
}
```

**Output:**

```text
1
3
5
7
9
...
47
49
```

### Q5. Find the sum of first N natural numbers.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, i = 1, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    while (i <= n) {
        sum += i;
        i++;
    }

    printf("Sum = %d", sum);

    return 0;
}
```

**Output:**

```text
Enter a number: 5
Sum = 15
```

### Q6. Print the multiplication table of a number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, i = 1;

    printf("Enter a number: ");
    scanf("%d", &n);

    while (i <= 10) {
        printf("%d x %d = %d\n", n, i, n * i);
        i++;
    }

    return 0;
}
```

**Output:**

```text
Enter a number: 5
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

### Q7. Find the factorial of a number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, i = 1;
    long long fact = 1;

    printf("Enter a number: ");
    scanf("%d", &n);

    while (i <= n) {
        fact *= i;
        i++;
    }

    printf("Factorial = %lld", fact);

    return 0;
}
```

**Output:**

```text
Enter a number: 5
Factorial = 120
```

### Q8. Count the number of digits in a number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, count = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    if (n == 0) {
        count = 1;
    } else {
        while (n != 0) {
            n /= 10;
            count++;
        }
    }

    printf("Total digits = %d", count);

    return 0;
}
```

**Output:**

```text
Enter a number: 12345
Total digits = 5
```

---

# Intermediate Level

### Q9. Find the sum of digits of a number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    while (n != 0) {
        sum += n % 10;
        n /= 10;
    }

    printf("Sum of digits = %d", sum);

    return 0;
}
```

**Output:**

```text
Enter a number: 1234
Sum of digits = 10
```

### Q10. Reverse a number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, reverse = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    while (n != 0) {
        reverse = reverse * 10 + n % 10;
        n /= 10;
    }

    printf("Reverse = %d", reverse);

    return 0;
}
```

**Output:**

```text
Enter a number: 1234
Reverse = 4321
```

### Q11. Check whether a number is palindrome.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, original, reverse = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    original = n;

    while (n > 0) {
        reverse = reverse * 10 + n % 10;
        n /= 10;
    }

    if (original >= 0 && original == reverse) {
        printf("Palindrome number");
    } else {
        printf("Not a palindrome number");
    }

    return 0;
}
```

**Output:**

```text
Enter a number: 121
Palindrome number
```

### Q12. Check whether a number is Armstrong.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, original, temp, digit;
    int sum = 0, count = 0, power;

    printf("Enter a number: ");
    scanf("%d", &n);

    if (n < 0) {
        printf("Not an Armstrong number");
        return 0;
    }

    original = n;
    temp = n;

    if (temp == 0) {
        count = 1;
    }

    while (temp > 0) {
        count++;
        temp /= 10;
    }

    temp = n;

    while (temp > 0) {
        digit = temp % 10;
        power = 1;

        int i = 1;

        while (i <= count) {
            power *= digit;
            i++;
        }

        sum += power;
        temp /= 10;
    }

    if (sum == original) {
        printf("Armstrong number");
    } else {
        printf("Not an Armstrong number");
    }

    return 0;
}
```

**Output:**

```text
Enter a number: 153
Armstrong number
```

### Q13. Check whether a number is prime.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, i = 2, prime = 1;

    printf("Enter a number: ");
    scanf("%d", &n);

    if (n <= 1) {
        prime = 0;
    }

    while (i <= n / i && prime == 1) {
        if (n % i == 0) {
            prime = 0;
        }
        i++;
    }

    if (prime) {
        printf("Prime number");
    } else {
        printf("Not a prime number");
    }

    return 0;
}
```

**Output:**

```text
Enter a number: 7
Prime number
```

### Q14. Find the largest digit in a number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, digit, max = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    if (n < 0) {
        n = -n;
    }

    while (n > 0) {
        digit = n % 10;

        if (digit > max) {
            max = digit;
        }

        n /= 10;
    }

    printf("Largest digit = %d", max);

    return 0;
}
```

**Output:**

```text
Enter a number: 5832
Largest digit = 8
```

### Q15. Find the smallest digit in a number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, digit, min = 9;

    printf("Enter a number: ");
    scanf("%d", &n);

    if (n < 0) {
        n = -n;
    }

    if (n == 0) {
        min = 0;
    }

    while (n > 0) {
        digit = n % 10;

        if (digit < min) {
            min = digit;
        }

        n /= 10;
    }

    printf("Smallest digit = %d", min);

    return 0;
}
```

**Output:**

```text
Enter a number: 5832
Smallest digit = 2
```

---

# Advanced Level

### Q16. Print the Fibonacci series up to N terms.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, i = 1;
    int a = 0, b = 1, c;

    printf("Enter number of terms: ");
    scanf("%d", &n);

    while (i <= n) {
        printf("%d ", a);

        c = a + b;
        a = b;
        b = c;

        i++;
    }

    return 0;
}
```

**Output:**

```text
Enter number of terms: 7
0 1 1 2 3 5 8
```

### Q17. Find the GCD (HCF) of two numbers.

**Solution:**

```c
#include <stdio.h>

int main() {
    int a, b, temp;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    while (b != 0) {
        temp = b;
        b = a % b;
        a = temp;
    }

    printf("GCD = %d", a);

    return 0;
}
```

**Output:**

```text
Enter two numbers: 12 18
GCD = 6
```

### Q18. Find the LCM of two numbers.

**Solution:**

```c
#include <stdio.h>

int main() {
    int a, b, x, y, temp;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    x = a;
    y = b;

    while (y != 0) {
        temp = y;
        y = x % y;
        x = temp;
    }

    if (a == 0 || b == 0) {
        printf("LCM = 0");
    } else {
        printf("LCM = %d", (a / x) * b);
    }

    return 0;
}
```

**Output:**

```text
Enter two numbers: 12 18
LCM = 36
```

### Q19. Check whether a number is a perfect number.

**Solution:**

```c
#include <stdio.h>

int main() {
    int n, i = 1, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    while (i <= n / 2) {
        if (n % i == 0) {
            sum += i;
        }
        i++;
    }

    if (n > 1 && sum == n) {
        printf("Perfect number");
    } else {
        printf("Not a perfect number");
    }

    return 0;
}
```

**Output:**

```text
Enter a number: 6
Perfect number
```

### Q20. Create a simple calculator using while loop.

**Solution:**

```c
#include <stdio.h>

int main() {
    int choice;
    float a, b;

    while (1) {
        printf("\n--- Calculator ---\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Exit\n");

        printf("Enter your choice: ");
        scanf("%d", &choice);

        if (choice == 5) {
            printf("Calculator closed");
            break;
        }

        if (choice < 1 || choice > 5) {
            printf("Invalid choice\n");
            continue;
        }

        printf("Enter two numbers: ");
        scanf("%f %f", &a, &b);

        switch (choice) {
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
                if (b != 0) {
                    printf("Result = %.2f\n", a / b);
                } else {
                    printf("Division by zero is not allowed\n");
                }
                break;
        }
    }

    return 0;
}
```

**Output:**

```text
--- Calculator ---
1. Addition
2. Subtraction
3. Multiplication
4. Division
5. Exit

Enter your choice: 1
Enter two numbers: 10 20
Result = 30.00
```

---

# Important While Loop Concepts

| Concept | Description |
|---|---|
| Initialization | Sets the starting value |
| Condition | Checks whether the loop should execute |
| Increment | Increases the variable |
| Decrement | Decreases the variable |
| break | Terminates the loop |
| continue | Skips the current iteration |

---


