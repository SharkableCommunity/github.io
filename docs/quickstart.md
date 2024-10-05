add package from nuget
```bash
dotnet add package Sharkable --version 0.0.24
```
or  using package reference
```xml
<PackageReference Include="Sharkable" Version="0.0.24" />
```
add using in your project
```csharp
using Sharkable
```

add Sharkable services(normal mode)
```csharp 
builder.Services.AddShark();
```

add Sharkable services(aot mode) \
(for aot users please specify assemblies by youself and avoid code trim)
```csharp
build.Services.AddShark([typeof(Program).Assembly]);
```

add use for application
```csharp
var app = builder.Build();

//add this line
app.UseShark();
```

there you go, enjoy the freedom of Sharkable!