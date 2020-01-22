# .NET Core Interview Questions And Answers

The sun is setting on .NET Framework. From now on, .NET Core is king. New projects, be they web or desktop, should be started in .NET Core. Stay prepared for your next .NET Core Tech Interview with our list of top .NET Core interview questions and answers.

> You could also find all the answers here 👉 https://www.fullstack.cafe/.NET%20Core.

## Q1: What is .NET Core? ⭐

**Answer:**

The .NET Core platform is a new .NET stack that is optimized for open source development and agile delivery on NuGet. 

.NET Core has two major components. It includes a small runtime that is built from the same codebase as the .NET Framework CLR. The .NET Core runtime includes the same GC and JIT (RyuJIT), but doesn’t include features like Application Domains or Code Access Security. The runtime is delivered via NuGet, as part of the ASP.NET Core package.

.NET Core also includes the base class libraries. These libraries are largely the same code as the .NET Framework class libraries, but have been factored (removal of dependencies) to enable to ship a smaller set of libraries. These libraries are shipped as `System.*` NuGet packages on NuGet.org.

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/26908049/what-is-net-core)


## Q2: What is the difference between String and string in C#? ⭐

**Answer:**

`string` is an alias in C# for `System.String`. So technically, there is no difference. It's like `int` vs. `System.Int32`.

As far as guidelines, it's generally recommended to use `string` any time you're referring to an object.
```csharp
string place = "world";
```

Likewise, it's generally recommended to use `String` if you need to refer specifically to the class.
```csharp
string greet = String.Format("Hello {0}!", place);
```

🔗 **Source:** [blogs.msdn.microsoft.com](https://stackoverflow.com/questions/618535/difference-between-decimal-float-and-double-in-net)


## Q3: What is the .NET Framework? ⭐

**Answer:**

The .NET is a Framework, which is a collection of classes of reusable libraries given by Microsoft to be used in other .NET applications and to develop, build and deploy many types of applications on the Windows platform including the following:

*   Console Applications
*   Windows Forms Applications
*   Windows Presentation Foundation (WPF) Applications
*   Web Applications
*   Web Services
*   Windows Services
*   Services-oriented applications using Windows Communications Foundation (WCF)
*   Workflow-enabled applications using Windows Workflow Foundation(WF)

🔗 **Source:** [c-sharpcorner.com](https://www.c-sharpcorner.com/UploadFile/8ef97c/interview-question-on-net-framework-or-clr/)


## Q4: What is .NET Standard? ⭐

**Answer:**

The **.NET Standard** is a formal specification of .NET APIs that are intended to be available on all .NET implementations.

🔗 **Source:** [docs.microsoft.com](https://docs.microsoft.com/en-us/dotnet/standard/net-standard)


## Q5: What is the difference between .NET Core and Mono? ⭐⭐

**Answer:**

To be simple:
* Mono is third party implementation of .Net Framework for Linux/Android/iOs
* .Net Core is Microsoft's own implementation for same.

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/37738106/net-core-vs-mono)


## Q6: What are some characteristics of .NET Core? ⭐⭐

**Answer:**

* **Flexible deployment**: Can be included in your app or installed side-by-side user- or machine-wide.

* **Cross-platform**: Runs on Windows, macOS and Linux; can be ported to other OSes. The supported Operating Systems (OS), CPUs and application scenarios will grow over time, provided by Microsoft, other companies, and individuals.

* **Command-line tools**: All product scenarios can be exercised at the command-line.

* **Compatible**: .NET Core is compatible with .NET Framework, Xamarin and Mono, via the .NET Standard Library.

* **Open source**: The .NET Core platform is open source, using MIT and Apache 2 licenses. Documentation is licensed under CC-BY. .NET Core is a .NET Foundation project.

* **Supported by Microsoft**: .NET Core is supported by Microsoft, per .NET Core Support

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/26908049/what-is-net-core)


## Q7: What's the difference between SDK and Runtime in .NET Core? ⭐⭐

**Answer:**

* The SDK is all of the stuff that is needed/makes developing a .NET Core application easier, such as the CLI and a compiler.

* The runtime is the "virtual machine" that hosts/runs the application and abstracts all the interaction with the base operating system.

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/47733014/whats-the-difference-between-sdk-and-runtime-in-net-core)


## Q8: What is the difference between decimal, float and double in .NET?  ⭐⭐

**Questions Details:**

When would someone use one of these?


**Answer:**

Precision is the main difference.

* Float - 7 digits (32 bit)
* Double-15-16 digits (64 bit)
* Decimal -28-29 significant digits (128 bit)

As for what to use when:

* For values which are "naturally exact decimals" it's good to use decimal. This is usually suitable for any concepts invented by humans: financial values are the most obvious example, but there are others too. Consider the score given to divers or ice skaters, for example.

* For values which are more artefacts of nature which can't really be measured exactly anyway, float/double are more appropriate. For example, scientific data would usually be represented in this form. Here, the original values won't be "decimally accurate" to start with, so it's not important for the expected results to maintain the "decimal accuracy". Floating binary point types are much faster to work with than decimals.

🔗 **Source:** [blogs.msdn.microsoft.com](https://stackoverflow.com/questions/618535/difference-between-decimal-float-and-double-in-net)


## Q9: What is an unmanaged resource?  ⭐⭐

**Answer:**

Use that rule of thumb: 
* If you found it in the Microsoft .NET Framework: _it's managed_. 
* If you went poking around MSDN yourself, _it's unmanaged_. 

Anything you've used P/Invoke calls to get outside of the nice comfy world of everything available to you in the .NET Framwork is unmanaged – and you're now _responsible_ for cleaning it up.

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/538060/proper-use-of-the-idisposable-interface)


## Q10: What is MSIL? ⭐⭐

**Answer:**

When we compile our .NET code then it is not directly converted to native/binary code; it is first converted into intermediate code known as MSIL code which is then interpreted by the CLR. MSIL is independent of hardware and the operating system. Cross language relationships are possible since MSIL is the same for all .NET languages. MSIL is further converted into native code.  

🔗 **Source:** [c-sharpcorner.com](https://www.c-sharpcorner.com/UploadFile/8ef97c/interview-question-on-net-framework-or-clr/)


## Q11: What is a .NET application domain? ⭐⭐

**Answer:**

It is an isolation layer provided by the .NET runtime. As such, App domains live with in a process (1 process can have many app domains) and have their own virtual address space.

App domains are useful because:

* They are less expensive than full processes
* They are multithreaded
* You can stop one without killing everything in the process
* Segregation of resources/config/etc
* Each app domain runs on its own security level

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/1094478/what-is-a-net-application-domain)


## Q12: Name some CLR services? ⭐⭐

**Answer:**

**CLR services**

*   Assembly Resolver
*   Assembly Loader
*   Type Checker
*   COM marshalled
*   Debug Manager
*   Thread Support
*   IL to Native compiler
*   Exception Manager
*   Garbage Collector

🔗 **Source:** [c-sharpcorner.com](https://www.c-sharpcorner.com/UploadFile/8ef97c/interview-question-on-net-framework-or-clr/)


## Q13: What is CLR? ⭐⭐

**Answer:**

The **CLR** stands for Common Language Runtime and it is an Execution Environment. It works as a layer between Operating Systems and the applications written in .NET languages that conforms to the Common Language Specification (CLS). The main function of Common Language Runtime (CLR) is to convert the Managed Code into native code and then execute the program.

🔗 **Source:** [c-sharpcorner.com](https://www.c-sharpcorner.com/UploadFile/8ef97c/interview-question-on-net-framework-or-clr/)


## Q14: What is CTS? ⭐⭐

**Answer:**

The **Common Type System (CTS)** standardizes the data types of all programming languages using .NET under the umbrella of .NET to a common data type for easy and smooth communication among these .NET languages. 

CTS is designed as a singly rooted object hierarchy with `System.Object` as the base type from which all other types are derived. CTS supports two different kinds of types: 

1. **Value Types**: Contain the values that need to be stored directly on the stack or allocated inline in a structure. They can be built-in (standard primitive types), user-defined (defined in source code) or enumerations (sets of enumerated values that are represented by labels but stored as a numeric type).
2. **Reference Types**: Store a reference to the value‘s memory address and are allocated on the heap. Reference types can be any of the pointer types, interface types or self-describing types (arrays and class types such as user-defined classes, boxed value types and delegates).

🔗 **Source:** [c-sharpcorner.com](https://www.c-sharpcorner.com/UploadFile/8ef97c/interview-question-on-net-framework-or-clr/)


## Q15: What is .NET Standard and why we need to consider it? ⭐⭐

**Answer:**

 1. **.NET Standard** solves the code sharing problem for .NET developers across all platforms by bringing all the APIs that you expect and love across the environments that you need: desktop applications, mobile apps & games, and cloud services:
 2. **.NET Standard** is a **set of APIs** that **all** .NET platforms **have to implement**. This **unifies the .NET platforms** and **prevents future fragmentation**.
 3. **.NET Standard 2.0** will be implemented by **.NET Framework**, .**NET Core**,
    and **Xamarin**. For **.NET Core**, this will add many of the existing APIs
    that have been requested.
 3. **.NET Standard 2.0** includes a compatibility shim for **.NET Framework** binaries, significantly increasing the set of libraries that you can reference from your .NET Standard libraries.
 4. **.NET Standard** **will replace Portable Class Libraries (PCLs)** as the
    tooling story for building multi-platform .NET libraries.

<div class="text-center">
<img src="https://i.stack.imgur.com/tE1ny.png" class="img-fluid" style="max-width: 500px;"/>
</div>

🔗 **Source:** [stackoverflow.com](https://stackoverflow.com/questions/42939454/what-is-the-difference-between-net-core-and-net-standard-class-library-project)


## Q16: What is Kestrel? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q17: Talk about new .csproj file? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q18: What about NuGet packages and packages.config? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q19: What is difference between .NET Core and .NET Framework? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q20: Explain what is included in .NET Core? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q21: What is .NET Standard? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q22: What's the difference between .NET Core, .NET Framework, and Xamarin? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q23: Explain two types of deployment for .NET Core applications ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q24: What is CoreCLR? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q25: Is there a way to catch multiple exceptions at once and without code duplication? ⭐⭐⭐

**Questions Details:**

Consider:
```csharp
try
{
    WebId = new Guid(queryString["web"]);
}
catch (FormatException)
{
    WebId = Guid.Empty;
}
catch (OverflowException)
{
    WebId = Guid.Empty;
}
```
Is there a way to catch both exceptions and only call the `WebId = Guid.Empty` call once?


 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q26: Why to use of the IDisposable interface? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q27: Explain the difference between Task and Thread in .NET ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q28: What is FCL? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q29: What's is BCL? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q30: What is implicit compilation? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q31: What is JIT compiler? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q32: What is Explicit Compilation? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q33: What are the benefits of explicit compilation? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q34: What does Common Language Specification (CLS) mean? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q35: Explain the difference between “managed” and “unmanaged” code? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q36: What is the difference between .NET Standard and PCL (Portable Class Libraries)? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q37: What is the difference between Class Library (.NET Standard) and Class Library (.NET Core)? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q38: When should we use .NET Core and .NET Standard Class Library project types? ⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q39: What is the difference between .NET Framework/Core and .NET Standard Class Library project types? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q40: What's the difference between RyuJIT and Roslyn? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q41: Explain how does Asynchronous tasks (Async/Await) work in .NET? ⭐⭐⭐⭐

**Questions Details:**

Consider:
```csharp
private async Task<bool> TestFunction()
{
  var x = await DoesSomethingExists();
  var y = await DoesSomethingElseExists();
  return y;
}
```
Does the second `await` statement get executed right away or after the first `await` returns?


 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q42: What are benefits of using JIT? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q43: Why does .NET use a JIT compiler instead of just compiling the code once on the target machine? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q44: What is the difference between CIL and MSIL (IL)? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q45: What is the difference between AppDomain, Assembly, Process, and a Thread? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q46: Why does .NET Standard library exist? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q47: How to choose the target version of .NET Standard library? ⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q48: Explain Finalize vs Dispose usage? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q49: What is the difference between Node.js async model and async/await in .NET? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q50: How many types of JIT Compilations do you know? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


## Q51: Could you name the difference between .Net Core, Portable, Standard, Compact, UWP, and PCL? ⭐⭐⭐⭐⭐

 See 👉 **[Answer](https://www.fullstack.cafe/.NET%20Core)**


