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

#### Well of Ideas - Easy Version

##### Java
```java
public class Kata {

  public static String well(String[] x) {
    int counter = 0;
    for(int i=0; i < x.length; i++) {
      if(x[i].equals("good")) {
        counter++;
      }
    }
    if(counter > 0 && counter <= 2 ) {
      return "Publish!";
    } else if(counter > 2) {
      return "I smell a series!";
    } else {
      return "Fail!";
    }
  }
}
```
#### Reversed Strings

##### Java
```java
public class Kata {

  public static String solution(String str) {
    String result = "";
    for(int i = str.length()-1; i >= 0; i--) {
      result +=str.charAt(i);
    }
    return result;
  }
}
```

#### Numbers to Letters

##### JavaScript
```javascript
function switcher(x){
  let word = '';
  let str = (" ?!abcdefghijklmnopqrstuvwxyz-").split("").reverse();
  for(let i=0; i < x.length; i++) {
    word += str[x[i]];
  }
  return word;
}
```

#### Debug the functions EASY

##### JavaScript
```javascript
function multi(arr) {
  let num = 1;
  for(let i=0; i<arr.length; i++) {
    num *= arr[i];
  }
  return num;
}
function add(arr) {
  let num = 0;
  for(let i=0; i<arr.length; i++) {
    num += arr[i];
  }
  return num;
}
function reverse(str) {
  return str.split('').reverse().join('');
}
```

#### Count the Monkeys!

##### JavaScript
```javascript
function monkeyCount(n) {
let arr = [];
  for(let i = 0; i < n; i++) {
    arr[i] = i+1;
  }
  return arr;
}
```

#### Playing with cubes I

##### Java
```java
public class Cube{
  private int side;
  
  public int getSide() {
    return side;
  }

  public void setSide(int side) {
    this.side = side;
  }  
}
```