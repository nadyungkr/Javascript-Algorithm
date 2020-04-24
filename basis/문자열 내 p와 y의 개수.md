## 문자열 내 p와 y의 개수

### 문제 설명
- 대문자와 소문자가 섞여있는 문자열 s가 주어집니다. s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요.
- 'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다. 단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.
- 예를들어 s가 "pPoooyY"면 true를 return 하고 "Pyy"라면 false를 return합니다

### 제한 사항
- 문자열 s의 길이: 50이하의 자연수
- 문자열 s는 알파벳으로만 이루어져 있습니다.

### 입출력 예
s|anwer
|------|--------|
"pPoooyY"|true
"Pyy"|false

### 입출력 예 설명
- 'p'의 개수 2개, 'y'의 개수 2개로 같으므로 true를 return
- 'p'의 개수 1개, 'y'의 개수 2개로 다르므로 false를 return

### solution.js
```javascript
function solution(s){
    var answer = true;

    // [실행] 버튼을 누르면 출력 값을 볼 수 있습니다.
    console.log('Hello Javascript')

    return answer;
}
```

- 문자열 S에 p, P, y, Y가 있는지 검사해야 하기 때문에 `for in`문을 활용 한다.
- `if 문`과 `else if`문을 사용해서 문자열 s에 p, P, y, Y가 있다면 개수를 저장할 수 있도록 변수를 선언한다.
- 문자열에서 대문자 또는 소문자 상관없이 센다고 했으므로, 형변환을 하여 저장할 수 있도록 `toUpperCase` 또는 `toLowerCase`를 사용한다.

```javascript
function solution(s){ 
    var a = 0;
    var b = 0;
    for( var i in s ) {
        if (s[i].toUpperCase() == "P" ){
            a++;
        } else if ( s[i].toUpperCase() == "Y" ){
            b++;
        }
    }
    if ( a == b ) { 
        return true;
    } else {
        return false;
    }
}
```
