# C#_Notes
- object-oriented programming language
- Created Microsoft
- Runs on the .NET Framework
- roots from the C family
- close to C++ and Java
- Most popular
- easy to learn
- huge community
- clear structure, reusable, lowering dev costs

# Create project
cmd:    cd C:\Users\ljhha\Documents\C\
cmd:    dotnet new console  // create project
cmd:    code .              // open project in vCode

# Run C# CMD
# setup: https://www.youtube.com/watch?v=CO4BGZOuUkM
cmd:    dotnet run          // or use the play button

# Execution
static void Main(string[] args){}

# File Type
# Unlike Java, the name of the C# file does not have to match the class name, 
# but they often do (for better organization)
filename.cs

# Import Console Class
using System;

# Print
Console.WriteLine("Hello World!");
Console.Write("Hello World! "); // does not create a new line afterward

# .NET version
dotnet --version

# Function: input user-data
# Program asks to write something in the Terminal:
string userName = Console.ReadLine();

# Namespace
- Source: https://www.tutorialspoint.com/csharp/csharp_namespaces.htm
- Is a set of classes
- Its like a Package


// EXAMPLE: declare namespace:
namespace myspace {
  class my class {
    public void func() {}
  }
}

// initiate function
class TestClass {
  static void Main(stirng[] args) {
    myspace.myclass obj = new myspace.myclass();
  obj.func();
  }
}

# Import Static Method
Namespace.Class.func(6));


# -------------------------------------------------------------------
#                               VARIABLE
# -------------------------------------------------------------------

# Variables
int myNum = 5;               // Integer (whole number)
double myDoubleNum = 5.99D;  // Floating point number
float myNum = 5.75F;
char myLetter = 'D';         // Character
bool myBool = true;          // Boolean
string myText = "Hello";     // String

# Variables - Many 
int x = 5, y = 6, z = 50;
int x, y, z;
x = y = z = 50;

# Variables - Constant (unchangeable)
const int myNum = 15;

# TypeCasting
Implicit Casting (automatically) - converting a smaller type to a larger type size
    char -> int -> long -> float -> double

    int myInt = 9;
    double myDouble = myInt;       // Automatic casting: int to double

Explicit Casting (manually) - converting a larger type to a smaller size type
    double -> float -> long -> int -> char

    double myDouble = 9.78;
    int myInt = (int) myDouble;    // Manual casting: double to int

# Convert
Convert.ToString(myInt));    // convert int to string
Convert.ToDouble(myInt));    // convert int to double
Convert.ToInt32(myDouble));  // convert double to int
Convert.ToString(myBool));   // convert bool to string

# String to Int
int numVal = Int32.Parse("-105");

# String to Char list
using System.Collections.Generic;
char[] characters = str.ToCharArray();

# int to char
char.GetNumericValue(x);

# Multi List
List<List<int>> list = new List<List<int>>();
list.Add(new List<int>()); //adds a new list to your list of lists
list[0].Add(1); //adds a value to the first list
list[0].Add(2); //adds a value to the first list
Console.WriteLine(list[0][0]); //gets the first value in your first list
Console.WriteLine(list[0][1]); //gets the second value in your first list

list.Add(new List<int>()); //adds a new list to your list of lists
list[1].Add(3); //adds a value to the second list
list[1].Add(4); //adds a value to the second list
Console.WriteLine(list[1][0]); //gets the first value in your second list
Console.WriteLine(list[1][1]); //gets the second value in your second list

# Get Multi list
multiList[0][0]


# -------------------------------------------------------------------
#                               Method
# -------------------------------------------------------------------

# input array
myMethod(new int[] {1,2,3,4,5})


# -------------------------------------------------------------------
#                               MATH
# -------------------------------------------------------------------

# get highest value
Math.Max(5, 10); // 10

# get lowest value
Math.Min(5, 10); // 5

# get square root
Math.Sqrt(64); // 8

# get absolute (positive)
Math.Abs(-4.7); // 4.7

# get nearest value
Math.Round(9.99); // 10

# Modulus (Arithmetic Operators)
x % y

# Pow
 Math.Pow(10, 8))

# Math array ( perform mathematical operations such as Sum, Min, Max, Average, etc.)
 int[] arr = { 10, 15, 20 };
      // Multiplication
      int res = arr.Aggregate((x, y) => x * y);
      Console.WriteLine(res);

# -------------------------------------------------------------------
#                               STRING
# -------------------------------------------------------------------

# String - Length (size)
string txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
Console.WriteLine("The length of the txt string is: " + txt.Length);

# String - Up- / Lower Case
string txt = "Hello World";
Console.WriteLine(txt.ToUpper());   // Outputs "HELLO WORLD"
Console.WriteLine(txt.ToLower());   // Outputs "hello world"

# String - Concatenation
string name = firstName + lastName;
string name = string.Concat(firstName, lastName);

# String Interpolation (Formatting)
string firstName = "John";
string lastName = "Doe";
string name = $"My full name is: {firstName} {lastName}";

# String Access
string myString = "Hello";
Console.WriteLine(myString[0]);             // Outputs "H"

# Index Of
string myString = "Hello";
Console.WriteLine(myString.IndexOf("e"));  // Outputs "1"

# Quotes
string txt = "I'm \"Vikings\"  Dirk.";      // I'm "Vikings" Dirk. 
string txt = "It\'s alright.";              // It's alright. 
string txt = "Character \\ is.";            // Character \ is.

# Remove outsite spaces
" test ".Trim()

# Escape Characters
\n 	New Line 	
\t 	Tab 	
\b 	Backspace


# -------------------------------------------------------------------
#                               Loop
# -------------------------------------------------------------------

# foreach
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
foreach (string i in cars) 
{
  Console.WriteLine(i);
}

# -------------------------------------------------------------------
#                               Array
# -------------------------------------------------------------------

# Declare Array
string[] cars = new string[4];

int[] myNumbers = {5, 1, 8, 9};
      Console.WriteLine(myNumbers.Max());  // returns the largest value
      Console.WriteLine(myNumbers.Min());  // returns the smallest value
      Console.WriteLine(myNumbers.Sum());  // returns the sum of elements

# Sum
public static double SumArray(double[] array) => array.Sum();

# Average
public static int arrAverage(int[] arr) => arr.Average();

# Contain Object
public static bool Check3(object[] a, object v) => a.Contains(v);

# Change all values
Array.ConvertAll(x, n => n * 2); // each value times 2 

# List
List<int> myList = new List<int>();
myList.Add(1);                    // adding element
myList.Insert(1, 11);             // inserts at index

Console.WriteLine(myList[0]);     // get element
numbers.Contains(10);             // contains element

numbers.Remove(10);               // removes the element
numbers.RemoveAt(2);              // removes from index

myList.AddRange(cities);          // convert array to list
int[] array = list.ToArray();     // convert list to array

# Delete duplicates from list
myList = myList.Distinct().ToList();

# ------------------------------------------------------------------- 
#                               Condition
# -------------------------------------------------------------------

# Ternary Operator
string result = (time < 18) ? "Good day." : "Good evening.";

# Switch
      switch(op){
        case '+': return val1+val2;
        case '-': return val1-val2;
        case '*': return val1*val2;
        case '/': return val1/val2;
        default:
           throw new System.ArgumentException("Unknown operation!", op.ToString());
      }

# ------------------------------------------------------------------- 
#                               String
# -------------------------------------------------------------------

# Split
public static string[] StringToArray(string str) => str.Split(" ");

# Sub
public static string getSub(string str) => str.Substring(0,1);

# Contains
str.Contains("hello")

# ------------------------------------------------------------------- 
#                               Lambda
# -------------------------------------------------------------------

# Lambda
 public static int LitresLambda(double time) => (int)time/2;

# Where Function
var oldList = new List<int> {0,1,2,3,4,5,6,7,9};
var newList = oldList.Where(item => item > 5);

# All Function
var game list = new List<Game> {
  new Game {Name"Doom", Score=8},
  new Game {Name"Halo", Score=7},
  new Game {Name"Mario", Score=9}
};

// if all items satisfy our condition
bool AllHave9ScoreOrBetter = gameList.All(g => g.SteamScore >= 9); // false

# Select Function
List<string> gameNames = gameList.Select(g => g.Name).ToList; // Doom, Halo, Mario

# First (get first item that meets the condition)
Game gameWithScoreOf2 = gameList.First(g => Score == 7); // Halo
Game gameWithScoreOf2 = gameList.FirstOrDefault(g => Score == 5); // null

# OrderBy
List<string> orderScore = gameList.orderBy(g => g.Score).ToList; // Doom, Halo, Mario

# Take (take the first num of items from list)
List<string> orderScore = gameList.Take(2).ToList; // Doom, Halo



# ------------------------------------------------------------------- 
#                               Properties
# -------------------------------------------------------------------

public class Person
{ 
  // declare
  public string FirstName { get; set; }
  public string LastName { get; set; }
}

class Program 
{
// initialize
Person obj = new Person();
obj.FirstName = "Tim";
obj.LastName = "Hart";
}

// initialize list
List<Person> people new List<Person>();
people.Add(new Person { FirstName = "Sean", LastName = "Cowboy" });
people.Add(new Person { FirstName = "Jeff", LastName = "Fish" });
people.Add(new Person { FirstName = "Jul", LastName = "Pink" });