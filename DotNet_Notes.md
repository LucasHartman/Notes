# ASPNETCore_Notes

# Source Code Examples
https://github.com/PacktPublishing/ASP.NET-Core-5-for-Beginners

# .NET
- .NET this is the Common Language Runtime
-  translates your code in real time to the underlying machine code understood by your computer.
- 

# .NET Core
- able to handle cross-platform execution

#  Active Server Pages (ASP)


# ASP.NET MVC 
- visible on the web page where the customer can view the store and its products and perform actions.
-  implementing the Model-View-Controller pattern,
-  products, orders, and so on commonly stored in a database.
- Models:       The products and order.
- Controller:   The actions performed, such as decreasing the number, retrieving pricing info, and so.
- View:         The rendering of output visible to the end user, as well as accepting input from end users

# .NET Standard
- set of APIs that are in the Base Class Library
- 

# Start Project
1. Start Visual Studio and select Create a new Project
2. Select ASP.NET Core Web API - NEXT
3. 


# Configure method 
- runs as a sequence loading features dynamically into the startup for the web hosting process.
-  order of the statements matters, and it's easy to mix this up if you're not paying attention.

# ---------------------------------------------
# 4 Razor View Engine
# ---------------------------------------------

- Building dynamic and data-driven web applications 
- ASP.NET used to have its own engines for rendering dynamic web pages, Active Server Pages (Classic ASP),  Web Forms, which is commonly known as the Web Forms view engine and later ASP.NET MVC 1.0

# Razor view engine
- C#-based template markup syntax for generating HTML with dynamic content.  
- The Razor view engine in the ASP.NET full .NET Framework C# (.cshtml) as the server-side language.
-  if you request a page, the C# code gets executed on the
server. It then processes whatever logic it requires, takes data from somewhere, and then
returns the generated data, along with the HTML that makes up the page, to the browser

# Syntax
-  injecting a server-side code block by using the  @{...} expression

# Syntax - HomeController.class
public IActionResult Index()
{
ViewData[“Message”] = “Razor is Awesome!”;
return View();
}

# Syntax - Index.cshtml
@{
ViewData[“Title”] = “Home Page”;
}

<h1>@ViewData[“Title”]</h1>
<h2>@ViewData[“Message”]</h2>


# MVC: Design Pattern
# Model
Manages the behavior and data
# View
Manages the display of data
# Controller:
Handles page events and navigation

# MVC: steps
1. User:        event
2. Router:      sends event URL
3. Controller:  handles event
4. Model:       action
5. Database:    get data with SQL queries
6. Model:       receives data
7. Controller:  sends data to a View
8. View:        view data in cshtml

# Instance Variable + Getter & Setter
public int Id { get; set; }

