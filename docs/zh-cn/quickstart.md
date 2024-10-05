从nuget添加包

```bash
dotnet add package Sharkable --version 0.0.24

```

或使用包引用

```xml
<PackageReference Include="Sharkable" Version="0.0.24" />
```

添加在您的项目中

```csharp
using Sharkable

```

添加Sharkable服务 (正常模式)

```csharp
builder.Services.AddShark();

```

添加Sharkable服务 (aot模式)  
(对于aot用户，请自行指定程序集并避免代码修剪)

```csharp
build.Services.AddShark([typeof(Program).Assembly]);

```

添加应用程序的使用

```csharp
var app = builder.Build();

//add this line
app.UseShark();

```

好了，开始享受Sharkable吧!