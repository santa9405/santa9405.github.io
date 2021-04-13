---
title: "Programmers - JAVA"
excerpt: "가운데 글자 가져오기"
categories: 
  - Algorithm 
tags: 
  - Algorithm  
  - Programmers
toc : true
---

## 가운데 글자 가져오기

![image](https://user-images.githubusercontent.com/72387870/114520357-545a1680-9c7c-11eb-9c2e-e45cb860ba2f.png)

<br><br>

### 풀이

``` java
class Solution {
    public String solution(String s) {
        String answer = "";
        for(int i = 0; i < s.length(); i++){
            if(i == (s.length()/2)){
                if(s.length()%2 == 1){
                    answer = s.charAt(i) + "";
                }else{
                    answer = s.charAt(i-1) + "" + s.charAt(i);
                }
            }
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

### 풀이

``` java
class Solution {
    public String solution(String s) {
        int length = s.length();
        int mid = length/2;
        return length%2 == 1 ? s.substring(mid, mid+1) : s.substring(mid-1, mid+1);
    }
}
```
<br/><br/>

- s의 길이와 길이/2의 값을 변수에 넣고 사용했다.
- s가 홀수이면 가운데 글자만 리턴, 짝수인 경우 가운데 두 글자를 리턴했다.
- 처음에 작성했던 코드보다 깔끔해져서 기분이 좋다!

<br/><br/>