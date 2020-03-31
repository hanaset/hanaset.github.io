---
layout: page
title: Java Version 별 특징
description: >
 각 자바의 버젼에 대해서 공부한 내용을 정
hide_description: true
---

# Java Version 특징
2019년 6월 본격적으로 Java를  쓰기 시작하면서 Java 8을 주로 쓰다가 우연치 않은 계기로 
<br>Java 13을 접하게 되서 과연 Java의 버젼마다 차이가 무엇인지 공부하고 싶어 포스팅을 하게 되었다.
<br>
<br>리
우선 *@SupportedSourceVersion*이라는 Annotation에서는 Java의 각 버젼에 대해 <br>
간략하게 enum형태로 보여주고 있으나 좀더 자세히 공부해보도록 하자.
```
     * Summary of language evolution
     * 1.1: nested classes
     * 1.2: strictfp
     * 1.3: no changes
     * 1.4: assert
     * 1.5: annotations, generics, autoboxing, var-args...
     * 1.6: no changes
     * 1.7: diamond syntax, try-with-resources, etc.
     * 1.8: lambda expressions and default methods
     *   9: modules, small cleanups to 1.7 and 1.8 changes
     *  10: local-variable type inference (var)
     *  11: local-variable syntax for lambda parameters
     *  12: no changes (switch expressions were in preview)
     *  13: no changes (switch expressions and text blocks in preview)
```

우선 Java8부터 변화를 하나씩 알아보겠다.

Java 8
-
*interface의 변화*
* 기존 인터페이스는 public abstract 메소드만 선언이 가능하였지만, Java 8이 되면서
인터페이스에서도 static, default 메소드를 선언 할수 있게 되었다.
<br>
이것은 항상 Overriding 해야하던 interface애 Overriding이 필요없는 메소드와 전역 메소드를 전언할수 있게 된 것이다.
<br>

*메소드의 직관화*
* lambda에서의 static 메소드와, instance 메소드들이 좀더 직관적으로 쓸수 있게 되었다.<br>
또한 new(생성자) 또한 가능하다.
```
기존 : userList.stream.map(u -> User.check(u));
Java 8 : userList.stream.map(User::check);
``` 
*Optional의 등장*
* Optional을 통해 if문을 통한 Null체크 코드가 필요 없어짐.

Java 9
-
tool적인 부분을 제외하고 언어적인 부분만 이야기를 하자면

*Interface의 private 추가*
* interface 구현에 있어 문제 해결을 위해 private와 private static을 할수 있도록 구현되었음.


### 참고
https://www.baeldung.com/java-8-new-features
