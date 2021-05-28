# repro for `Microsoft.Extensions.Logging`

Can't build a project with `Microsoft.Extensions.Logging` version `6.0.0-preview.4.21253.7` when multi targeting:
`dotnet build`

```
Build FAILED.

/usr/local/share/dotnet/sdk/6.0.100-preview.4.21255.9/Sdks/Microsoft.NET.Sdk/targets/Microsoft.NET.EolTargetFrameworks.targets(28,5): warning NETSDK1138: The target framework 'netcoreapp3.0' is out of support and will not receive security updates in the future. Please refer to https://aka.ms/dotnet-core-support for more information about the support policy. [/Users/bruno/git/repro-mel-multi-target/repro-mel-multi-target.csproj]
/usr/local/share/dotnet/sdk/6.0.100-preview.4.21255.9/Sdks/Microsoft.NET.Sdk/targets/Microsoft.NET.EolTargetFrameworks.targets(28,5): warning NETSDK1138: The target framework 'netcoreapp3.0' is out of support and will not receive security updates in the future. Please refer to https://aka.ms/dotnet-core-support for more information about the support policy. [/Users/bruno/git/repro-mel-multi-target/repro-mel-multi-target.csproj]
CSC : error CS0006: Metadata file '/Users/bruno/.nuget/packages/microsoft.extensions.logging/2.1.0/analyzers/dotnet/cs/Microsoft.Extensions.Logging.Generators.dll' could not be found [/Users/bruno/git/repro-mel-multi-target/repro-mel-multi-target.csproj]
CSC : error CS0006: Metadata file '/Users/bruno/.nuget/packages/microsoft.extensions.logging/3.0.0/analyzers/dotnet/cs/Microsoft.Extensions.Logging.Generators.dll' could not be found [/Users/bruno/git/repro-mel-multi-target/repro-mel-multi-target.csproj]
CSC : error CS0006: Metadata file '/Users/bruno/.nuget/packages/microsoft.extensions.logging/5.0.0/analyzers/dotnet/cs/Microsoft.Extensions.Logging.Generators.dll' could not be found [/Users/bruno/git/repro-mel-multi-target/repro-mel-multi-target.csproj]
    2 Warning(s)
    3 Error(s)
```