### Scaffhold,build,publish .net core app
```bash
$ dotnet new console -o app1
$ dotnet restore -r osx.10.10-x64
$ dotnet build -r osx.10.10-x64
$ dotnet publish -c Release -o ~/app2 -r osx.10.10-x64
$ ~/app2/app1
```

>PS: Key thing here is before running dotnet restore make sure RuntimeIdentifier is set in .csproj file.
>More Info 
>https://docs.microsoft.com/en-us/dotnet/articles/core/rid-catalog 
>Ex:    <RuntimeIdentifiers>osx.10.11-x64</RuntimeIdentifiers>

### Dockerizing Standalone Application
```bash
$ cat Dockerfile
FROM ubuntu/latest
cd ~/app2
MKDIR /opt/app
COPY ~/app2 /opt/app/
RUN /opt/app/app1
```



