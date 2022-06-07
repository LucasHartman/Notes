# DotNet

# Source:ASP.NET Core Crash Course
https://www.youtube.com/watch?v=ZXdFisA_hOY


# ---------------------------------------------------
# Setup
# ---------------------------------------------------

# Version
dotnet --version 

# List of SDK's
dotnet --info

# Change SDK
dotnet new globaljson --sdk-version 5.0.408 --force

# Create Project
dotnet new webapi -n WebApp

# Restart OmniSharp
install: C# Extension (older version)
ctrl+shift+p
OmniSharp: Restart OmniSharp
OmniSharp: Select Project


# Get URL
- Properties > launchSetting.json > Catalog > applicationURL

# Certify Authority
- if the browser complains about "You connection isn't private":
- dotnet dev-certs http --trust

# Run Application
- Ctrl+Shift+d
- Debug Icon > Play Button

# ---------------------------------------------------
# HotKeys
# ---------------------------------------------------

# implement /interface
1. mouse on Interface
2. ctrl+.
3. Implement interface
All of the methods in the interface we show up this class

# ---------------------------------------------------
# Extensions
# ---------------------------------------------------

# C#
- Setup the C# project with OmniSharp for building and debugging

# C# Extensions
- Generate C# file

# Auto-Using for C#
- imports the right package for each new method


# ---------------------------------------------------
# Files
# ---------------------------------------------------

# File: ProjectName.csproject
- Project file
- Framework (set of API's available to the app)
- Packages

# File: Program.cs
- Entry point of this application
- runs Startup.cs

# File: Startup.cs
- Read Configuration properties for multiple sources
- Method: Configure(): Runs additional components that will execute before controller

# File: Controller
- Routes your service

# File: appsettings.json
- declare configuration

# File: appsettings.Development.json
- declare configuration in a Development environment

# File: .vscode > tasks.json
- declares tasks
- declare the build comment

# File: .vscode/launch.json
- Controls what is going to be launched

# File: Properties > launchSetting.json
- get localhost https
- get localhost http

# ---------------------------------------------------
# Syntax
# ---------------------------------------------------

# namespace
- Package name
 
# Record
- public record ClassName {}
- Is a specials class
- Use for immutable objects (like Entities)
- Supports With-expressions
- Supports Value-based equality

# With-expressions
Item potions2 = potions1 with { Price = 12};

# Value-based equality
- 2 instances with the same properties will be seen as equal
- Its like strings in a string-pool: 2 variable address the same object

# type; Guid
- using System;


# init-only properties;
- public property immutable
- once you have defined them, they cannot change

# type; decimal

# IEnumberable<Item>
- Return a Simple list of Items

# ActionResult<Item>
- public ActionResult<Item> Item GetItem(Guide id) {}
- Return more then one type, from this method

# ---------------------------------------------------
# Annotations
# ---------------------------------------------------

# [ApiController]
- Found in the Controller Class
- Brings in a number of default behaviors for the controller class

# [Route("[controller]")]
- Found in the Controller Class
- Route to selected HTTP 
- "[controller]" or "[items]" - select the default controller class (items.cs)

# [HttpGet]
- Found in the Controller Class
- This method will executes when someone goes to this Http

# [Required]
- When values gets posted it can't be a null value

# [Range(1, 1000)]
- Wen value gets posted in must be between the range values

# ---------------------------------------------------
# Class Implementation
# ---------------------------------------------------

# ControllerBase
- public class ItemsController : ControllerBase {}
- ControllerBase makes this class a controller class

# ---------------------------------------------------
# Dependency Injection (DI)
# ---------------------------------------------------



# ---------------------------------------------------
# Develop: MVC (Model View Controller)
# ---------------------------------------------------

# Remove Redundant Files
- WeatherForecast.cs
- Controller > WeatherForecastController.cs

# Create: Models > Item.cs (Entity)
namespace WebApp.Model
{
    public record Item
    {
        public Guid Id {get; init;}
        public string Name {get; init;}
        public decimal Price {get; init}
        public DateTimeOffset CreatedDate {get; init;}
    }
}

# Create: Repo > InMemItemsRepository.cs (Storage)
namespace Catalog.Repositories
{
    public class InMemItemsRepository
    {
        private readonly List<Item> items = new()
        {   // initialize a list of items
            new Item { Id= Guide.NewGuid(), nameof= "Potion", Price=9, CreatedDate=DateTimeOffSet.UTcNow},
            new Item { Id= Guide.NewGuid(), nameof= "Iron Swords", Price=20, CreatedDate=DateTimeOffSet.UTcNow},
            new Item { Id= Guide.NewGuid(), nameof= "Bronze Shield", Price=18, CreatedDate=DateTimeOffSet.UTcNow}
        };

        public IEnumberable<Item> GetItems()
        {   // get all items
            return items;
        }

        public Item GetItem(Guide id)
        {   // get a single item bases on id
            return items.Where(item => item.id==id).SingleOrDefault();
        }

    }
}




