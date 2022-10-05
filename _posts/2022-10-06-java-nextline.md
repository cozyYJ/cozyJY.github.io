---
layout: post
title: (JAVA) Can't input using nextLine()
subtitle: Difference between next() and nextLine()
categories: JAVA
tags: [JAVA, user_input]
---

## Problem

```jAVA
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("What is your name?: ");
        String name = scanner.nextLine();
        System.out.print("How old are you?: ");
        int age = scanner.nextInt();
        System.out.print("What is your favorite food?: ");
        String food = scanner.nextLine();

        System.out.println("Hello "+name);
        System.out.println("You are "+age+" years old");
        System.out.println("You like "+food);
    }
}
```

When you code like this above, you can't type anything in food section.<br>
Screen would show only the two sentences in the last paragraph (name, age) well, not last one (food). It just prints "You like "<br>

### Cause

This is because _nextLine()_ method reads an entire line of text and stop when it reaches a new line character, which is \n.

However, nextInt() (and next()) doesn't read \n, so it is delivered when you press Enter key. And nextLine() at food part only reads the \n, gets automatically proceeded to the next step that prints the inputted infos.

### Solution

Therefore, you should write like one of these:

```java
System.out.print("How old are you?: ");
int age = scanner.nextInt();
scanner.nextLine(); //clean the new line character (Enter key)
System.out.print("What is your favorite food?: ");
String food = scanner.nextLine();
```

or

```java
System.out.print("How old are you?: ");
int age = scanner.nextInt();
System.out.print("What is your favorite food?: ");
String food = scanner.next(); //to not read \n
```

## Result

Then it will show what you expected.

![expected_result](https://user-images.githubusercontent.com/79247938/194130956-57385125-3767-4dcf-9df4-4986b571cc9c.png)
