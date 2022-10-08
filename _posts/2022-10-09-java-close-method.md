---
layout: post
title: (JAVA) Why scanner.close()?
categories: JAVA
tags: [JAVA, user_input]
published: true
---

## Problem

What is the precise reason for adding sc.close(); when I use Scanner class?

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Score: ");
        int score = sc.nextInt();
        sc.close();
    }
}
```

## Reason

![reason](https://user-images.githubusercontent.com/79247938/194723758-b0e4823d-664a-4555-af2e-2b0cf95b9fb3.png)

## Source

[java_sc.close();](https://kin.naver.com/qna/detail.nhn?d1id=1&dirId=1040201&docId=384617557&qb=c2M/Pz8/ID8/Pz8=&enc=utf8&section=kin.qna&rank=5&search_sort=0&spq=0)
