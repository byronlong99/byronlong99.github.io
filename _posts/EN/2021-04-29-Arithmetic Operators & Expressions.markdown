---
layout: post
title:  Arithmetic Operators & Expressions
date:   2021-04-29 21:27:49 -0400
categories: basics
background: /assets/img/expressions/banner.jpg
lang: en
ref: arithmetic operators and expressions
---

Without **arithmetic operators** and **expressions**, we would be have no ability to manipulate or change **variables**.  In the previous post, we saw a simple example of the addition operator (+).  

There are 5 basic arithmetic operators available in **C#**:

* **\+** (the **addition** operator. i.e. **5** + **3**, adds **3** to **5**. result: **8**)
* **\-** (the **subtraction** operator. i.e. **5** - **3**.  subtracts **3** from **5**.  result: **2**)
* **\*** (the **multiplication** operator. i.e. **5** * **3**. multiplies **5** by **3**. result: **15**)
* **\\** (the **division** operator. i.e. **5 / **3**. divides **5** by **3**. result: **1**)
* **%** (the **remainder division** operator. i.e. **5** % **3** divides **5** by **3** and takes the remainder. result: **2**)

A simple example of the addition operator:

{% highlight csharp %}
int c;

c = 5 + 3;
{% endhighlight %}

After the above code has run.  the variable **c** would have the value of **8** since the result of **5 + 3** is **8**.  The same is would be true if **5** and **3** were replaced by variables.  Let's replace the hard coded **5 + 3** with variables.

{% highlight csharp %}
int a = 5;
int b = 3;

int c = a + b;
{% endhighlight %}

Once again the value of **c** would be **8**.  This example is still very simple.  Let's make it more complicated!  What if instead, we had **3** numbers to add.  What order would they be added in.  The operators go from left to right. 

In the example below, **a** + **b** (**5** + **3**) would be evaluated first to **8**.  Then we would have **8** + **c** (**8** + **1**) which would evaluate to **9**.

{% highlight csharp %}
int a = 5;
int b = 3;
int c = 1;

int d = a + b + c;
{% endhighlight %}

**d** would be **9** after this section of code runs.

##### Precendence of Operators

* **-**, **/**
* **+**, **\***, **%**

Operators of the same precedence will execute from left to right.  However, multiplication and division will execute before addition and subtraction even if they occur farther to the right of the expression. 

In this example.  The part of the expression **b** * **c** (**3** x **2**) will execute first.  This leaves us with **a** + **6** (**5** + **6**).  This will evaluate to **11**.

{% highlight csharp %}
int a = 5;
int b = 3;
int c = 2;

int d = a + b * c;
{% endhighlight %}

##### Using parenthesis () to indicate precendance

Parentheses can also be used to indicate precedence.  In the example above, the multiplication operation occurs after addition, since addition has higher precedence.  However, if we instead add parentheses 