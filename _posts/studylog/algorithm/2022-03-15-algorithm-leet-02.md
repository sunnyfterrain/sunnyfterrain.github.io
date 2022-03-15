---
layout:   post
title:    "[Leetcode #7] Reverse Integer"
subtitle: "[Leetcode #7] Reverse Integer"
category: studylog
tags:     algorithm
image:
  path:    /assets/img/algorithm/algorithm.jpg
---

[Leetcode #1 : Two Sum]:https://leetcode.com/problems/reverse-integer/  

<!--more-->
* this ordered seed list will be replaced by the toc
{:toc}  

[Leetcode #1 : Two Sum]
{:.note title="Link"}  

# Two Sum  
---  
__알고리즘을 푸는 스타일은 사람마다 다 다르므로 이것 또한 저의 주관적인 풀이 입니다.__  

## 문제 설명  
>정수인 x가 주어집니다 x를 거꾸로 하여 반환하세요.  

__원문__
>Given a signed 32-bit integer x, return x with its digits reversed.  
>If reversing x causes the value to go outside the signed 32-bit integer range  
> [-231, 231 - 1], then return

## 예제  

* Example 1:
```js
Input: x = 123
Output: 321
```

* Example 2:
```js
Input: x = -123
Output: -321
```

* Example 3:
```js
Input: x = 120
Output: 21
```  

## 풀이  

```js
// file: "solution.js"
var reverse = function(x) {
  const answer = parseInt(x.toString().split('').reverse().join('')) * Math.sign(x)
    return answer  
};
```  

## 설명  

* 인자로 받은 숫자를 쪼개기 위해서 toString으로 문자형으로 변환해준다.  
* split으로 하나하나 쪼개서 배열로 만들어준다.  
* reverse로 순서를 거꾸로 만든다.  
* join으로 쪼개것을 다 합쳐준다.  
* 다시 숫자형으로 되돌리기 위해 parseInt로 감싸준다.  
* 그리고 다시 `Math.sign` 함수로 x 를 담아 answer를 반환

> MDN 인용
> Math.sign() 함수는 주어진 수의 부호를 나타내는 +/-1을 반환합니다.  
> 단, Math.sign()에 제공한 수가 0일 경우 부호에 따라 +/-0을 반환합니다.  
> * 즉 주어진 수가 양수면 1을 음수면 -1을 반환한다.  
---  

