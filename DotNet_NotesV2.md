# DotNet_NotesV2

# ------------------------------------------
# Static Files
# ------------------------------------------

- Source: https://www.tutorialspoint.com/asp.net_core/asp.net_core_static_files.htm
- By default, the wwwroot folder in the ASP.NET Core project is treated as a web root folder.

# Mini Tutorial
1. Source: https://www.nuget.org/packages/Microsoft.AspNet.StaticFiles/1.0.0-rc1-final
2. cmd:    dotnet add package Microsoft.AspNet.StaticFiles --version 1.0.0-rc1-final
3. Add     app.UseStaticFiles(); to startup.cs > configure() methods
4. Create  index.html in side wwwroot directory
5. Run     application
6. Brows:  https://localhost:5001/index.html
7. Add:    app.UseDefaultFiles(); above  app.UseStaticFiles(); to make index.html the default page


# ------------------------------------------
# Exceptions
# ------------------------------------------

Source: https://www.tutorialspoint.com/asp.net_core/asp.net_core_exceptions.htm



# ------------------------------------------
# Packages
# ------------------------------------------

# add package
Source: https://www.tutorialspoint.com/asp.net_core/asp.net_core_project_json.htm
1. download .NET CLIdotnet list package: https://www.nuget.org/
2. cmd: dotnet add package <PACKAGE_NAME> --version <VERSION>
- Or just type the name in the project.json
- Or through the UI > Manage NuGet packages
3. Now go to the Configure() method and invoke app.UseWelcomePage middleware.

# list of package
dotnet list package

# remove package
dotnet remove package <PACKAGE_NAME>


# ------------------------------------------
# Middleware
# ------------------------------------------

Source: https://www.tutorialspoint.com/asp.net_core/asp.net_core_middleware.htm

# Middleware
- Middleware are components that are assembled into an application pipeline
- Each component chooses whether to pass the request on to the 
    next component in the pipeline, 
    and can perform certain actions before and after the 
    next component is invoked in the pipeline.
- Controls how to respond to HTTP requests.
- Controls error.
- Controls authenticate and authorize

# Logger component
- Logger is simply going to record some information
-  pass along this request to the next piece of middleware

# Authorize component
- authorizer might be looking for specific cookie or access tokens in the HTTP headers
- If the authorizer finds a token, it allows the request to proceed. 
- f not, perhaps the authorizer itself will respond to the request with an HTTP error code or redirect code to send the user to a login page.
-  the authorizer will pass the request to the next piece of middleware which is a router.

# Router component
- A router looks at the URL and determines your next step of action.
- The router looks over the application for something to respond to and if the router doesn't find anything to respond to, the router itself might return a 404 Not Found error


# ------------------------------------------
# Files
# ------------------------------------------

# solutionFile.sln
- Open app in Visual Studio.

# global.json
- This file tells ASP.NEt to look for source code.

# project.json
- stores configuration information
- version information
- add dependencies

# Startup.cs
Source: https://www.tutorialspoint.com/asp.net_core/asp.net_core_configuration.htm
1. Startup method
    - configure application
2. Configure method
    - Configure HTTP request
    - Change the pipeline add some code to the configure method
3. ConfigureServices method  
    - configure components for your application.