---
layout: post
title:  Aplicación de Consola y Método Principal
date:   2021-04-16 21:27:49 -0400
categories: basics
background: /assets/img/consoleapp/helloworld.png
lang: es
ref: console
---

Este blog se pretende dar una explicación clara de los conceptos de programación desde la comienza en .NET.  Sin embargo, omitiré la organización del editor de código y creación del proyecto.  Ya que esto es el **.NET CORE** usaremos C# como el languaje de ejemplo, pero la mayoría (si no todos) de los conceptos son aplicables a todos los languajes.

Para tener un programa, Primero debemos tener un **punto inicial**.  El **método principal** nos provee con nuestro punto inicial.  Cuando ejecutamos el programa, comenzará en línea nueve en el bloque de código abajo.  La salida resultante sería **"Hola Mundo"** y el programa terminaría ya que no hay mas líneas de código para ejecutar.

{% highlight csharp linenos %}
using System;
 
namespace ConsoleApp
{
    static class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hola Mundo!");
        }
    }
}
{% endhighlight %}

La sola línea de código ejecutable en este ejemplo es línea **9**.

Salida abajo:

{% highlight console %}
C:\ConsoleApp\bin\Debug\netcoreapp3.1>ConsoleApp.exe
Hola Mundo!
{% endhighlight %}

La **consola** representa la ventana de comando arriba y podemos escribirle texto (en la forma de un **string**, mas sobre esto después) o leer texto de él (también en la forma de un **string**).

# Leer de una aplicación de consola

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