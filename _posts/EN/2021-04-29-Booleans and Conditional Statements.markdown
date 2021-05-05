---
layout: post
title:  Booleans and Conditional Statements
date:   2021-04-28 21:27:49 -0400
categories: basics
background: /assets/img/banner.jpg
lang: en
ref: booleans
---

**Booleans** are a type that has 2 possible values, **true** and **false**, nothing more.  It is the simplest of all primitive types.

There are several **operators** that can be used with booleans.  And, or, not, equals, etc.  For example, **true** && **false** would be **false** since both parts are not true.  **true** \|\|  **false** would be **true**.

##### Boolean Operators:


A       |       B       | AND           |   OR       |
------- | ------------- | -----------   | ---------- |
false   |   false       |   **false**   |  **false** |
false   |   true        |   **false**   |  **true**  |
true    |   false       |   **false**   |  **true**  |
true    |   true        |   **true**    |  **false** |

Here is some code to demonstrate the and (**&&**) operator: 

{% highlight csharp %}
bool booleanA = true;
bool booleanB = false;

bool resultingBoolean = booleanA && booleanB;
{% endhighlight %}

After the above code runs, the value of **resultingBoolean** would be **"true"** since both **booleanA** and **booleanB** are not true.

Demonstration of or (**\|\|**) operator:

{% highlight csharp %}
bool booleanA = true;
bool booleanB = false;

bool resultingBoolean = booleanA || booleanB;
{% endhighlight %}

In the example above, the resulting value of **resultingBoolean** would be **"true"** since **booleanA** is true and **booleanB** is false.

Demonstration of not (**!**) operator:

{% highlight csharp %}
bool booleanA = true;

bool resultingBoolean = !booleanA;
{% endhighlight %}

Resulting value of **resultingBoolean** would be **"false"** since **booleanA** is true.

Here is the list of operators:

* **&&** (and, this is **true** if both parts are **true**)
* **\|\|** (or, this is true if either part is true)
* **!** (not, this make false true and true)

From these

### Conditionals