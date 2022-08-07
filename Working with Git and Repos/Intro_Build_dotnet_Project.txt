In dotnet projects we will have a solution and under the solution we can have multiple projects

STEPS to download ans Install .NET
1. Download and Install .NET sdk
2. Open the new terminal / command prompt and check the following command
$ dotnet --version
$ cd ~ && mkdir dotnet && cd dotnet

STEPS to Create Solution and Project
$ dotnet new sln -o HelloWorldApp
# This will create a solution file it will create a dir HelloWorldApp
# This HelloWorldApp directory is the working directory

$ dotnet new mvc -n HelloWorldApp.Web
# This will create the directory with HelloWorldApp.Web with class and project related files explore them
$ cd HelloWorldApp.Web
$ ls -la

# Now the project and solution do not belong to each other
# Need to tie them up to each other
$ cd ..
$ dotnet sln HelloWorldApp.sln add HelloWorldApp.Web/HelloWorldApp.Web.csproj

STEPS to Build Run and Publish
3. In order to build the project in dotnet we require the following commands
$ dotnet dev-certs https --trust
$ dotnet restore        # Downloading all NuGet dependencies to local machine
$ dotnet build          # Builds and generates executable - runs restore and build
After build we can test the application
$ dotnet HelloWorldApp.Web/bin/Debug/net6.0/HelloWorldApp.Web.dll
# Launches dotnet runtime and loads application in it

$ dotnet publish        # This publishes the executable - runs restore, build and publish

$ dotnet publish -o ./myapp/
# This creates the directory myapp in the same directory and observe the dll file
$ cd myapp
$ dotnet HelloWorldApp.Web.dll
# This will run the HelloWorld Applciation in localhost 5000 port

In the browser check the following command and see if the application is running or not
http://localhost:5000
https://localhost:5001



