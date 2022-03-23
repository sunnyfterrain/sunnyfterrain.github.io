---
layout:   post
title:    "[Leetcode #20] Valid Parentheses"
subtitle: "[Leetcode #20] Valid Parentheses"
category: studylog
tags:     algorithm
image:
  path:    /assets/img/algorithm/algorithm.jpg
---

[Leetcode #20 : Valid Parentheses]:https://leetcode.com/problems/valid-parentheses/

<!--more-->
* this ordered seed list will be replaced by the toc
{:toc}  

[Leetcode #20 : Valid Parentheses]
{:.note title="Link"}  

# Majority Element  
---  
__알고리즘을 푸는 스타일은 사람마다 다 다르므로 이것 또한 저의 주관적인 풀이 입니다.__  

## 문제 설명  
>크기가 n인 num로 이루어진 배열이 주어진다. 과반수를 리턴하라  
>과반수는 [n / 2] 이상으로 나타나는 요소이다.  
>과반수 요소는 항상 배열에 존재한다.  

__원문__
>Given a string s containing just the characters '(', ')', '{', '}', '[' and ']',  
>determine if the input >string is valid.  
>You may assume that the majority element always exists in the array.  
>An input string is valid if:
>Open brackets must be closed by the same type of brackets.
>Open brackets must be closed in the correct order.
<br>  
## 예제  

* Example 1:
```js
Input: s = "()"
Output: true
```  

* Example 2:
```js
Input: s = "()[]{}"
Output: true
```  

* Example 3:
```js
Input: s = "(]"
Output: false
```  

## 풀이  

```js
// file: "solution.js"
var isValid = function(s) {
  while(s.includes('()') || s.includes('{}')|| s.includes('[]')){
    s = s.replace('()','').replace('{}','').replace('[]','')
  } return !s.length
};
```  

## 설명  


