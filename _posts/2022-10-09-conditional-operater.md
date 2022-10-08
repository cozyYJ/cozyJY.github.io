---
layout: post
title: (BOJ) Applying Conditional Operator
subtitle: MULTIPLE conditional operator!
categories: BOJ JAVA C
tags: [BOJ, JAVA, C]
published: true
---

## Problem

**BOJ No.9498**

![example](https://user-images.githubusercontent.com/79247938/194723997-be0a058e-8789-41b0-bdcf-47ead48904a5.png)

### Solution

Surely we can solve this by using if statements.<br>
But here's a brand new perspective (for me) on this; using a multiple conditional operator.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Score: ");
        int score = sc.nextInt();
        sc.close();

        System.out.print((score>=90)? "A": (score>=80)? "B": (score>=70)? "C": (score>=60)? "D": "F");
    }
}
```

```c
#include <stdio.h>

int main() {
    int score;
    scanf_s("%d", &score);
    printf("%c", (score>=90)? 'A': (score>=80)? 'B': (score>=70)? 'C': (score>=60)? 'D': 'F');
}
```

## Result

Normal and desirable result comes up.

## Source

[BOJ-9498](https://st-lab.tistory.com/22)
