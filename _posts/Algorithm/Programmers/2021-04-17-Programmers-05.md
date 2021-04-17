---
title: "Programmers - JAVA"
excerpt: "두 정수 사이의 합"
categories: 
  - Algorithm 
tags: 
  - Algorithm  
  - Programmers
toc : true
---

## 두 정수 사이의 합
![image](https://user-images.githubusercontent.com/72387870/115113608-251e0f00-9fc6-11eb-834e-74d28d9d4650.png)

<br><br>

### 풀이

``` java
class Solution {
    public long solution(int a, int b) {
        long answer = 0;
        if(a > b){
            for(int i = b; i <= a; i++) answer += i;
        }else{
            for(int i = a; i <= b; i++) answer += i;
        }
        return answer;
    }
}
```
<br/><br/>

- a가 큰 경우 b부터 a까지 answer 누적하며 더해주기!
- b가 큰 경우 a부터 b까지 answer 누적하며 더해주기!
- 제출 후 다른 사람의 풀이를 참고해보니 Math.max/min 클래스를 이용한 풀이가 있어서 나도 이용해봤다!

<br><br>

``` java
class Solution {
    public long solution(int a, int b) {
        long answer = 0;
        
        int max = Math.max(a, b);
        int min = Math.min(a, b);
        
        for(int i = min; i <= max; i++){
            answer += i;
        }
        return answer;
    }
}
```
<br/><br/>
