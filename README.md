


* BootStrap new application
```bash
$ dotnet new console -o app1
```
add below to .csproj xml
```xml
    <RuntimeIdentifiers>osx.10.11-x64</RuntimeIdentifiers>
```
Refer https://docs.microsoft.com/en-us/dotnet/articles/core/rid-catalog for more targetting other Runtimes.
* Gathering Dependencies
```bash
dotnet restore -r osx.10.10-x64
```
* Build Application
```bash
$ dotnet build -r osx.10.10-x64
```


* Generating Standalone Application For MacosX
```bash
$dotnet publish -c Release -o ~/app2 -r osx.10.10-x64
```

```bash
$~/app2/app1
```
