---
title: "Programmers - JAVA"
excerpt: "2016년"
categories: 
  - Algorithm 
tags: 
  - Algorithm  
  - Programmers
toc : true
---

## 2016년

![image](https://user-images.githubusercontent.com/72387870/114331388-d8c66f80-9b7e-11eb-88d1-a699e9665fb2.png)

<br><br>

### 풀이

``` java
class Solution {
    public String solution(int a, int b) {
        String answer = "";        
        String[] day = { "FRI", "SAT", "SUN", "MON", "TUE", "WED", "THU" };
        int[] date = { 31, 29, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31 };
        int sumDate = 0;
        
        // 해당 월 전까지의 전체 일 수 더하기
        for(int i = 0; i < a-1; i++)
            sumDate += date[i];
        
        // 해당 월의 일 수 더하기
        sumDate += b - 1;
        
        // 일주일로 나눈 나머지 계산
        answer = day[sumDate % 7];
        
        return answer;
    }
}
```
<br/><br/>

- 특정 날짜 계산하는 방법을 찾아보니 Date 클래스의 SimpleDateFormat과, Calendar 클래스의 getInstance() 메소드를 이용해 계산하는 방법이 있었다.
- 하지만 2016년이 윤년이라는 조건과, 2016년 1월 1일이 금요일이라는 조건이 있어서 이를 이용해 요일을 계산했다.
- 2016년 1월 1일이 금요일이기 때문에 배열 day는 FRI부터 넣었고, 윤년이기 때문에 2월은 29일로 계산될 수 있도록 했다.
- 해당 월의 일 수 더해줄 때 -1을 안 했더니 WED가 나왔는데, 7로 나눈 나머지의 값을 day의 index 값을 이용하므로 -1을 해주니까 TUE가 나왔다.

<br/><br/>