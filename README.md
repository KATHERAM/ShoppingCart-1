# ShoppingCart

Shopping online from any where

This Project is created for understanding github, CI CD Pipeline enabling

# Sample Application for understanding CI CD

### Create Git Repository From Visual Studio 2019
      Step 1: Create Application (Console/Windows/Web/others) in visual studio 2019
      Step 2: Click "Add to Source Control" appears at vs2019 bottom right corner 
      Step 3: Available Source Control List will appear, select Git
      Step 4: Github will prompt authentication
      Step 5: Commit with comment
      Step 6: Click Publish to GitHub - Check in Github Repository new repository will be created with the project name

### CI CD Process
      Based on the consideration of the firm CI CD can be defined based on their needs.
      Continuous Integration Can be considerd one of the bellow points based on firm needs.
      1. Master branch check in, build the project.
      2. Master branch check in, build the project, run the test cases successfully.
      3. Master branch check in, build the project, run the test cases successfully, run the integration testing successfully
      4. Master branch check in, build the project, run the test cases successfully, run the integration testing successfully, deploy the package
      

### ========= 15-05-2019 CI Process =================
      [ As of now this process is considered as CI ]  And Deploy the publish items to iis
      
      
      
      
      commit
      
      
      commit
      MSBuild - build automation
      1. Choose the project folder contains *.csproj 
         Ex: Go to ~\ShoppingCart\ShoppingCart contains ShoppingCart.csproj
      2. launch the command prompt and run the comamnd - dotnet build
      3. "dotnet build" - build will run succesfully and we can see the below output in command prompt.
            Microsoft (R) Build Engine version 16.5.0+d4cbfca49 for .NET Core
            Copyright (C) Microsoft Corporation. All rights reserved.

            Restore completed in 54.13 ms for ~\ShoppingCart\ShoppingCart\ShoppingCart.csproj.
            ShoppingCart -> ~\ShoppingCart\ShoppingCart\bin\Debug\netcoreapp3.1\ShoppingCart.dll
            ShoppingCart -> ~\ShoppingCart\ShoppingCart\bin\Debug\netcoreapp3.1\ShoppingCart.Views.dll

            Build succeeded.
                0 Warning(s)
                0 Error(s)
      4. package will be created in bin\Debug\netcoreapp3.1 folder
      5. "dotnet run" - Run the application locally
            Ex: Below result will be showned in command prompt, application will be listening on the port
               
               ~\ShoppingCart\ShoppingCart>dotnet run

               info: Microsoft.Hosting.Lifetime[0]
                  Now listening on: http://localhost:5000
               info: Microsoft.Hosting.Lifetime[0]
                  Application started. Press Ctrl+C to shut down.
               info: Microsoft.Hosting.Lifetime[0]
                  Hosting environment: Development
               info: Microsoft.Hosting.Lifetime[0]
                  Content root path: ~\ShoppingCart\ShoppingCart
            
      6. "dotnet publish" - publish the application.
            Ex: dotnet publish --output C:\inetpub\wwwroot\ShoppingCart
            
      7. iis refresh:
            if "iisreset /noforce" not works properly in the system then try to stop it and start it using below commands ref:7.1 & 7.2.
            
            7.1. iisreset /stop
                  Ex:   C:\>iisreset /stop
                  
                        Attempting stop...
                        Internet services successfully stopped\
                        
            7.2. net start w3svc
                  Ex:   C:\>net start w3svc
                        The World Wide Web Publishing Service service is starting.
                        The World Wide Web Publishing Service service was started successfully.

###### DevOps CI/CD pipeline setup in Jenkins

      Step 1: Create a Free style proejct
      
      Step 2: Configure the Git URL under "Source Code Management" section
      
      Step 3: Configure the below commands in Jenkins freestyle job under "Build" section --> Execute Windows Batch Command

                  echo WORKSPACE: %WORKSPACE%

                  cd %WORKSPACE%/ShoppingCart

                  dotnet -h

                  dotnet clean 

                  dotnet build

                  dotnet publish

                  dotnet pack
                  
                  dotnet run

      Step 4:   Launch the URL localhost:5000 in any browser (if you used the command "dotnet" run in your build)       
       

### ========= 15-05-2019 CI Process =================
