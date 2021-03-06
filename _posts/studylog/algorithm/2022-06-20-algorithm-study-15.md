---
layout:   post
title:    "[백준 #10799] 쇠막대기"
subtitle: "[백준 #10799] 쇠막대기"
category: studylog
tags:     algorithm
image:
  path:    /assets/img/algorithm/algorithm.jpg
---

<!--more-->

[백준 #10799 : 쇠막대기 ]:https://www.acmicpc.net/problem/10799

* this ordered seed list will be replaced by the toc
{:toc}  

[백준 #10799 : 쇠막대기]  
{:.note title="Link"}  

__알고리즘을 푸는 스타일은 사람마다 다 다르므로 이것 또한 저의 주관적인 풀이 입니다.__  

## 문제 설명  

>쇠막대기  
>
>여러 개의 쇠막대기를 레이저로 절단하려고 한다.  
>효율적인 작업을 위해서 쇠막대기를 아래에 서 위로 겹쳐 놓고,  
>레이저를 위에서 수직으로 발사하여 쇠막대기들을 자른다.  
>쇠막대기와 레 이저의 배치는 다음 조건을 만족한다.  
>• 쇠막대기는 자신보다 긴 쇠막대기 위에만 놓일 수 있다.  
>  - 쇠막대기를 다른 쇠막대기 위에 놓는 경우 완전히 포함되도록 놓되,  
>    끝점은 겹치지 않도록 놓는다.
>• 각 쇠막대기를 자르는 레이저는 적어도 하나 존재한다.  
>• 레이저는 어떤 쇠막대기의 양 끝점과도 겹치지 않는다.  

>아래 그림은 위 조건을 만족하는 예를 보여준다.  
>수평으로 그려진 굵은 실선은 쇠막대기이고, 점은 레이저의 위치, 수직으로 그려진  
>점선 화살표는 레이저의 발사 방향이다.  

![](https://onlinejudgeimages.s3-ap-northeast-1.amazonaws.com/problem/10799/1.png)

>이러한 레이저와 쇠막대기의 배치는 다음과 같이 괄호를 이용하여 왼쪽부터 순서대로  
>표현할 수 있다.

>1. 레이저는 여는 괄호와 닫는 괄호의 인접한 쌍 ‘( ) ’ 으로 표현된다.  
>또한, 모든 ‘( ) ’는 반 드시 레이저를 표현한다.  
>2. 쇠막대기의 왼쪽 끝은 여는 괄호 ‘ ( ’ 로, 오른쪽 끝은 닫힌 괄호 ‘) ’ 로 표현된다.  

>위 예의 괄호 표현은 그림 위에 주어져 있다.  
>쇠막대기는 레이저에 의해 몇 개의 조각으로 잘려지는데, 위 예에서 가장 위에 있는  
>두 개의 쇠막대기는 각각 3개와 2개의 조각으로 잘려지고, 이와 같은 방식으로 주어진  
>쇠막대기들은 총 17개의 조각으로 잘려진다.  
>쇠막대기와 레이저의 배치를 나타내는 괄호 표현이 주어졌을 때, 잘려진 쇠막대기  
>조각의 총 개수를 구하는 프로그램을 작성하시오.

<br>  

## 문제 예제  

▣ 입력설명  
한 줄에 쇠막대기와 레이저의 배치를 나타내는 괄호 표현이 공백없이 주어진다.  
괄호 문자의 개수는 최대 100,000이다.  

▣ 출력설명  
잘려진 조각의 총 개수를 나타내는 정수를 한 줄에 출력한다.  

▣ 입력예제 1  
()(((()())(())()))(())  

▣ 출력예제 1  
17  

▣ 입력예제 2  
(((()(()()))(())()))(()())  

▣ 출력예제 2  
24  



## 풀이  

```java
// file: "solution.js"
function solution(s) {
  let answer = 0;
  let stack = [];  // #1
  for (i = 0; i < s.length; i++) {  // #2
    if (s[i] === '(') stack.push(s[i]);  // #3
    else {
      stack.pop();  // #4
      if (s[i - 1] === '(') answer += stack.length;  // #5
      else answer += 1;  // #6
    }
  }
  return answer;
}
```

## 설명  

1. 스택을 넣어줄 빈 배열을 생성합니다.  
2. 매개변수로 들어온 문자열 s를 반복문 돌립니다.  
3. 문자열에서 '(' 를 만나면 stack에 push 해줍니다. '(' 하나가 철판 하나인 셈입니다.  
4. '(' 이 아니라면? (')' 밖에 없겠죠) 레이져이기때문에 stack 에서 `pop` 을 해줍니다.  
5. 그리고 만약에 레이저 이전의 문자가 '(' 라면 철판들이기 때문에 그동안 잘린게  
스택에 쌓여있을 것입니다. 그것을 answer에 더해줍시다.  
6. '('가 아니라면 이전이 레이저인거고 철판의 끝부분 이기때문에 하나가 더 잘렸으니  
answer에 +1을 해줍니다.  