---
title: "Programmers - JAVA"
excerpt: "같은 숫자는 싫어"
categories: 
  - Algorithm 
tags: 
  - Algorithm  
  - Programmers
toc : true
---

## 같은 숫자는 싫어
![image](https://user-images.githubusercontent.com/72387870/114882269-c11d0e80-9e3e-11eb-85e2-c3d2b6036f10.png)

<br><br>

### 풀이

``` java
public class Solution {
    public int[] solution(int []arr) {
        int current = 10;
        ArrayList<Integer> list = new ArrayList<Integer>();
        for(int i = 0 ; i < arr.length; i++){
            if(arr[i] != current){
                list.add(arr[i]);
                current = arr[i];
            }
        }    
        int[] answer = new int[list.size()];    
        for(int i = 0; i < list.size(); i++){
            answer[i] = list.get(i);
        }
        return answer;
    }
}
```
<br/><br/>

- current의 값을 10으로 주어 for문 안의 if문이 처음에는 무조건 실행된다.
- if문이 실행되면 arr의 i번째 값이 list에 추가된다.
- 그 후 current의 값을 arr의 i번째 값으로 변경하여 if문의 조건이 달라지도록 했다.
- answer배열 길이를 리스트의 사이즈만큼 생성한 후 list에 있는 데이터를 answer배열에 옮겨주었다.

<br><br>