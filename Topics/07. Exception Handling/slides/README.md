<!-- section start -->
<!-- attr: { id:'', class:'slide-title', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Exception Handling
## Handling Errors during the Program Execution
<img class="slide-image" src="\imgs\pic01.png" style="top:53.52%; left:50.07%; width:19.55%; z-index:-1" />
<img class="slide-image" src="\imgs\pic02.png" style="top:52.71%; left:73.92%; width:29.62%; z-index:-1" />
<div class="signature">
	<p class="signature-course"></p>
	<p class="signature-initiative"></p>
	<a href="" class="signature-link"></a>
</div>




<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Table of Contents
- What are Exceptions?
- Handling Exceptions
- The System.Exception Class
- Types of Exceptions and their		 Hierarchy
- Raising (Throwing) Exceptions
- Best Practices
<img class="slide-image" src="\imgs\pic03.png" style="top:15.66%; left:82.34%; width:20.28%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# What are Exceptions?
## The Paradigm of Exceptions in OOP
<img class="slide-image" src="\imgs\pic04.png" style="top:52%; left:30.93%; width:42%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# What are Exceptions?
- The `exceptions` in .NET Framework are classic implementation of the OOP exception model
- Deliver powerful mechanism for centralized handling of errors and unusual events
- Substitute procedure-oriented approach, in which each function returns error code
- Simplify code construction and maintenance
- Allow the problematic situations to be processed at multiple levels




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Handling Exceptions
<img class="slide-image" src="\imgs\pic05.png" style="top:42%; left:37.87%; width:34.38%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Handling Exceptions
- In C# the exceptions can be handled by the `try-catch-finally` construction

```cs
try
{
    // Do some work that can raise an exception
}
catch (SomeException)
{
    // Handle the caught exception
}
```

- `catch` blocks can be used multiple times to process different exception types
<img class="slide-image" src="\imgs\pic06.png" style="top:25.56%; left:92.63%; width:12.54%; z-index:0" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Handling Exceptions – _Example_

```cs
static void Main()
{
    string s = Console.ReadLine();
    try
    {
        Int32.Parse(s);
        Console.WriteLine(
           "You entered valid Int32 number {0}.", s);
    }
    catch (FormatException)
    {
        Console.WriteLine("Invalid integer number!");
    }
    catch (OverflowException)
    {
        Console.WriteLine(
           "The number is too big to fit in Int32!");
    }
}
```

<img class="slide-image" src="\imgs\pic07.png" style="top:15.32%; left:83.01%; width:18.76%; z-index:0" />


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Handling Exceptions
<img class="slide-image" src="\imgs\pic08.png" style="top:29.09%; left:65.35%; width:36.61%; z-index:-1" />
<img class="slide-image" src="\imgs\pic09.png" style="top:49.92%; left:22.72%; width:21.23%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# The System.Exception Class
- Exceptions in .NET are objects
- The `System.Exception` class is base for all exceptions in CLR
  - Contains information for the cause of the error / unusual situation
    - `Message` – text description of the exception
    - `StackTrace` – the snapshot of the stack at the moment of exception throwing
    - `InnerException` – exception caused the currentexception (if any)


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Exception Properties – _Example_

```cs
class Exceptions_Example_
{
  public static void CauseFormatException()
  {
    string s = "an invalid number";
    Int32.Parse(s);
  }
  static void Main()
  {
    try
    {
      CauseFormatException();
    }
    catch (FormatException fe)
    {
      Console.Error.WriteLine("Exception: {0}\n{1}",
        fe.Message, fe.StackTrace);
    }
  }
}
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Exception Properties
- The `Message` property gives brief description of the problem
- The `StackTrace` property is extremely useful when identifying the reason caused the exception

```cs
Exception caught: Input string was not in a correct format.
   at System.Number.ParseInt32(String s, NumberStyles style, NumberFormatInfo info)
   at System.Int32.Parse(String s)
   at ExceptionsTest.CauseFormatException() in c:\consoleapplication1\exceptionstest.cs:line 8
   at ExceptionsTest.Main(String[] args) in c:\consoleapplication1\exceptionstest.cs:line 15
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Exception Properties -->
- File names and line numbers are accessible only if the compilation was in `Debug` mode
- When compiled in `Release` mode, the information in the property `StackTrace` is quite different:

```cs
Exception caught: Input string was not in a correct format.
   at System.Number.ParseInt32(String s, NumberStyles style, NumberFormatInfo info)
   at ExceptionsTest.Main(String[] args)
```

<img class="slide-image" src="\imgs\pic10.png" style="top:72%; left:24.33%; width:60.61%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Exception Properties
## [Demo]()
<img class="slide-image" src="\imgs\pic11.png" style="top:52%; left:28.98%; width:50.27%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# The Hierarchy of Exceptions
<img class="slide-image" src="\imgs\pic12.png" style="top:42%; left:35.47%; width:35.67%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Exception Hierarchy
- Exceptions in .NET Framework are organized in a hierarchy
<img class="slide-image" src="\imgs\pic13.png" style="top:27.13%; left:5.55%; width:95.55%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Types of Exceptions
- .NET exceptions inherit from `System.Exception`
- The system exceptions inherit from `System.SystemException`, e.g.
  - `System.ArgumentException`
  - `System.NullReferenceException`
  - `System.OutOfMemoryException`
  - `System.StackOverflowException`
- User-defined exceptions should inherit from `System.Exception` ([more info](http://stackoverflow.com/questions/9037907/applicationexception-base-class-missing/9037944#9037944))


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 40px;' } -->
# Handling Exceptions
- When catching an exception of a particular class, all its inheritors (child exceptions) are caught too
- _Example_:

```cs
try
{
  // Do some works that can cause an exception
}
catch (System.ArithmeticException)
{
    // Handle the caught arithmetic exception
}
```

- 	Handles `ArithmeticException` and its descendants `DivideByZeroException` and `OverflowException`



<img class="slide-image" src="\imgs\pic14.png" style="top:27.99%; left:87.95%; width:15.14%; z-index:0" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 40px;' } -->
# Find the Mistake!

```cs
static void Main()
{
   string s = Console.ReadLine();
   try
   {
      Int32.Parse(s);
   }
   catch (Exception)
   {
      Console.WriteLine("Can not parse the number!");
   }
   catch (FormatException)
   {
      Console.WriteLine("Invalid integer number!");
   }
   catch (OverflowException)
   {
      Console.WriteLine(
       "The number is too big to fit in Int32!");
   }
}
```

<div class="fragment balloon" style="top:38.71%; left:44.08%; width:35.26%">This should be last</div>
<div class="fragment balloon" style="top:52.45%; left:55.24%; width:35.26%">Unreachable code</div>
<div class="fragment balloon" style="top:67.66%; left:55.62%; width:35.26%">Unreachable code</div>


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Handling All Exceptions
- All exceptions thrown by .NET managed code inherit the `System.Exception` exception
- Unmanaged code can throw other exceptions
- For handling all exceptions (even unmanaged) use the construction:

```cs
try
{
    // Do some works that can raise any exception
}
catch
{
    // Handle the caught exception
}
```

<img class="slide-image" src="\imgs\pic15.png" style="top:42.71%; left:88.89%; width:16.75%; z-index:0" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Throwing Exceptions
<img class="slide-image" src="\imgs\pic16.png" style="top:42%; left:32.75%; width:44.08%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Throwing Exceptions
- Exceptions are thrown (raised) by `throw` keyword in C#
  - Used to notify the calling code in case of error or unusual situation
- When an exception is thrown:
  - The program execution stops
  - The exception travels over the stack until a suitable `catch` block is reached to handle it
- Unhandled exceptions display error message


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# How Exceptions Work?



<img class="slide-image" src="\imgs\exceptions-how.png" style="top:10%; left:10%; width:85  %; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Using throw Keyword
- Throwing an exception with an error message:

```cs
throw new ArgumentException("Invalid amount!");
```

- Exceptions can accept message and cause:
- _Note_: if the original exception is not passed the initial cause of the exception is lost

```cs
try
{
  Int32.Parse(str);
}
catch (FormatException fe)
{
  throw new ArgumentException("Invalid number", fe);
}
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Re-Throwing Exceptions
- Caught exceptions can be re-thrown again:

```cs
try
{
  Int32.Parse(str);
}
catch (FormatException fe)
{
  Console.WriteLine("Parse failed!");
  throw fe; // Re-throw the caught exception
}
```


```cs
catch (FormatException)
{
  throw; // Re-throws the last caught exception
}
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Throwing Exceptions – _Example_

```cs
public static double Sqrt(double value)
{
   if (value < 0)
       throw new System.ArgumentOutOfRangeException(
          "Sqrt for negative numbers is undefined!");
   return Math.Sqrt(value);
}
static void Main()
{
   try
   {
       Sqrt(-1);
   }
   catch (ArgumentOutOfRangeException ex)
   {
       Console.Error.WriteLine("Error: " + ex.Message);
       throw;
   }
}
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Throwing Exceptions
## [Demo]()
<img class="slide-image" src="\imgs\pic18.png" style="top:41.39%; left:89.82%; width:13.00%; z-index:-1" />
<img class="slide-image" src="\imgs\pic19.png" style="top:50.44%; left:46.43%; width:22.37%; z-index:-1" />
<img class="slide-image" src="\imgs\pic20.png" style="top:39.63%; left:7.49%; width:22.92%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# Choosing the Exception Type
- When an invalid parameter is passed to a method:
  - `ArgumentException`, `ArgumentNullException`, `ArgumentOutOfRangeException`
- When requested operation is not supported
  - `NotSupportedException`
- When a method is still not implemented
  - `NotImplementedException`
- If no suitable standard exception class is available
  - Create own exception class (inherit `Exception`)




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Using Try-Finally Blocks
<img class="slide-image" src="\imgs\pic21.png" style="top:42%; left:37.67%; width:34.38%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# The try-finally Statement
- The statement:

```cs
try
{
    // Do some work that can cause an exception
}
finally
{
    // This block will always execute
}
```

- Ensures execution of given block in all cases
  - When exception is raised or not in the `try` block
- Used for execution of cleaning-up code, e.g. releasing resources





<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# try-finally – _Example_

```cs
static void TestTryFinally()
{
  Console.WriteLine("Code executed before try-finally.");
  try
  {
    string str = Console.ReadLine();
    Int32.Parse(str);
    Console.WriteLine("Parsing was successful.");
    return; // Exit from the current method
  }
  catch (FormatException)
  {
    Console.WriteLine("Parsing failed!");
  }
  finally
  {
    Console.WriteLine(
      "This cleanup code is always executed.");
  }
  Console.WriteLine(
    "This code is after the try-finally block.");
}
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Try-Finally
## [Demo]()
<img class="slide-image" src="\imgs\pic22.png" style="top:52%; left:45.78%; width:19.39%; z-index:-1" />
<img class="slide-image" src="\imgs\pic23.png" style="top:32.05%; left:80.96%; width:21.57%; z-index:-1" />
<img class="slide-image" src="\imgs\pic24.png" style="top:32.62%; left:7.49%; width:24.68%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Exceptions: Best Practices


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Exceptions – Best Practices
- `catch` blocks should begin with the exceptions lowest in the hierarchy
  - And continue with the more general exceptions
  - Otherwise a compilation error will occur
- Each `catch` block should handle only these exceptions which it expects
  - If a method is not competent to handle an exception, it should be left unhandled
  - Handling all exceptions disregarding their type is popular bad practice (anti-pattern)!


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Exceptions – Best Practices -->
- When raising an exception always pass to the constructor good explanation message
- When throwing an exception always pass a good description of the problem
  - `Exception message` should explain what causes the problem and how to solve it
  - Good: "Size should be integer in range [1…15]"
  - Good: "Invalid state. First call Initialize()"
  - Bad: "Unexpected error"
  - Bad: "Invalid argument"
<img class="slide-image" src="\imgs\pic26.png" style="top:52.19%; left:94.35%; width:12.05%; z-index:-1" />
<img class="slide-image" src="\imgs\pic27.png" style="top:75.53%; left:95.80%; width:10.68%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Exceptions – Best Practices -->
- Exceptions can decrease the application performance
  - Throw exceptions only in situations which are really `exceptional` and should be handled
  - Do not throw exceptions in the normal program control flow (e.g. for invalid user input)
- CLR could throw exceptions at any time with no way to predict them
  - E.g. `System.OutOfMemoryException`


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Summary
- Exceptions provide flexible error handling mechanism in .NET Framework
  - Allow errors to be handled at multiple levels
  - Each exception handler processes only errors of particular type (and its child types)
    - Other types of errors are processed by some other handlers later
  - Unhandled exceptions cause error messages
- Try-finally ensures given code block is always executed (even when an exception is thrown)


<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Exception Handling
## Questions? -->


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Free Trainings @ Telerik Academy
- “C# Programming @ Telerik Academy
    - [csharpfundamentals.telerik.com](csharpfundamentals.telerik.com)
  - Telerik Software Academy
    - [academy.telerik.com](academy.telerik.com)
  - Telerik Academy @ Facebook
    - [facebook.com/TelerikAcademy](facebook.com/TelerikAcademy)
  - Telerik Software Academy Forums
    - forums.academy.telerik.com
<img class="slide-image" src="\imgs\pic28.png" style="top:60.37%; left:92.39%; width:13.45%; z-index:-1" />
<img class="slide-image" src="\imgs\pic29.png" style="top:30.85%; left:68.14%; width:36.30%; z-index:-1" />
<img class="slide-image" src="\imgs\pic30.png" style="top:46.32%; left:95.14%; width:10.85%; z-index:-1" />
<img class="slide-image" src="\imgs\pic31.png" style="top:13.00%; left:92.85%; width:13.01%; z-index:-1" />
