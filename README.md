


* BootStrap new application
```bash
$ dotnet new console -o app1
```
add below to .csproj xml
```xml
    <RuntimeIdentifiers>osx.10.11-x64</RuntimeIdentifiers>
```
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
