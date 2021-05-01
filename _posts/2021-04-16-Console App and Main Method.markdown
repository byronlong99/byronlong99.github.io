---
layout: post
title:  Console App and Main Method
date:   2021-04-16 21:27:49 -0400
categories: basics
background: /assets/img/consoleapp/helloworld.png
lang: en
ref: console
---

This blog is intended to give a straightforward, explanation of programming concepts starting from the beginning in .NET.  However, I will omit the setup of the IDE and creation of the project. Since this is **the .NET CORE** we will use C# as the example language, but most (if not all) of the concepts are applicable to all languages.

To have a program, we must first have a **starting point**. The **main method** provides us with our starting point. When we execute the program, it will begin on line **9** in the below code block. The resulting output of the console would be **“Hello World”** and the program would terminate since there are no more lines of code to execute.

{% highlight csharp linenos %}
using System;
 
namespace ConsoleApp
{
    static class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
        }
    }
}
{% endhighlight %}

The only executable code in this example is line **9**.  

Output below:

{% highlight console %}
C:\ConsoleApp\bin\Debug\netcoreapp3.1>ConsoleApp.exe
Hello World!
{% endhighlight %}



The **console** represents the the command window above and we can either write text to it (in the form of a string, more on this later) or read text from it (also in the form of a string).

# Reading from a Console App

While the above example demonstrates how we write to the console, sometimes, it is necessary to read from one.  In the below example the console app will print "Please enter your name..." and pause.

{% highlight csharp linenos %}
using System;

namespace ConsoleApp
{
    static class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Please enter your first name...");
            string firstName = Console.ReadLine();
            Console.WriteLine("Please enter your last name...");
            string lastName = Console.ReadLine();
            Console.WriteLine("Your name is: " + firstName + " " + lastName);
        }
    }
}
{% endhighlight %}

{% highlight console %}
C:\ConsoleApp\bin\Debug\netcoreapp3.1>ConsoleApp.exe
Please enter your first name...
Billy
Please enter your last name...
Bob
Your name is Billy Bob
{% endhighlight %}

You can then type in your first name, press enter, then type your last name, and press enter once again.  If you typed "Billy", then "Bob" for example, the program would output "Your name is Billy Bob".