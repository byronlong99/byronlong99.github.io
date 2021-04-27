---
layout: post
title:  "Console App and Main Method"
date:   2021-04-16 21:27:49 -0400
categories: basics
---

This blog is intended to give a straightforward, explanation of programming concepts starting from the beginning in .NET. However, I will omit the setup of the IDE and creation of the project. Since this is **the .NET Core** we will use C# as the example language, but most (if not all) of the concepts are applicable to all languages.

To have a program, we must first have a **starting point**. The main method provides us with our starting point. When we execute the program, it will begin on line 9 in the below code block. The resulting output of the console would be **“Hello World”** and the program would terminate since there are no more lines of code to execute.

```csharp
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
```

```console
C:\Users\MyAccount\ConsoleApp\ConsoleApp\bin\Debug\netcoreapp3.1>ConsoleApp.exe
Hello World!
```

The **console** represents the the command window above and we can either write text to it (in the form of a string, more on this later) or read text from it (also in the form of a string).

# Reading from a Console App

While the above example demonstrates how we can read from a console app. Sometimes, it is necessary to write from one.  In the below example the console app will print "Please enter your name..." and pause.

```csharp
using System;
namespace ConsoleApp
{
    static class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Please enter your name...");
            string name = Console.ReadLine();
        }
    }
}
```

```console
C:\Users\MyAccount\ConsoleApp\ConsoleApp\bin\Debug\netcoreapp3.1>ConsoleApp.exe
Please enter your name...
```

You can then type in your name.  If you typed "Billy Bob" and pressed enter, for example.  The value of the variable **name** would be "Billy Bob".