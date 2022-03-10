---
layout:   post
title:    "[Leetcode #1] Two Sum"
subtitle: "[Leetcode #1] Two Sum"
category: studylog
tags:     algorithm
image:
  path:    /assets/img/algorithm/algorithm.jpg
---

[Leetcode #1 : Two Sum]:https://leetcode.com/problems/two-sum/  

<!--more-->
* this ordered seed list will be replaced by the toc
{:toc}  

[Leetcode #1 : Two Sum]
{:.note title="Link"}  

# Two Sum  
---  
__알고리즘을 푸는 스타일은 사람마다 다 다르므로 이것 또한 저의 주관적인 풀이 입니다.__  

## 문제 설명  
>정수인 배열 num 과 정수인 숫자 target 이 인자로 주어집니다.
>num 배열의 두 숫자 인덱스를 더하여 target 을 반환해야합니다.

__원문__
>Given an array of integers nums and an integer target,
>return indices of the two numbers such that they add up to target.  

## 예제  

* Example 1:

```js
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
```

* Example 2:
```
Input: nums = [3,2,4], target = 6
Output: [1,2]
```

* Example 3:
```
Input: nums = [3,3], target = 6
Output: [0,1]
```  

## 풀이  

```js
// file: "solution.js"
var twoSum = function(nums, target) {
    for (i=0; i<nums.length; i++) {
        for (j=i+1; j<nums.length; j++){
            if(nums[i]+nums[j]===target)
                return ([i, j])   
        }
    }
};
```  

## 설명  

* for 문 두개를 사용하여 하나는 기존배열에 +1을 하여 돈다.  
* 두개의 다른 for문이 배열의 인덱스를 돌며 값을 더한 후 target과 비교  
* target과 같은 값이 나오는 배열 인덱스를 반환한다.  