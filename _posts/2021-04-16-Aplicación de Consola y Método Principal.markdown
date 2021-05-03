---
layout: post
title:  Aplicación de Consola y Método Principal
date:   2021-04-16 21:27:49 -0400
categories: basics
background: /assets/img/consoleapp/helloworld.png
lang: es
ref: console
---

Este blog se pretende dar una explicación clara de los conceptos de programación desde la comienza en **.NET**.  Sin embargo, omitiré la organización del editor de código y creación del proyecto.  Ya que esto es el **.NET CORE** usaremos **C#** como el languaje de ejemplo, pero la mayoría (si no todos) de los conceptos son aplicables a todos los languajes.

Para tener un programa, Primero debemos tener un **punto inicial**.  El **método principal** nos provee con nuestro punto inicial.  Cuando ejecutamos el programa, comenzará en la línea nueve en el bloque de código abajo.  La salida resultante sería **"Hola Mundo"** y el programa terminaría ya que no hay mas líneas de código para ejecutar.

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

Mientras que en el ejemplo anterior demuestra como escribimos a la consola, a veces, es necessario leer de una.  En el ejemplo abajo la consola imprimirá "Por favor escribe tu nombre..." y se detendrá.

{% highlight csharp linenos %}
using System;

namespace ConsoleApp
{
    static class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Por favor escribe tu nombre...");
            string nombre = Console.ReadLine();
            Console.WriteLine("Por favor escribe tu apellido...");
            string apellido = Console.ReadLine();
            Console.WriteLine("Tu nombre entero es: " + nombre + " " + apellido);
        }
    }
}
{% endhighlight %}

{% highlight console %}
C:\ConsoleApp\bin\Debug\netcoreapp3.1>ConsoleApp.exe
Por favor escribe tu nombre...
Billy
Por favor escribe tu apellido...
Bob
Tu nombre entero es Billy Bob
{% endhighlight %}

Puedes escribir tu nombre, presionar enter, escribir tu apellido, y presionar enter otra vez.  Si escribiste **"Billy"**, después **"Bob"** por ejemplo, el programa saldría "Tu nombre entero es **Billy Bob**".