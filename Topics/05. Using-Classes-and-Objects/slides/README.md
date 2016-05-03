<!-- section start -->
<!-- attr: { id:'', class:'slide-title', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Using Classes and Objects
## Using the Standard .NET Framework Classes
<img class="slide-image" src="\imgs\pic00.png" style="top:53.40%; left:52.19%; width:17.08%; z-index:-1" />
<img class="slide-image" src="\imgs\pic01.png" style="top:5.92%; left:84.74%; width:19.55%; z-index:-1" />
<img class="slide-image" src="\imgs\pic02.png" style="top:50.50%; left:74.85%; width:33.33%; z-index:-1" />
<div class="signature">
	<p class="signature-course">C# Advanced</p>
	<p class="signature-initiative">Telerik Software Academy</p>
	<a href="https://telerikacademy.com" class="signature-link">https://telerikacademy.com</a>
</div>




<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Table of Contents
- Classes and Objects
  - What are Objects?
  - What are Classes?
- Classes in C#
  - Declaring Class
  - Fields and Properties: Instance and Static
  - Instance and Static Methods
  - Constructors
- Enumerations
<img class="slide-image" src="\imgs\pic03.png" style="top:13.22%; left:85.50%; width:18.18%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
<!-- # Table of Contents -->
- Structures
- Namespaces
- **Random** class
- Introduction to .NET Common Type System
<img class="slide-image" src="\imgs\pic04.png" style="top:14.99%; left:82.34%; width:19.50%; z-index:-1" />
<img class="slide-image" src="\imgs\pic05.png" style="top:48.48%; left:58.38%; width:42.08%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Classes and Objects
## Modeling Real-world Entities with Objects
<img class="slide-image" src="\imgs\pic06.png" style="top:35.59%; left:28.07%; width:52.89%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# What are Objects?
- Software objects model real-world objects or abstract concepts
  - _Examples_:
    - bank, account, customer, dog, bicycle, queue
- Real-world objects have **states** and **behaviors**
  - Account' states:
    - holder, balance, type
  - Account' behaviors:
    - withdraw, deposit, suspend


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
<!-- # What are Objects? -->
- How do software objects implement real-world objects?
  - Use variables/data to implement states
  - Use methods/functions to implement behaviors
- An object is a software bundle of variables and related methods
<img class="slide-image" src="\imgs\pic07.png" style="top:49.37%; left:60.82%; width:41.43%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Objects Represent
- Things from the real world
    - **&#10004;** checks
    - **&#10004;** people
    - **&#10004;** shopping list
- Things from the computer world
    - **&#10004;** numbers
    - **&#10004;** characters
    - **&#10004;** queues
    - **&#10004;** arrays



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# What is a Class?
- The formal definition of **class**:
- Definition by Google

    - **Classes** act as templates from which an instance of an object is created at run time. Classes define the properties of the object and the methods used to control the object's behavior.


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Classes
- Classes provide the structure for objects
  - Define their prototype, act as template
- Classes define:
  - Set of **attributes**
    - Represented by variables and properties
    - Hold their **state**
  - Set of actions (**behavior**)
    - Represented by methods
- A class defines the methods and types of data associated with an object


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Classes – _Example_

```cs
Account
```


```cs
+Owner: Person
+Ammount: double
```


```cs
+Suspend()
+Deposit(sum:double)
+Withdraw(sum:double)
```

<div class="fragment balloon" style="top:15%; left:37.97%; width:23.80%">Class Name</div>
<div class="fragment balloon" style="top:25%; left:37.97%; width:25.03%">Attributes</div>
<div class="fragment balloon" style="top:32%; left:37.97%; width:25.03%">(Properties and Fields)</div>
<div class="fragment balloon" style="top:45%; left:37.97%; width:24.85%">Operations</div>
<div class="fragment balloon" style="top:52%; left:37.97%; width:24.85%">(Methods)</div>


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Objects
- An **object** is a concrete **instance** of a particular class
- Creating an object from a class is called **instantiation**
- Objects have state
  - Set of values associated to their attributes
- _Example_:
  - Class: Account
  - Objects: Ivan's account, Peter's account


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'font-size: 40px;' } -->
# Objects – _Example_

- Class

```cs
Account

+Owner: Person
+Ammount: double

+Suspend()
+Deposit(sum:double)
+Withdraw(sum:double)
```

<div class="fragment balloon" style="top:25%; left:45%; width:14.10%">Class</div>

```cs
ivanAccount

+Owner="Ivan Kolev"
+Ammount=5000.0
```


```cs
peterAccount

+Owner="Peter Kirov"
+Ammount=1825.33
```


<div class="fragment balloon" style="top:60%; left:45%; width:14.10%">Object</div>
<div class="fragment balloon" style="top:80%; left:45%; width:14.10%">Object</div>




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Classes in C#
<img class="slide-image" src="\imgs\pic08.png" style="top:48.93%; left:78.60%; width:25.21%; z-index:-1" />
<img class="slide-image" src="\imgs\pic09.png" style="top:49.37%; left:8.42%; width:50.15%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Classes in C#
- Classes – basic units that compose programs
- Implementation is **encapsulated** (hidden)
- Classes in C# can contain:
  - Fields (member variables)
  - Properties
  - Methods
  - Constructors
  - Inner types
  - Etc. (events, indexers, operators, …)
<img class="slide-image" src="\imgs\pic10.png" style="top:32.29%; left:77.66%; width:24.35%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Classes in C# – _Examples_
- _Example_ of classes (structures):
  - **System.Console**
  - **System.String** (**string** in C#)
  - **System.Int32** (**int** in C#)
  - **System.Array**
  - **System.Math**
  - **System.Random**
  - **System.DateTime**
  - **System.Collections.Generics.List<T>**
<img class="slide-image" src="\imgs\pic11.png" style="top:40.55%; left:71.48%; width:27.86%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Declaring Objects
- An instance of a class or structure can be defined like any other variable:

```cs
using System;
...
// Define two variables of type DateTime
DateTime today;
DateTime halloween;
```

- Instances cannot be used if they are not initialized

```cs
// Declare and initialize a structure instance
DateTime today = DateTime.Now;
```


<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Fields and Properties
## Accessing Fields and Properties
<img class="slide-image" src="\imgs\pic12.png" style="top:52%; left:29.01%; width:48.54%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Fields
- **Fields** are data members of a class
  - Can be variables and constants (read-only)
- Accessing a field doesn’t invoke any actions of the object
  - Just accesses its value
- _Example_:
  - **String.Empty** (the **""** string)
<img class="slide-image" src="\imgs\pic13.png" style="top:51.13%; left:81.40%; width:23.80%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Accessing Fields
- **Constant fields** can be only read
- **Variable fields** can be read and modified
- Usually properties are used instead of directly accessing variable fields
- _Examples_:

```cs
// Accessing read-only field
String empty = String.Empty;

// Accessing constant field
int maxInt = Int32.MaxValue;
```

<img class="slide-image" src="\imgs\pic14.png" style="top:49.60%; left:84.21%; width:17.88%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Properties
- **Properties** look like fields
  - Have name and type
  - Can contain code, executed when accessed
- Usually used as wrappers
  - To control the access to the data fields
  - Can contain more complex logic
- Can have two components called **accessors**
  - **get** for reading their value
  - **set** for changing their value
<img class="slide-image" src="\imgs\pic15.png" style="top:60.83%; left:86.39%; width:18.66%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
<!-- # Properties -->
- According to the implemented accessors properties can be:
  - Read-only (**get** accessor only)
  - Read and write (both **get** and **set** accessors)
  - Write-only (**set** accessor only)
- _Example_ of read-only property:
  - **String.Length**
- _Example_ of read-write property:
  - **Console.BackgroundColor**
<img class="slide-image" src="\imgs\pic16.png" style="top:48.39%; left:86.08%; width:17.96%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Accessing Properties and Fields – _Example_

```cs
using System;
...
DateTime christmas = new DateTime(2009, 12, 25);
int day = christmas.Day;
int month = christmas.Month;
int year = christmas.Year;
Console.WriteLine(
  "Christmas day: {0}, month: {1}, year: {2}",
  day, month, year);
Console.WriteLine(
  "Day of year: {0}", christmas.DayOfYear);
Console.WriteLine("Is {0} leap year: {1}",
  year, DateTime.IsLeapYear(year));
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Accessing Properties and Fields
<img class="slide-image" src="\imgs\pic17.png" style="top:40%; left:65%; width:35%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Instance and Static Members
## Accessing Object and Class Members
<img class="slide-image" src="\imgs\pic18.png" style="top:62%; left:38%; width:25%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Instance and Static Members
- Fields, properties and methods can be:
  - **Instance** (or object members)
  - **Static** (or class members)
- Instance members are specific for each object
  - _Example_: different dogs have different name
- Static members are common for all instances of a class
  - _Example_: **DateTime.MinValue** is shared between all instances of **DateTime**


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Accessing Members – Syntax
- Accessing instance members
  - The name of the **instance**, followed by the name of the member (field or property), separated by dot ("**.**")

  ```cs
  <instance_name>.<member_name>
  ```

- Accessing static members
  - The name of the **class**, followed by the name of the member

```cs
<class_name>.<member_name>
```



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Instance and Static Members – _Examples_
- _Example_ of instance member
  - **String.Length**
    - Each string object has a different length
    - E.g. **"I like C#".Length** &rarr; 9
- _Example_ of static member
  - **Console.ReadLine()**
    - The console is only one (global for the program)
    - Reading from the console does not require to create an instance of it




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Methods
## Calling Instance and Static Methods
<img class="slide-image" src="\imgs\pic19.png" style="top:52%; left:5.61%; width:22.92%; z-index:-1" />
<img class="slide-image" src="\imgs\pic20.png" style="top:52%; left:34.62%; width:39.72%; z-index:-1" />
<img class="slide-image" src="\imgs\pic21.png" style="top:52%; left:81.45%; width:22.92%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Methods
- Methods manipulate the data of the object to which they belong or perform other tasks
- _Examples_:
  - **Console.WriteLine(…)**
  - **Console.ReadLine()**
  - **String.Substring(index, length)**
  - **Array.GetLength(index)**
  - **List<T>.Add(item)**
  - **DateTime.AddDays(count)**
<img class="slide-image" src="\imgs\pic22.png" style="top:55.54%; left:87.95%; width:17.41%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Instance Methods
- **Instance methods** manipulate the data of a specified object or perform any other tasks
  - If a value is returned, it depends on the particular class instance
- Syntax:
  - The name of the instance, followed by the name of the method, separated by dot

```cs
<object_name>.<method_name>(<parameters>)
```



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Calling Instance Methods –  _Examples_
- Calling instance methods of **String**:

```cs
String sampleLower = new String('a', 5);
String sampleUpper = sampleLower.ToUpper();

Console.WriteLine(sampleLower); // aaaaa
Console.WriteLine(sampleUpper); // AAAAA
```

- Calling instance methods of **DateTime**:

```cs
DateTime now = DateTime.Now;
DateTime later = now.AddHours(8);

Console.WriteLine("Now: {0}", now);
Console.WriteLine("8 hours later: {0}", later);
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Calling Instance Methods
## [Demo]()
<img class="slide-image" src="\imgs\pic23.png" style="top:44.96%; left:58.01%; width:38.57%; z-index:-1" />
<img class="slide-image" src="\imgs\pic24.png" style="top:46.36%; left:14.74%; width:22.26%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Static Methods
- **Static methods** are common for all instances of a class (shared between all instances)
  - Returned value depends only on the passed parameters
  - No particular class instance is available
- Syntax:
  - The name of the class, followed by the name of the method, separated by dot

```cs
<class_name>.<method_name>(<parameters>)
```



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Calling Static Methods – _Examples_

```cs
using System;

double radius = 2.9;
double area = Math.PI * Math.Pow(radius, 2);
Console.WriteLine("Area: {0}", area);
// Area: 26,4207942166902

double precise = 8.7654321;
double round3 = Math.Round(precise, 3);
double round1 = Math.Round(precise, 1);
Console.WriteLine(
    "{0}; {1}; {2}", precise, round3, round1);
// 8,7654321; 8,765; 8,8
```

<div class="fragment balloon" style="top:33%; left:26%; width:18.51%">Constant field</div>
<div class="fragment balloon" style="top:33%; left:51%; width:18.51%">Static method</div>
<div class="fragment balloon" style="top:54.23%; left:30%; width:15.87%">Static method</div>
<div class="fragment balloon" style="top:66%; left:32%; width:15.87%">Static method</div>


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Calling Static Methods
## [Demo]()

<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Constructors
- **Constructors** are special methods used to assign initial values of the fields in an object
  - Executed when an object of a given type is being created
  - Have the same name as the class that holds them
  - Do not return a value
- A class may have several constructors with different set of parameters


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
<!-- # Constructors -->
- Constructor is invoked by the **new** operator

```cs
<instance_name> = new <class_name>(<parameters>)
```

- _Examples_:

```cs
String s = new String(new char[]{'a','b','c'});
```




```cs
String s = new String('*', 5); // s = "*****"
```


```cs
DateTime dt = new DateTime(2009, 12, 30);
```


```cs
DateTime dt = new DateTime(2009, 12, 30, 12, 33, 59);
```


```cs
Int32 value = new Int32();
```



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Parameterless Constructors
- The constructor without parameters is called **default**(**parameterless**) constructor
- _Example_:
  - Creating an object for generating random numbers with a default seed

```cs
using System;
...
Random randomGenerator = new Random();
```

<div class="fragment balloon" style="top:72%; left:7.93%; width:68.76%">The class **System.Random** provides generation of pseudo-random numbers</div>
<div class="fragment balloon" style="top:56%; left:55%; width:29.09%">Parameterless constructor call</div>


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Constructor with Parameters
- _Example_
  - Creating objects for generating random values with specified initial seeds

```cs
using System;
...
Random randomGenerator1 = new Random(123);
Console.WriteLine(randomGenerator1.Next());
// 2114319875

Random randomGenerator2 = new Random(456);
Console.WriteLine(randomGenerator2.Next(50));
// 47
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Generating Random Numbers
## [Demo]()

<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# More Constructor _Examples_
- Creating a **DateTime** object for a specified date and time

```cs
using System;

DateTime halloween = new DateTime(2009, 10, 31);
Console.WriteLine(halloween);

DateTime julyMorning =
  new DateTime(2009, 7, 1, 5, 52, 0);
Console.WriteLine(julyMorning);
```

- Different constructors are called depending on the different sets of parameters

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Creating DateTime Objects
## [Demo]()
<img class="slide-image" src="\imgs\pic27.png" style="top:41.43%; left:2%; width:40%; z-index:-1" />


<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Enumerations
## Types Limited to a Predefined Set of Values
<img class="slide-image" src="\imgs\pic28.png" style="top:52%; left:32%; width:35%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Enumerations
- **Enumerations** in C# are types whose values are limited to a predefined set of values
  - E.g. the days of week
  - Declared by the keyword **enum** in C#
  - Hold values from a predefined set

```cs
public enum Color { Red, Green, Blue, Black }
…
Color color = Color.Red;
Console.WriteLine(color); // Red
color = 5; // Compilation error!
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Enumerations
## [Demo]()
<img class="slide-image" src="\imgs\pic29.png" style="top:40%; left:17%; width:26.45%; z-index:-1" />
<img class="slide-image" src="\imgs\pic30.png" style="top:40%; left:61.73%; width:21.17%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Structures
## What are Structures? When to Use Them?

<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Structures
- **Structures** in C# are similar to classes
  - Structures are **value types** (directly hold a value)
  - Classes are **reference types** (pointers)
- Structures are usually used for storing data structures, without any other functionality
- Structures can have fields, properties, etc.
  - Using methods is not recommended
- _Example_ of structure
  - **System.DateTime** – represents a date and time


<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Namespaces
## Organizing Classes Logically into Namespaces

<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# What is a Namespace?
- **Namespaces** are used to organize the source code into more logical and manageable way
- Namespaces can contain
  - Definitions of classes, structures, interfaces and other types and other namespaces
- Namespaces can contain other namespaces
- For example:
  - **System** namespace contains **Data** namespace
  - The name of the nested namespace is **System.Data**


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Full Class Names
- A full name of a class is the name of the class preceded by the name of its namespace

```cs
<namespace_name>.<class_name>
```

- _Example_:
  - **Array** class, defined in the **System** namespace
  - The full name of the class is **System.Array**





<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Including Namespaces
- The **using** directive in C#:

```cs
using <namespace_name>
```

- Allows using types in a namespace, without specifying their full name
- 	_Example_:

```cs
using System;
DateTime date;
```

- 	instead of

```cs
System.DateTime date;
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# The **Random** Class
## Password Generator Demo
<img class="slide-image" src="\imgs\pic34.png" style="top:39.71%; left:6.55%; width:33.50%; z-index:-1" />
<img class="slide-image" src="\imgs\pic36.png" style="top:47.40%; left:64.03%; width:22.92%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# The Random Class
- The **Random** class
  - Generates random integer numbers

```cs
Random rand = new Random();
for (int number = 1; number <= 6; number++)
{
   int randomNumber = rand.Next(49) + 1;
   Console.Write("{0} ", randomNumber);
}
```

- This generates 6 random int in range [1..49]
- Always use a single **Random** instance!
  - This will avoid abnormalities


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Password Generator – _Example_
- Write a program to generate a random password between 8 and 15 characters
  - The password contains of at least two capital letters, two small letters, one digit and  three special characters
- Constructing the password generator class:
  - Start from an empty password
  - Place 2 random capital letters at random positions
  - Place 2 random small letters at random positions
  - Place 1 random digit at random positions
  - Place 3 special characters at random positions


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
<!-- # Password Generator -->
- Now we have exactly 8 characters
  - To make the password length between 8 and 15 we add between 0 and 7 random characters
    - Capital / small letters / digits / special character
    - Inserts each of them at random position
<img class="slide-image" src="\imgs\pic38.png" style="top:51.94%; left:15.61%; width:32.08%; z-index:-1" />
<img class="slide-image" src="\imgs\pic39.png" style="top:48.55%; left:63.41%; width:36.14%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Password Generator Class

```cs
class RandomPasswordGenerator
{
   private const string CapitalLetters=
    "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
   private const string SmallLetters =
    "abcdefghijklmnopqrstuvwxyz";
   private const string Digits = "0123456789";
   private const string SpecialChars =
    "~!@#$%^&*()_+=**{}[]\\|':;.,/?<>";
   private const string AllChars =
    CapitalLetters + SmallLetters + Digits + SpecialChars;
  	 private static Random rnd = new Random();

 // the example continues…
```



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'font-size: 40px;' } -->
<!-- # Password Generator Class -->

```cs
static void Main()
{
   StringBuilder password = new StringBuilder();
   for (int i = 1; i <= 2; i++)
   {
      char capitalLetter = GenerateChar(CapitalLetters);
      InsertAtRandomPosition(password, capitalLetter);
   }
   for (int i = 1; i <= 2; i++)
   {
      char smallLetter = GenerateChar(SmallLetters);
      InsertAtRandomPosition(password, smallLetter);
   }
   char digit = GenerateChar(Digits);
   InsertAtRandomPosition(password, digit);
   for (int i = 1; i <= 3; i++)
   {
      char specialChar = GenerateChar(SpecialChars);
      InsertAtRandomPosition(password, specialChar);
   } 
// the example continues…
```



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'font-size: 40px;' } -->
<!-- # Password Generator Class -->

```cs
   int count = rnd.Next(8);
   for (int i = 1; i <= count; i++)
   {
      char specialChar = GenerateChar(AllChars);
      InsertAtRandomPosition(password, specialChar);
   } 
   Console.WriteLine(password);
}
private static void InsertAtRandomPosition(
   StringBuilder password, char character)
{
   int randomPosition = rnd.Next(password.Length + 1);
   password.Insert(randomPosition, character);
}
private static char GenerateChar(string availableChars)
{
   int randomIndex = rnd.Next(availableChars.Length);
   char randomChar = availableChars[randomIndex];
   return randomChar;
}
```

<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# .NET Common Type System
## Brief Introduction
<img class="slide-image" src="\imgs\pic40.png" style="top:52%; left:14.83%; width:76.91%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
<!-- # Common Type System (C -->
- **CTS** defines all **data** **types** supported in .NET Framework
  - Primitive types (e.g. **int**, **float**, **object**)
  - Classes (e.g. **String**, **Console**, **Array**)
  - Structures (e.g. **DateTime**)
  - Arrays (e.g. **int[]**, **string[,]**)
  - Etc.
- Object-oriented by design


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'font-size: 40px;' } -->
# CTS and Different Languages
- CTS is common for all .NET languages
  - C#, VB.NET, J#, JScript.NET, ...
- CTS type mappings:

| CTS Type       | C# Type | VB.NET Type |
|:---------------|:--------|:------------|
| System.Int32   | int     | Integer     |
| System.Single  | float   | Single      |
| System.Boolean | bool    | Boolean     |
| System.String  | string  | String      |
| System.Object  | object  | Object      |



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# System.Object: CTS Base Type
- **System.Object** (**object** in C#) is a base type for all other types in CTS
  - Can hold values of any other type:

  ```cs
  string s = "test";
  object obj = s;
  ```

- All .NET types derive common methods from **System.Object**, e.g. **ToString()**

```cs
DateTime now = DateTime.Now;
string nowInWords = now.ToString();
Console.WriteLine(nowInWords);
```



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'font-size: 40px;' } -->
# Value and Reference Types
- In CTS there are two categories of types
  - **Value** **types**
  - **Reference types**
- Placed in different areas of memory
  - Value types live in the **execution stack***
    - Freed when become out of scope
  - Reference types live in the **managed heap**(dynamic memory)
    - Freed by the **garbage collector**
- ***_Note_: this does not mean that value types, which are part of reference types live on the stack. E.g., integers in a List&lt;int&gt; do not live on the stack**


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Value and Reference Types – _Examples_
- **Value types**
  - Most of the primitive types
  - Structures
  - _Examples_: **int**, **float**, **bool**, **DateTime**
- **Reference types**
  - Classes and interfaces
  - Strings
  - Arrays
  - _Examples_: **string**, **Random**, **object**, **int[]**


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Value and Reference Types

```cs
int intNum = 5;
DateTime date = DateTime.Now;
int[] intArr = new int[] {5, 6, 7};
string str = "telerik";
```
<img class="slide-image" src="\imgs\values.png" style="top:35%; left:14.83%; width:76.91%; z-index:-1" />



<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Summary
- Classes provide the structure for objects
- Objects are particular instances of classes
- Classes have different members
  - Methods, fields, properties, etc.
  - Instance and static members
  - Members can be accessed
  - Methods can be called
- Structures are used for storing data
- Namespaces group related classes
<img class="slide-image" src="\imgs\pic41.png" style="top:29.97%; left:83.27%; width:21.16%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
<!-- # Summary -->
- Namespaces help organizing the classes
- Common Type System (CTS) defines the types for all .NET languages
  - Values types
  - Reference types
<img class="slide-image" src="\imgs\pic42.png" style="top:34.38%; left:79.53%; width:25.02%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
<!-- # Using Classes and Objects
## Questions?-->


<!-- attr: { id:'', class:'', showInPresentation:true, hasScriptWrapper:true, style:'' } -->
# Free Trainings @ Telerik Academy
- “C# Programming @ Telerik Academy
    - [csharpfundamentals.telerik.com](csharpfundamentals.telerik.com)
  - Telerik Software Academy
    - [academy.telerik.com](academy.telerik.com)
  - Telerik Academy @ Facebook
    - [facebook.com/TelerikAcademy](facebook.com/TelerikAcademy)
  - Telerik Software Academy Forums
    - forums.academy.telerik.com
<img class="slide-image" src="\imgs\pic43.png" style="top:60.37%; left:92.39%; width:13.45%; z-index:-1" />
<img class="slide-image" src="\imgs\pic44.png" style="top:30.85%; left:68.14%; width:36.30%; z-index:-1" />
<img class="slide-image" src="\imgs\pic45.png" style="top:46.32%; left:95.14%; width:10.85%; z-index:-1" />
<img class="slide-image" src="\imgs\pic46.png" style="top:13.00%; left:92.85%; width:13.01%; z-index:-1" />
