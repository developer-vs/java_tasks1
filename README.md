# solved-tasks

#### Remove String Spaces

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
