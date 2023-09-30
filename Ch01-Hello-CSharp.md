# Hello CSharp (C#)

## Creating Console Apps with Visual Studio Code

We will create a console application from the command line.

Create a new folder.

```cmd
	md VSCode
```

Now, inside this another folder.

```cmd
	md HelloCS
```

Now, inside ``HelloCS`` run the following command.

```cmd
	dotnet new console -f net5.0
```

This is  the old legacy .Net Framework version of the console program.

It creates the following in the folder. The application is named after to folder name. In my case I named the folder ``HelloCS`` so the project will be named ``HelloCS.csproj``.

* Program.cs
* HelloCS.csproj
* obj

Contents of the Program.cs file

```csharp
	using System;
	
	namespace HelloCS
	{
		class Program
		{
			static void Main(string[] args)
			{
				Console.WriteLine("Hello World!");
			}
		}
	}
```

In the legacy code the ``using`` statement is inserted into the boilerplate code.

Open the project in Visual Studio Code.

```cmd
	dotnet build
```

or

```cmd
	dotnet run
```

This command builds and runs the project in one command.

Once you build the project .Net will add a new ``Debug`` folder that contains the executable.

You will also notice that another folder named ``.vscode`` is created with some files that are used by Visual Studio Code to provide features like IntelliSense during debugging.

### Add another project to our solution

Create a new folder inside the ``VSCode`` folder.

```cmd
	md TopLevelProgram
```

Now, make another console program.

```cmd
	dotnet new console -f net7.0
```

This will be the new modern .Net core framework.

Code for ``Program.cs``.

```csharp
	// See https://aka.ms/new-console-template for more information
	Console.WriteLine("Hello, World!");
```

Change the code to.

```csharp
	// See https://aka.ms/new-console-template for more information
	Console.WriteLine("Hello, C#!");

	Console.WriteLine("Hello from a Top Level Program!");
	Console.WriteLine(Environment.OSVersion.VersionString);
```

Run with.

```cmd
	dotnet run
```

Output

> Hello, C#!
> Hello from a Top Level Program!
> Microsoft Windows NT 10.0.22621.0

### Managing multiple files using Visual Studio Code

If you have multiple files that you want to work with at the same time, then you can put them
side by side as you edit them:

1. In EXPLORER, expand the two projects.
2. Open both Program.cs files from the two projects.
3. Click, hold, and drag the edit window tab for one of your open files to arrange them so that you can see both files at the same time.
