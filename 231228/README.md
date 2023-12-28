# Java의 자료형(숫자와 문자)

<br>

## 1. 숫자(Number)

자바에서는 "" 숫자는 문자로 인식한다.

```java
public class numberType {
    public static void main (String[] args){
        System.out.println(1);        // 1
        System.out.println(1 + 1);    // 2
        System.out.println(1 * 3);    // 3
        System.out.println(4 / 1);    // 4
        System.out.println(15 % 10);  // 5
    }
}
```

<br>

<br>

## 2. 문자(Character)와 문자열(String)

자바는 단일 문자와 문자열을 구분하며, 작은 따옴표 `''` 와 큰 따옴표 `""`로 구분한다.

<br>

### 2.1. 문자(Character)

```java
public class charType {
    public static void main (String[] args){
        System.out.println('가'); // 가
    }
}
```

한 글자에 작은 따옴표를 붙였을 때는 정상적으로 실행된다.

<br>

### 2.2. 문자열(String)

이번에는 문자열을 살펴보자

```java
public class stringType {
    public static void main (String[] args){
        System.out.println("가");
        System.out.println("가나다");
    }
}
```

한 글자 임에도 큰 따옴표로 이상없이 출력된다.

그렇다면 반대로 두 글자 이상에 작은 따옴표를 붙여보자.

```java
public class stringType {
    public static void main (String[] args){
        System.out.println('가나다');
    }
}

// Exception in thread "main" java.lang.Error: Unresolved compilation problem: 
// 	Invalid character constant

// 	at org.dataType.stringType.main(stringType.java:5)
```

위와 같이 에러가 발생한다.

따라서 작은 따옴표는 한글자(문자)에만, 큰 따옴표는 한글자 이상(한글자도 포함된 문자열)일 경우에 사용한다.

<br>

<br>

## 3. 다양한 문자의 표현

문자열을 표현할 때 큰 따옴표를 출력하고 싶거나 다음 줄로 넘겨 출력하고 싶을 떄는 어떻게 해야하는지 알아보자.

<br>

### 3.1. 이스케이프

큰 따옴표는 문자가 시작해서 끝남을 알려주는 약속이다.

문자열 안에서 큰 따옴표를 사용하고 싶다면, 다음과 같이 역슬래시(\)로 표현하여 문자열을 표현하는 큰 따옴표가 아님을 밝혀주면된다.

```java
public class escape {
    public static void main (String[] args){
        System.out.println("char1ey said \"hello world\"");
    }
}

// char1ey said "hello world"
```

<br>

### 3.2. 여러줄 표시

다음으로 알아볼 것은 다음줄로  한 칸 띄어 출력하는 방법이다.

```java
public class multipleLines {
    public static void main (String[] args){
        System.out.println("H\nE\nL\nL\nO\n \nW\nO\nR\nL\nD");
    }
}
// H
// E
// L
// L
// O
//  
// W
// O
// R
// D
// L
```