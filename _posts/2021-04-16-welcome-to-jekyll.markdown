---
layout: post
title:  "Console App and Main Method"
date:   2021-04-16 21:27:49 -0400
categories: jekyll update
---

This blog is intended to give a straightforward, explanation of programming concepts starting from the beginning in .NET. However, I will omit the setup of the IDE and creation of the project. Since this is **the .NET Core** we will use C# as the example language, but most (if not all) of the concepts are applicable to all languages.

To have a program, we must first have a **starting point**. The main method provides us with our starting point. When we execute the program, it will begin on line 9 in the below code block. The resulting output of the console would be **“Hello World”** and the program would terminate since there are no more lines of code to execute.

{% highlight csharp %}
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

![My image Name](/assets/img/image.png)

The console represents the the command window above and we can either write text to it (in the form of a string, more on this later) or read text from it (also in the form of a string).

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
