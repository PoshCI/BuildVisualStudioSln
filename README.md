####What is it?

A [PoshCI](https://github.com/PoshCI/PoshCI) step that builds one or more [Visual Studio](http://www.visualstudio.com) solutions

####How do I install it?

```PowerShell
Add-CIStep -Name "YOUR-CISTEP-NAME" -ModulePackageId "BuildVisualStudioSln"
```

####What parameters are available?

#####IncludeSlnFilePath
A String[] representing included .sln file paths. Either literal or wildcard paths are allowed; Default is all .sln files within the project root dir @ any depth
```PowerShell
[String[]]
[Parameter(
    ValueFromPipelineByPropertyName=$true)]
$IncludeSlnFilePath
```

#####Recurse
a Switch representing whether to include .sln files located in sub directories of $IncludeSlnFilePath (at any depth)
```PowerShell
[Switch]
[Parameter(
    ValueFromPipelineByPropertyName=$true)]
$Recurse
```

#####PathToMsBuildExe
path to msbuild.exe on your machine
```PowerShell
[String]
[Parameter(
    Mandatory=$true,
    ValueFromPipelineByPropertyName=$true)]
$PathToMsBuildExe
```

####What's the build status?
![](https://ci.appveyor.com/api/projects/status/9tp100rf05jd7mcy?svg=true)
