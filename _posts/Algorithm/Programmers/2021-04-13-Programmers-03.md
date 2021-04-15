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

- 가운데 글자를 반환해야 하기 때문에 s.length()/2를 하여 가운데 인덱스 번호를 구했다.
- 단어의 길이가 짝수인 경우는 가운데 두 글자를 반환해야 하므로 가운데 인덱스 번호에서 i-1과 i를 반환하도록 했다.
- 풀고 다른 사람들의 코드를 참고해보니 내 코드가 너무 길다..!
- 삼항 연산자를 이용하여 풀 수 있었는데 왜 생각을 못 했을까..!
- 그래서 삼항 연산자로 다시 풀어봤다.

<br><br>