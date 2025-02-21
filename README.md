# How do C# Top-Level Statements Work?: Code Samples

This is the sample repository for my article on C# top-level statements. 

Written by Benjamin Day  
Pluralsight Author | Microsoft MVP | Scrum.org Professional Scrum Trainer  
https://www.benday.com  
https://www.slidespeaker.ai  
info@benday.com  
YouTube: https://www.youtube.com/@_benday  

## Create the Projects
Here's how how I created the projects.  

The version without the top-level statements:
`dotnet new console`

The version with the top-level statements:
`dotnet new console --use-program-main`

## Install ILDASM

Here's the command to install the `dotnet-ildasm2` tool:
`dotnet tool install dotnet-ildasm2 -g`

## Run the ILDASM Tool

Here are the commands for extracting the IL.  You'll need to compile the projects first and then go into the `bin\debug\net9.0` folder for each project before running the following commands.  

The version without the top-level statements:
`ildasm .\Benday.WithoutTopLevelStatements.dll --output .\Benday.WithoutTopLevelStatements.il.txt`

The version with the top-level statements:
`ildasm .\Benday.WithTopLevelStatements.dll --output .\Benday.WithTopLevelStatements.il.txt`


