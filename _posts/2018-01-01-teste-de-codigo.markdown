---
layout: post
title:  "Teste com linhas de código"
date:   2017-09-10 00:00:00 +0000
comments: true
tags: [csharp]
---

Teste de post com código.

<!--more-->

``` csharp
ConsoleColor background = Console.BackgroundColor;  
ConsoleColor foreground = Console.ForegroundColor;  
```

``` csharp
using System;  
class ConsoleColorsClass {  
    static void Main(string[] args) {  
        // Let's go through all Console colors and set them as foreground  
        foreach(ConsoleColor color in Enum.GetValues(typeof(ConsoleColor))) {  
            Console.ForegroundColor = color;  
            Console.WriteLine($ "Foreground color set to {color}");  
        }  
        Console.WriteLine("=====================================");  
        Console.ForegroundColor = ConsoleColor.White;  
        // Let's go through all Console colors and set them as background  
        foreach(ConsoleColor color in Enum.GetValues(typeof(ConsoleColor))) {  
            Console.BackgroundColor = color;  
            Console.WriteLine($ "Background color set to {color}");  
        }  
        Console.WriteLine("=====================================");  
        // Restore original colors  
        Console.ResetColor();  
        Console.ReadKey();  
    }  
}  
```