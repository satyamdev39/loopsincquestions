# For Loop Practice Questions in C

## Introduction

Practice C programming questions using the `for` loop.

The `for` loop is used when the number of iterations is known in advance.

### Syntax

```c
for(initialization; condition; increment/decrement){
    // Statements
}
```

---

# Basic Level

### Q1. Print numbers from 1 to 20.

**Concept:** Basic for loop

**Solution:**

```c
#include <stdio.h>

int main() {
    int i;
    for(i=1; i<=20; i++) {
        printf("%d\n", i);
    }
    return 0;
}
```

**Output:**

```text
1
2
3
...
20
```

---

### Q2. Print numbers from 20 to 1.

```c
#include <stdio.h>

int main() {
    int i;
    for(i=20; i>=1; i--) {
        printf("%d\n", i);
    }
    return 0;
}
```

**Output**

```text
20
19
18
...
1
```

---

### Q3. Print the square of numbers from 1 to 10.

```c
#include <stdio.h>

int main() {
    int i;
    for(i=1; i<=10; i++) {
        printf("%d ", i*i);
    }
    return 0;
}
```

**Output**

```text
1 4 9 16 25 36 49 64 81 100
```

---

### Q4. Print the cube of numbers from 1 to 10.

```c
#include <stdio.h>

int main() {
    int i;
    for(i=1; i<=10; i++) {
        printf("%d ", i*i*i);
    }
    return 0;
}
```

**Output**

```text
1 8 27 64 125 216 343 512 729 1000
```

---

### Q5. Print all numbers divisible by 5 from 1 to 100.

```c
#include <stdio.h>

int main() {
    int i;
    for(i=5; i<=100; i+=5) {
        printf("%d ", i);
    }
    return 0;
}
```

**Output**

```text
5 10 15 ... 100
```

---

### Q6. Find the sum of even numbers from 1 to 100.

```c
#include <stdio.h>

int main() {
    int i,sum=0;
    for(i=2;i<=100;i+=2){
        sum+=i;
    }
    printf("Sum=%d",sum);
    return 0;
}
```

**Output**

```text
Sum=2550
```

---

### Q7. Find the sum of odd numbers from 1 to 100.

```c
#include <stdio.h>

int main() {
    int i,sum=0;
    for(i=1;i<=100;i+=2){
        sum+=i;
    }
    printf("Sum=%d",sum);
    return 0;
}
```

**Output**

```text
Sum=2500
```

---

# Intermediate Level

### Q8. Print ASCII values of characters A to Z.

```c
#include <stdio.h>

int main() {
    char ch;
    for(ch='A'; ch<='Z'; ch++){
        printf("%c = %d\n",ch,ch);
    }
    return 0;
}
```

**Output**

```text
A = 65
B = 66
...
Z = 90
```

---

### Q9. Print lowercase letters a to z.

```c
#include <stdio.h>

int main() {
    char ch;
    for(ch='a'; ch<='z'; ch++){
        printf("%c ",ch);
    }
    return 0;
}
```

**Output**

```text
a b c d ... z
```

---

### Q10. Find the product of first N natural numbers.

```c
#include <stdio.h>

int main() {
    int n,i;
    long long product=1;

    scanf("%d",&n);

    for(i=1;i<=n;i++){
        product*=i;
    }

    printf("%lld",product);

    return 0;
}
```

**Output**

```text
Input:5
120
```

---

### Q11. Print a right triangle using `*`.

```c
#include <stdio.h>

int main() {
    int i,j;

    for(i=1;i<=5;i++){
        for(j=1;j<=i;j++){
            printf("*");
        }
        printf("\n");
    }

    return 0;
}
```

**Output**

```text
*
**
***
****
*****
```

---

### Q12. Print an inverted star triangle.

```c
#include <stdio.h>

int main() {
    int i,j;

    for(i=5;i>=1;i--){
        for(j=1;j<=i;j++){
            printf("*");
        }
        printf("\n");
    }

    return 0;
}
```

**Output**

```text
*****
****
***
**
*
```

---

### Q13. Print a number triangle.

```c
#include <stdio.h>

int main() {
    int i,j;

    for(i=1;i<=5;i++){
        for(j=1;j<=i;j++){
            printf("%d ",j);
        }
        printf("\n");
    }

    return 0;
}
```

**Output**

```text
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

---

### Q14. Print Floyd's Triangle.

```c
#include <stdio.h>

int main() {
    int i,j,num=1;

    for(i=1;i<=5;i++){
        for(j=1;j<=i;j++){
            printf("%d ",num++);
        }
        printf("\n");
    }

    return 0;
}
```

**Output**

```text
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

---

# Advanced Level

### Q15. Print multiplication tables from 1 to 10.

```c
#include <stdio.h>

int main() {
    int i,j;

    for(i=1;i<=10;i++){
        printf("\nTable of %d\n",i);
        for(j=1;j<=10;j++){
            printf("%d x %d = %d\n",i,j,i*j);
        }
    }

    return 0;
}
```

---

### Q16. Print all prime numbers from 1 to 100.

```c
#include <stdio.h>

int main() {
    int i,j,prime;

    for(i=2;i<=100;i++){
        prime=1;

        for(j=2;j*j<=i;j++){
            if(i%j==0){
                prime=0;
                break;
            }
        }

        if(prime)
            printf("%d ",i);
    }

    return 0;
}
```

**Output**

```text
2 3 5 7 11 ... 97
```

---

### Q17. Print the factorial of numbers from 1 to 10.

```c
#include <stdio.h>

int main() {
    int i,j;
    long long fact;

    for(i=1;i<=10;i++){
        fact=1;
        for(j=1;j<=i;j++){
            fact*=j;
        }
        printf("%d! = %lld\n",i,fact);
    }

    return 0;
}
```

---

### Q18. Print a hollow square pattern.

```c
#include <stdio.h>

int main() {
    int i,j,n=5;

    for(i=1;i<=n;i++){
        for(j=1;j<=n;j++){
            if(i==1||i==n||j==1||j==n)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }

    return 0;
}
```

**Output**

```text
* * * * *
*       *
*       *
*       *
* * * * *
```

---

### Q19. Print Pascal's Triangle (5 rows).

```c
#include <stdio.h>

int main() {
    int i,j,num;

    for(i=0;i<5;i++){
        num=1;
        for(j=0;j<=i;j++){
            printf("%d ",num);
            num=num*(i-j)/(j+1);
        }
        printf("\n");
    }

    return 0;
}
```

**Output**

```text
1
1 1
1 2 1
1 3 3 1
1 4 6 4 1
```

---

### Q20. Print a pyramid star pattern.

```c
#include <stdio.h>

int main() {
    int i,j,n=5;

    for(i=1;i<=n;i++){

        for(j=1;j<=n-i;j++)
            printf(" ");

        for(j=1;j<=2*i-1;j++)
            printf("*");

        printf("\n");
    }

    return 0;
}
```

**Output**

```text
    *
   ***
  *****
 *******
*********
```

---

# Important For Loop Concepts

| Concept | Description |
|----------|-------------|
| Initialization | Starting value |
| Condition | Controls loop execution |
| Increment | Increases value |
| Decrement | Decreases value |
| Nested Loop | Loop inside another loop |
| `break` | Exits the loop |
| `continue` | Skips one iteration |

---

