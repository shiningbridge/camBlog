---
layout: post
title: jekyll on ST3
categories: ['随笔']
tags: ['鞭长莫及']
published: True

---

### let's take a look. 


```java 
<!-- Highlight -->
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

