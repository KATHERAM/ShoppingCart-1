# ShoppingCart
Shopping online from any where

This Project is created for understanding github, CI CD Pipeline enabling

# Sample Application for understanding CI CD
#
# Create Git Repository From Visual Studio 2019
Step 1: Create Application (Console/Windows/Web/others) in visual studio 2019
Step 2: Click "Add to Source Control" appears at vs2019 bottom right corner 
Step 3: Available Source Control List will appear, select Git
Step 4: Github will prompt authentication
Step 5: Commit with comment
Step 6: Click Publish to GitHub - Check in Github Repository new repository will be created with the project name
#
# CI CD Process
Based on the consideration of the firm CI CD can be defined based on their needs.
Continuous Integration Can be considerd one of the bellow points based on firm needs.
1. Master branch check in, build the project. [ As of now this process is considered as CI ] #15-05-2019
2. Master branch check in, build the project, run the test cases successfully.
3. Master branch check in, build the project, run the test cases successfully, run the integration testing successfully
4. Master branch check in, build the project, run the test cases successfully, run the integration testing successfully, 
# 
# 15-05-2019 CI Process
MSBuild - build automation
1. Choose the project folder contains *.csproj 
   Ex: Go to ~\ShoppingCart\ShoppingCart contains ShoppingCart.csproj
2. launch the command prompt
3. type dotnet build
4. hit enter
5. build will run succesfully

Sample execution dotnet build command execution and result
====================================================================================================================

**  Restore completed in 54.13 ms for ~\ShoppingCart\ShoppingCart\ShoppingCart.csproj.
**  ShoppingCart -> ~\ShoppingCart\ShoppingCart\bin\Debug\netcoreapp3.1\ShoppingCart.dll
**  ShoppingCart -> ~\ShoppingCart\ShoppingCart\bin\Debug\netcoreapp3.1\ShoppingCart.Views.dll

====================================================================================================================
~\ShoppingCart\ShoppingCart>dotnet build

Welcome to .NET Core 3.1!
---------------------
SDK Version: 3.1.202

Telemetry
---------
The .NET Core tools collect usage data in order to help us improve your experience. The data is anonymous. It is collected by Microsoft and shared with the community. You can opt-out of telemetry by setting the DOTNET_CLI_TELEMETRY_OPTOUT environment variable to '1' or 'true' using your favorite shell.

Read more about .NET Core CLI Tools telemetry: https://aka.ms/dotnet-cli-telemetry

----------------
Explore documentation: https://aka.ms/dotnet-docs
Report issues and find source on GitHub: https://github.com/dotnet/core
Find out what's new: https://aka.ms/dotnet-whats-new
Learn about the installed HTTPS developer cert: https://aka.ms/aspnet-core-https
Use 'dotnet --help' to see available commands or visit: https://aka.ms/dotnet-cli-docs
Write your first app: https://aka.ms/first-net-core-app
--------------------------------------------------------------------------------------
Microsoft (R) Build Engine version 16.5.0+d4cbfca49 for .NET Core
Copyright (C) Microsoft Corporation. All rights reserved.

  Restore completed in 54.13 ms for ~\ShoppingCart\ShoppingCart\ShoppingCart.csproj.
  ShoppingCart -> ~\ShoppingCart\ShoppingCart\bin\Debug\netcoreapp3.1\ShoppingCart.dll
  ShoppingCart -> ~\ShoppingCart\ShoppingCart\bin\Debug\netcoreapp3.1\ShoppingCart.Views.dll

Build succeeded.
    0 Warning(s)
    0 Error(s)

Time Elapsed 00:00:48.99
====================================================================================================================


Devops Steps
Step 1:
Step 2:
Step 3:
Step 4:
Step 5:
Step 6:

# 15-05-2019 CI Process

