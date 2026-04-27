# .NET Runtime Image

.NET runtime image for running ASP.NET Core and console applications.

## Supported Versions

- .NET 8.0
- .NET 9.0

## Features

- ASP.NET Core runtime
- Console application support
- Multi-platform support (linux/amd64)

## Usage

```dockerfile
FROM __hive__/dotnet-runtime:8.0

# Copy your published app
COPY out/ /app
WORKDIR /app
CMD ["dotnet", "MyApp.dll"]
```

## Building

```bash
dotnet publish -c Release -o out
```
