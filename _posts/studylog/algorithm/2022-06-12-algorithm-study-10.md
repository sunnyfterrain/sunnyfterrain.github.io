---
layout:   post
title:    "[Inflearn #10] 멘토링"
subtitle: "[Inflearn #10] 멘토링"
category: studylog
tags:     algorithm
image:
  path:    /assets/img/algorithm/algorithm.jpg
---

<!--more-->

[인프런 : JS 알고리즘 문제풀이]:https://www.inflearn.com/course/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98-%EB%AC%B8%EC%A0%9C%ED%92%80%EC%9D%B4

* this ordered seed list will be replaced by the toc
{:toc}  

[인프런 : JS 알고리즘 문제풀이]  
{:.note title="Link"}  

__인프런 코테 대비 알고리즘 문제풀이를 정리해 놓은 것입니다.__  

## 문제 설명  

>멘토링  
>
>현수네 반 선생님은 반 학생들의 수학점수를 향상시키기 위해 멘토링 시스템을 만들려고 합니다.  
>멘토링은 멘토(도와주는 학생)와 멘티(도움을 받는 학생)가 한 짝이 되어 멘토가 멘티의  
>수학공부를 도와주는 것입니다.  
>선생님은 M번의 수학테스트 등수를 가지고 멘토와 멘티를 정합니다.  
>만약 A학생이 멘토이고, B학생이 멘티가 되는 짝이 되었다면, A학생은 M번의 수학테스트에서  
>모두 B학생보다 등수가 앞서야 합니다.  
>M번의 수학성적이 주어지면 멘토와 멘티가 되는 짝을 만들 수 있는 경우가 총 몇 가지 인지  
>출력하는 프로그램을 작성하세요.  


<br>  

## 문제 예제  

▣ 입력설명  
첫 번째 줄에 반 학생 수 N(1<=N<=20)과 M(1<=M<=10)이 주어진다.  
두 번째 줄부터 M개의 줄에 걸쳐 수학테스트 결과가 학생번호로 주어진다.  
학생번호가 제일 앞에서부터 1등, 2등, ...N등 순으로 표현된다.  
만약 한 줄에 N=4이고, 테스트 결과가 3 4 1 2로 입력되었다면 3번 학생이 1등,  
4번 학생이 2등, 1번 학생이 3등, 2번 학생이 4등을 의미합니다.  

▣ 출력설명  
첫 번째 줄에 짝을 만들 수 있는 총 경우를 출력합니다.  

▣ 입력예제 1  
3 4 1 2  
4 3 2 1  
3 1 4 2  


▣ 출력예제 1  
3  

(3, 1), (3, 2), (4, 2)와 같이 3가지 경우의 (멘토, 멘티) 짝을 만들 수 있다.  


## 풀이  

```java
// file: "solution.js"
function solution(test) {
  let answer = 0;
  let m = test.length;
  let n = test[0].length;  // #1
  let count;
  for (i = 1; i <= n; i++) {
    for (j = 1; j <= n; j++) {  // #2
      count = 0;  // #9
      for (k = 0; k < m; k++) { // #3
        let mto = 0;  // #4
        let mti = 0;
        for (s = 0; s < n; s++) {  // #5
          if (test[k][s] === i) mto = s;  // #6
          if (test[k][s] === j) mti = s;
        }
        if (mto > mti) count++;  // #7
      }
      if (count === m) answer++;  // #8
    }
  }
  return answer;
}
```

## 설명  

1. 반복문의 조건이 될 변수를 선언해 줍니다. 학생이 총 4명이므로 각각 비교할 학생은 n으로,  
테스트 결과는 3개이므로 m으로 설정해 줍니다. 짝이 맞는지 체크할 count도 선언합니다.  
2. 학생 4명을 다 돌릴 반복문을 만듭니다. 1~4번 학생이므로 0이 아닌 1부터 시작합니다.  
3. 테스트 결과를 다 돌릴 반복문을 설정해 줍니다.  
4. 이제 테스트 결과를 돌면서 멘토와 멘티의 수를 저장할 변수를 설정해 줍니다.  
5. 각각의 테스트 결과 점수를 돌릴 반복문을 설정해 줍니다.  
6. 각각의 테스트 결과와 각 학생(i와 j)이 동일하다면 멘토와 멘티에 그때의 인덱스를 넣어줍니다.  
7. 멘토의 더 등수가 높아야 하니 3개의 테스트 결과에서 멘토가 높았던 횟수를 카운트해 줍니다.  
8. 모든 테스트의 결과가 멘티보다 멘토가 더 높은 등수야 하므로 카운트의 수는 테스트 결과의 수(m)와  
같아야 하므로 같다면 answer를 증가시켜 줍니다.  
9. 그리고 다시 다음 사람을 돌아야 하므로 count는 0으로 초기화시켜 줍니다.  


