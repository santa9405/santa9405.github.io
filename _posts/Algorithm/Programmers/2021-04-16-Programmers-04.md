---
title: "Programmers - JAVA"
excerpt: "나누어 떨어지는 숫자 배열"
categories: 
  - Algorithm 
tags: 
  - Algorithm  
  - Programmers
toc : true
---

## 나누어 떨어지는 숫자 배열
![image](https://user-images.githubusercontent.com/72387870/115020244-4662fa80-9ef5-11eb-9f43-162498397a72.png)

<br><br>

### 풀이

``` java
import java.util.*;

class Solution {
    public int[] solution(int[] arr, int divisor) {
        ArrayList<Integer> num = new ArrayList<Integer>();
        for(int i = 0; i < arr.length; i++){
            if(arr[i] % divisor == 0)   num.add(arr[i]);
        }
        if(num.isEmpty()){
            num.add(-1);
        }

        int[] answer = new int[num.size()];
        for(int i = 0; i < num.size(); i++){
            answer[i] = num.get(i);
        }
        
        Arrays.sort(answer);
        
        return answer;
    }
}
```
<br/><br/>

- arr의 배열 i번째와 divisor를 나누었을 때 나머지가 0이면 num에 추가!
- 포문이 끝나고 나누어 떨어지는 요소가 없다면 -1 추가!
- 리스트를 배열로 변환 후 정렬!

<br><br>