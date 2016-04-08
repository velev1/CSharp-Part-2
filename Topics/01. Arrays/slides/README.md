<!-- section start -->
<!-- attr: { id:'', class:'slide-title', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Arrays
## Processing Sequences of Elements
<img class="slide-image" src="imgs/pic01.png" style="top:50%; left:60%; width:40%; z-index:-1" />
<img class="slide-image" src="imgs/pic02.png" style="top:40%; left:0%; width:25%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Table of Contents
- Declaring and Creating Arrays
- Accessing Array Elements
- Console Input and Output of Arrays
- Iterating Over Arrays Using **for** and **foreach**
- Dynamic Arrays
  - **List<T>**
- Copying Arrays
<img class="slide-image" src="imgs/pic03.png" style="top:44.96%; left:75.04%; width:27.15%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Declaring and Creating Arrays 
<img class="slide-image" src="imgs/pic04.png" style="top:45%; left:80%; width:20%; z-index:-1" />
<img class="slide-image" src="imgs/pic05.png" style="top:55%; left:10.48%; width:58.75%; z-index:-1" />

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# What are Arrays?
- An **array** is a sequence of elements
  - All elements are of the same type
  - The order of the elements is fixed
  - Has fixed size (**Array.Length**)
  
<img class="slide-image" src="imgs/array-5.png" style="top:50%; left:10%; width:80%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Declaring Arrays
- Declaration defines the type of the elements
- Square brackets **[]** mean "array"
- _Examples_:
  - Declaring array of integers:
    ```cs
    int[] myIntArray;
    ```
  - Declaring array of strings:
    ```cs
    string[] myStringArray;
    ```


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Creating Arrays
- Use the operator **new**
  - Specify array length
- _Example_ creating (allocating) array of 5 integers:

```cs
myIntArray = new int[5];
```
<img class="slide-image" src="imgs/creating-array.png" style="top:60%; left:10%; width:60%; z-index:-1" />

<img class="slide-image" src="imgs/pic09.png" style="top:60%; left:75%; width:26%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Creating and Initializing Arrays
- Creating and initializing can be done together:
```cs
myIntArray = {1, 2, 3, 4, 5};
```
- The **new** operator is not required when using curly brackets initialization

<img class="slide-image" src="imgs/creating-array.png" style="top:60%; left:10%; width:60%; z-index:-1" />

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Creating Array – _Example_
- Creating an array that contains the names of the days of the week

```cs
string[] daysOfWeek =
{
    "Monday",
    "Tuesday",
    "Wednesday",
    "Thursday",
    "Friday",
    "Saturday",
    "Sunday"
};
```

<img class="slide-image" src="imgs/pic10.png" style="top:26.10%; left:77.66%; width:24.79%; z-index:1" />


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Days of Week
## [Live Demo]()
<img class="slide-image" src="imgs/pic11.png" style="top:50%; left:65%; width:30%; z-index:-1" />
<img class="slide-image" src="imgs/pic12.png" style="top:5%; left:10%; width:15%; z-index:-1" />
<img class="slide-image" src="imgs/pic13.png" style="top:50%; left:10%; width:35%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Accessing Array Elements
## Read and Modify Elements by Index
<img class="slide-image" src="imgs/pic14.png" style="top:55%; left:30%; width:40%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# How to Access Array Element?
- Array elements are accessed using the square brackets operator **[]** (indexer)
  - Array indexer takes element’s index as parameter
  - The first element has index **0**
  - The last element has index **Length-1**
- Array elements can be retrieved and changed by the **[]** operator


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Reversing an Array – _Example_
- Reversing the contents of an array

```cs
int[] array = new int[] {1, 2, 3, 4, 5};

// Get array size
int length = array.Length;

// Declare and create the reversed array
int[] reversed = new int[length];
        
// Initialize the reversed array
for (int index = 0; index < length; index++)
{
    reversed[length-index-1] = array[index];
}
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Reversing an Array
## [Live Demo]()
<img class="slide-image" src="imgs/pic15.png" style="top:50%; left:65%; width:30%; z-index:-1" />
<img class="slide-image" src="imgs/pic16.png" style="top:55%; left:5%; width:30%; z-index:-1" />
<img class="slide-image" src="imgs/pic17.png" style="top:5%; left:85%; width:20%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Arrays: Input and Output
<img class="slide-image" src="imgs/pic18.png" style="top:55%; left:30%; width:40%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Reading Arrays From the Console
- First, read from the console the length of the array
```cs
int n = int.Parse(Console.ReadLine());
```
- Next, create the array of given size and read its elements in a **for** loop
```cs
int[] arr = new int[n];
for (int i=0; i<n; i++)
{
   arr[i] = int.Parse(Console.ReadLine());
}
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Symmetry Check – _Example_
- Read **int** array from the console and check if it is symmetric:
```cs
bool isSymmetric = true;
for (int i=0; i<array.Length/2; i++)
{
    if (array[i] != array[n-i-1])
    {
        isSymmetric = false;
    }
}
```
<img class="slide-image" src="imgs/symmetric-arrays.png" style="top:70%; left:5%; width:90%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Symmetry Check
## [Live Demo]()
<img class="slide-image" src="imgs/pic19.png" style="top:55%; left:32.5%; width:35%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Printing Arrays on the Console
- Process all elements of the array
- Print each element to the console
- Separate elements with white space or a new line

```cs
string[] array = {"one", "two", "three"};

// Process all elements of the array
for (int index = 0; index < array.Length; index++)
{
    // Print each element on a separate line
    Console.WriteLine("element[{0}] = {1}",
        index, array[index]);
}
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Printing Arrays
## [Live Demo]()
<img class="slide-image" src="imgs/pic20.png" style="top:55%; left:30%; width:40%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Processing Array Elements Using for and foreach
<img class="slide-image" src="imgs/pic21.png" style="top:55%; left:28%; width:40%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Processing Arrays: **for** Statement
- Use **for** loop to process an array when
  - Need to keep track of the index
  - Processing is not strictly sequential from the first to the last element
- In the loop body use the element at the loop index (**array[index]**):

```cs
for (int index = 0; index < array.Length; index++)
{
   squares[index] = array[index] * array[index];
}
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Processing Arrays Using **for** Loop – _Examples_
- Printing array of integers in reversed order:
```cs
Console.WriteLine("Reversed: ");
for (int i = array.Length-1; i >= 0; i--)
{
    Console.Write(array[i] + " ");
}
// Result: 5 4 3 2 1
```
- Initialize all array elements with their corresponding index number:
```cs
for (int index = 0; index < array.Length; index++)
{
    array[index] = index;
}
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Processing Arrays: **foreach**
- How **foreach** loop works?
  - **type** – the type of the element
  - **value** – local name of variable
  - **array** – processing array
```cs
foreach (type value in array)
{
    // statements
}
```
- Used when no indexing is needed
  - All elements are accessed one by one
  - Elements can not be modified (read only)



<img class="slide-image" src="imgs/pic22.png" style="top:29.97%; left:88.07%; width:14.21%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Processing Arrays Using **foreach** – _Example_
- Print all elements of a **string[]** array:

```cs
string[] capitals =
{
    "Sofia",
    "Washington",
    "London",
    "Paris"
};
foreach (string capital in capitals)
{
    Console.WriteLine(capital);
}
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Processing Arrays
## [Live Demo]()
<img class="slide-image" src="imgs/pic23.png" style="top:55%; left:28%; width:40%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Resizable Arrays
## List<T>
<img class="slide-image" src="imgs/pic24.png" style="top:5%; left:75%; width:20%; z-index:-1" />
<img class="slide-image" src="imgs/pic25.png" style="top:53.77%; left:64.56%; width:19.64%; z-index:-1" />
<img class="slide-image" src="imgs/pic26.png" style="top:45%; left:0%; width:35%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
<!-- # Lists (Resizable Arra -->
- **List<T>** – array that can resize dynamically
  - When adding or removing elements
  - Also have indexers **[]** (like arrays)
  - **T** is the type that the list will hold
    - E.g. **List<int>** will hold **integers**
    - **List<object>** will hold **objects**
- Basic methods and properties
  - **Add(T** **element)** – adds new element to the end
  - **Remove(element)** – removes the element 
  - **Count** – returns the current size of the list


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# List _Example_ 

```cs
List<int> intList = new List<int>();
for(int i = 0; i < 5; i++)
{
   intList.Add(i);
}
```

- Is the same as:

```cs
int[] intArray = new int[5];
for(int i = 0; i < 5; i++)
{
   intArray[i] = i;
}
```
- The main difference
  - When using lists we don't have to know the exact number of elements


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px' } -->
# Lists vs. Arrays
- Lets have an array with capacity of 5 elements
```cs
int[] intArray = new int[5];
```
- If we want to add a sixth element (we have already added 5) we have to manually resize
```cs
int[] copyArray = intArray;
int[] intArray = new int[6];
for (int i = 0; i < 5; i++)
{
   intArray[i] = copyArray[i];
}
intArray[5] = newValue;
```
- With **List<T>** we simply call
```cs
list.Add(newValue);
```


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Lists &#60;T>
## [Live Demo]()
<img class="slide-image" src="imgs/pic27.png" style="top:55%; left:55%; width:46.57%; z-index:-1" />
<img class="slide-image" src="imgs/pic28.png" style="top:55%; left:10%; width:25.56%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# How The List<T> Works?
- Why adding new elements is not slow?
  - When adding **n** elements in **List<T>** it resizes itself **log(2)n** times instead of **n**
- Initially a new **List<T>** has size of 0 elements
  - Counter for total capacity (**Capacity**)
  - Counter for number of used capacity (**Count**)
  - When created, both properties of the list have values of 0
  - When adding the first element **Count** becomes 1 and **Capacity** becomes 4


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# How The List<T> Works?
- Initially the **List<T>** is empty
  - When adding new element it is resized
  - But not every time
    - Only when it is needed
- Lets have a list with 3 elements
  - It looks like this:
  - When we add new elementit is appended to the end
  - Adding a fifth element doubles the Capacity of the list
<img class="slide-image" src="imgs/pic29.png" style="top:64.86%; left:73.79%; width:25.46%; z-index:-1" />
<img class="slide-image" src="imgs/pic30.png" style="top:73.54%; left:73.67%; width:25.56%; z-index:-1" />
<img class="slide-image" src="imgs/pic31.png" style="top:82.77%; left:64.10%; width:41.69%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Resizing Lists
## [Live Demo]()
<img class="slide-image" src="imgs/pic32.png" style="top:44.08%; left:72.05%; width:21.16%; z-index:-1" />
<img class="slide-image" src="imgs/pic33.png" style="top:43.91%; left:12.45%; width:21.16%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Copying Arrays
## The Array Class
<img class="slide-image" src="imgs/pic34.png" style="top:55%; left:15.91%; width:23.80%; z-index:-1" />
<img class="slide-image" src="imgs/pic35.png" style="top:55%; left:69.24%; width:22.04%; z-index:-1" />
<img class="slide-image" src="imgs/pic36.png" style="top:60%; left:48.65%; width:13.22%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Copying Arrays
- Sometimes we must **copy** the values from one array to another one
  - If we do it the intuitive way we would copy not only the values but the reference to the array
    - Changing some of the values in one array will affect the other
    ```cs
    int[] copyArray = (int[])array.Clone();
    ```
  - The way to avoid this is using **Clone()**
    - This way only the values will be copied but not the reference
```cs
    int[] copyArray = array;
```


<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
# Summary
- Arrays are a fixed-length sequences of elements of the same type
- Array elements are accessible by index
  - Can be read and modified
- Iteration over array elements can be done with **for** and **foreach** loops
- **List<T>** holds resizable arrays
  - Good when we don't know the number of elements initially

<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Arrays
<img class="slide-image" src="https://github.com/TelerikAcademy/Common/raw/master/revealjs-theme/css/imgs/questions-ninja.png" style="width:70%; top:15%; left:10%" />
<div style="position: absolute; bottom: 1em; right: 0; font-size: 26px;">http://academy.telerik.com</div>
