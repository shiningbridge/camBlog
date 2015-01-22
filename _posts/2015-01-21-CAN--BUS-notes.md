---
layout: post
title:  "CAN-BUS notes"
date:   2015-01-21 16:42:18
categories: Hardware
---

# CAN-BUS notes

Multi-drop, Multi-master, serial BUS.

## Characteristics 

- all msg. is broadcasted. 

- bus length / bit rate trade offs. 

- 120 Ohm terminated load.

- CAN-H and CAN-L differential.

## Bit timing
[TODO] add a pic 
[CAN-BUS notes.md](http://www.google.se)


### Four msg. type

+ Data msg. 
+ Remote msg. -- request data Tx.
+ Error msg. 
+ Overload msg. -- request a delay in Tx.

## Message format 
[TODO] add a pic 
[CAN-BUS notes.md](http://www.google.se)

## Error detection
+ Bit error
+ ACK error
+ From error
+ CRC error
+ Stuff error
	* more than 6 (include 6) consequtive bit exist in one Tx. is not allowed. 
	* usually incert a "stuff bit" to terminate consequtive zeros or ones. 

{% highlight  %}

{% endhighlight %}

java
import java.io.*
package javatar.simple.demo;

public class MM {
	public static void main(String[] args) {
		System.out.println("wokao" + "woqu" + 1 );
	}
}
