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
function getMiddle(s) {
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
          returneturn "Fail!";
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

#### Lombok Encapsulation

##### Java
```java
public class EncapsulationDemo{
    private int number;
    private String stringValue;
    private Object anObject;
  
    EncapsulationDemo() {};
  
    EncapsulationDemo(int number, String stringValue, Object anObject) {
        this.number = number;
        this.stringValue = stringValue;
        this.anObject = anObject;
    };

    public void setNumber(int number) {
        this.number = number;
    }
  
    public int getNumber() {
        return number;
    }
  
    public void setStringValue(String stringValue) {
        this.stringValue = stringValue;
    }
  
    public String getStringValue() {
        return stringValue;
    }

    public void setAnObject(Object anObject) {
        this.anObject = anObject;
    }
  
    public Object getAnObject() {
        return anObject;
    }
}
```

#### Building blocks

##### Java
```java
public class Block{
      private int width;
      private int length;
      private int height;
      private int volume;
      private int surfaceArea;

    Block(int[] arr) {
        this.width = arr[0];
        this.length = arr[1];
        this.height = arr[2];
        this.volume = height * length * width;
        this.surfaceArea = 2 * (length * width + length * height + width * height);
    }

    public int getWidth() {
        return width;
    }

    public int getLength() {
        return length;
    }

    public int getHeight() {
        return height;
    }

    public int getVolume() {
        return volume;
    }

    public int getSurfaceArea() {
        return surfaceArea;
    }
}
```

#### Two fighters, one winner.

##### Java
```java
public class Kata {

    public static String declareWinner(Fighter fighter1, Fighter fighter2, String firstAttacker) {

        String fighter = null;
        
        if(firstAttacker.equals(fighter1.name)) {
            while(fighter2.health > 0 || fighter1.health > 0) {
                fighter2.health -= fighter1.damagePerAttack; 
                if(fighter2.health <= 0) {
                    fighter = fighter1.name;
                    break;
                }
            
                fighter1.health -= fighter2.damagePerAttack;
                if(fighter1.health <= 0) {
                    fighter = fighter2.name;
                    break;
                }
            }
        }
        
        if(firstAttacker.equals(fighter2.name)) {
            while(fighter1.health > 0 || fighter2.health > 0) {
                fighter1.health -= fighter2.damagePerAttack;
                if(fighter1.health <= 0) {
                    fighter = fighter2.name;
                    break;
                }

                fighter2.health -= fighter1.damagePerAttack;
                if(fighter2.health <= 0) {
                    fighter = fighter1.name;
                    break;
                }
            }
        }
        return fighter;
    }
}
```

#### How to swap array elements in reverse order in Java

##### Java
```java
public class ArraysTesting {
    
    public static void main(String[] args) {
        String[] a = { "Каждый "," охотник "," желает "," знать "," где "," сидит "," фазан "};
        
        //Выводим изначальный массив в консоль
        for (int i=0; i<a.length; i++){
            System.out.print(a[i]);
        }
        
        System.out.println();
        
        int n = a.length;
 
        for (int i = 0; i < n/2; i++) {
            //Переменная, которая будет использоваться при обмене элементов
            String temp = a[n-i-1]; // a[7 - 0 - 1] == фазан
            a[n-i-1] = a[i]; // a[6] -> фазан = a[0] -> Каждый
            a[i] = temp;
        }
        //Выводим конечный массив в консоль
        for (int i=0; i<a.length; i++){
            System.out.print(a[i]);
        }
        
        System.out.println();
        
        int[] b = {1, 2, 3, 4, 5, 6, 7};
        
        for(int i = 0; i < b.length/2; i++) {
            int temp = b[b.length - i - 1];
            b[b.length - i - 1] = b[i];
            b[i] = temp;
        }
        
        for(int number : b) {
            System.out.print(number + " ");
        }
        
        System.out.println();
    }
}
```