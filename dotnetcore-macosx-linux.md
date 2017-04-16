* Quick Intro
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
$ dotnet restore -r osx.10.10-x64
$ dotnet build -r osx.10.10-x64
$ dotnet publish -c Release -o ~/app2 -r osx.10.10-x64
$ ~/app2/app1
```
