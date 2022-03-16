---
layout:   post
title:    "[Leetcode #3] Longest Substring Without Repeating Characters"
subtitle: "[Leetcode #3] Longest Substring Without Repeating Characters"
category: studylog
tags:     algorithm
image:
  path:    /assets/img/algorithm/algorithm.jpg
---

[Leetcode #1 : Two Sum]:https://leetcode.com/problems/longest-substring-without-repeating-characters/  

<!--more-->
* this ordered seed list will be replaced by the toc
{:toc}  

[Leetcode #3 : Longest Substring Without Repeating Characters]
{:.note title="Link"}  

# Two Sum  
---  
__알고리즘을 푸는 스타일은 사람마다 다 다르므로 이것 또한 저의 주관적인 풀이 입니다.__  

## 문제 설명  
>문자열인 s 인자가 주어집니다.  
>중복되지 않는 문자열중에 제일 긴 문자열의 길이를 반환하세요.

__원문__
>Given a string s, find the length of the longest substring  
>without repeating characters.  

## 예제  

* Example 1:
```js
Input: s = "abcabcbb"
Output: 3
Explanation: The answer is "abc", with the length of 3.
```

* Example 2:
```js
Input: s = "bbbbb"
Output: 1
Explanation: The answer is "b", with the length of 1.
```

* Example 3:
```js
Input: s = "pwwkew"
Output: 3
Explanation: The answer is "wke", with the length of 3.
Notice that the answer must be a substring, "pwke" is a subsequence and not a substring.
```  

## 풀이  

```js
// file: "solution.js"
var lengthOfLongestSubstring = function(s) {
  let start = 0;
  let index = 0;
  let result = "";
  let temporary = "";
  for (i=0; i<s.length; i++){
    
    }
};
```  

## 설명  

* for 문 두개를 사용하여 두개중 하나는 i+1을 하여 반복문을 돈다.  
* 두개의 다른 for문이 배열의 인덱스를 돌며 값을 더한 후 target과 비교  
* target과 같은 값이 나오는 배열 인덱스를 반환한다.  

---  

## 다른 풀이 방법  

```js
// file: "Another-solution.js"
function twoSum(nums, target) {
let numObj = {};
  for (let i = 0; i < nums.length; i++) {
    let complement = target - nums[i];
    if (numObj[complement] !== undefined) {
      return [numObj[complement], i];
    }
    numObj[nums[i]] = i;
  }
}
```

> 인터넷에 다른 외국인분이 푸신 문제
> 객체를 사용하여 풀었다. 어렵다.

* 빈오브젝트를 만들어서 변수에 numObj 넣어준다.  
* 반복문을 배열의 길이만큼 돌아준다.  
* target 값에 num[i] 를 빼준 값을 complement 변수에 담아준다.  
* numObj 객체의 위에서 저장한 complement 의 값이 없다면 생략하여  
 첫번째 키값을 가진 numObj 객체에 i번째 밸류값을 넣어준다.  
* 이렇게 돌다가 해당 키값에 대한 밸류가 존재 한다면 해당 키값이 가지고 있는 밸류값과
인덱스를 리턴한다.  

>너무 어렵다 ㅠㅠ