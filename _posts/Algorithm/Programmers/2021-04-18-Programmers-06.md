---
title: "Programmers - JAVA"
excerpt: "서울에서 김서방 찾기"
categories: 
  - Algorithm 
tags: 
  - Algorithm  
  - Programmers
toc : true
---

## 서울에서 김서방 찾기
![image](https://user-images.githubusercontent.com/72387870/115147468-1737bf00-a096-11eb-8051-ca08659701c3.png)

<br><br>

### 풀이

``` java
class Solution {
    public String solution(String[] seoul) {
        String answer = "";
        for(int i = 0; i < seoul.length; i++){
            if(seoul[i].equals("Kim"))
                answer = "김서방은 " + i + "에 있다";
        }
        return answer;
    }
}
```
<br/><br/>

- 문자열을 비교할 수 있는 equals를 사용하여 "Kim"의 위치를 찾았다!

<br><br>