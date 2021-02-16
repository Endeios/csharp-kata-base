# CSharp Kata starter

Is A kata starter

## How I like to start a C# Kata

1. make a dotnet solution

```powershell
dotnet new sln
```

2. add a console application project

```powershell
mkdir app
cd app
dotnet new console
cd ..
```

3. add the console app to the solution

```powershell
dotnet sln add .\app\app.csproj
```

4. add a NUnit test project

```powershell
mkdir app.test
cd app.test
dotnet new nunit
cd ..
```

5. add the app.test to the solution

```powershell
dotnet sln add .\app.test\app.test.csproj
```

6. add FakeItEasy and FluentAssertions to app.test

```powershell
cd app.test
dotnet add package FakeItEasy
dotnet add package FluentAssertions
```

7. add the namespaces to the test class

```csharp
...
using FakeItEasy;
using NUnit.Framework; 
using FluentAssertions;
...
```

8. add the app project reference to the app.test

```powershell
dotnet add reference ..\app\app.csproj
```
