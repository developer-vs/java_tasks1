# solved-tasks

#### Remove String Spaces

##### Java
```java
class Kata {
  static String noSpace(final String x) {
    String output = "";
    for(int i = 0; i < x.length(); i++) {
      String character = String.valueOf(x.charAt(i));
      if(!character.equals(" ")) {
        output += character;
      }
    }
    return output;
  }
}
```

##### JavaScript
```javascript
function noSpace(x){  
  let newStr = '';
  for(let i=0; i<x.length; i++) {
    if(x[i] !== ' ') {
      newStr = newStr + x[i];
    }
  }
  return newStr;
}
```
#### Get the Middle Character

##### Java
```java
class Kata {
  public static String getMiddle(String word) {
    String str = "";
    if(word.length() > 0) {
      if(word.length() % 2 == 0) {
        str = String.valueOf(word.charAt(word.length() / 2 - 1)) + String.valueOf(word.charAt(word.length() / 2));
       } else {
         str = String.valueOf(word.charAt((word.length() -1 ) / 2) );
       }
    }
    return str;
  }
}
```
##### JavaScript
```javascript
function getMiddle(s)
{
  if(s.length % 2 === 0) {
    return (s[s.length/2-1]+s[s.length/2]);
  }
  
  if(s.length % 2 > 0) {
    return (s[(s.length-1)/2]);
  }  
}
```
#### Multiples of 3 or 5

##### Java
```java
public class Solution {

  public int solution(int number) {
    int sum = 0;    
    for(int i = 0; i < number; i++) {         
      if(i % 3 == 0 && i % 5 == 0) {
        sum += i;   
      } else if(i % 3 == 0) {
        sum += + i;
      } else if(i % 5 == 0) {
        sum += + i;
      } else {
        sum += 0;
      }        
    }           
    return sum;
  }
}
```