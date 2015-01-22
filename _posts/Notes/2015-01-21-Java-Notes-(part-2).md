---
layout: post
title:  "Java Notes (part 2)"
date:   2015-01-21 13:42:18
categories: java
---
Java Notes (part 2)
===================

## Tips

### 向下转型，加一个判断

```java
class Person{
	private String name ; 
	private int age ; 
	public boolean equals(Object obj){
		if (this==obj){		// 地址相等
			return true ; 
		}
		if (!(obj instanceof Person)) {		// 加一个判断！！
			return false ; 
		}
		Person per = (Person)obj ; 
		if (this.name.euqals(per.name)&&this.age.equals(per.age)){
			return true ;
		}else{
			return false ;
		}
	}
	...
}

```

## Object 类

### 先有老子
代码：

```java
abstract class A {
	public A(){
		this.print();
	}
	public abstract void print();
}
class B extends A{
	private int x = 100;
	public B(int x){
		this.x = x;
	}
	public void print(){
		System.out.println("x = " + x);
	}
}
public class TestJava {
   	public static void main(String[] args) {
 		A a = new B(10); 	 	
   	 } 
}
```

子类实例化之前，父类必须先实例化，即执行构造方法，如果未执行完则不可能调用子类构造方法，所以子类所有属性都不能初始化，没有初始化意味着默认为 0。

