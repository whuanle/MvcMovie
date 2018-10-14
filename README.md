### **项目说明**
微软官方ASP.NET Core中文教程    创建 MVC Web 应用
https://docs.microsoft.com/zh-cn/aspnet/core/tutorials/first-mvc-app/?view=aspnetcore-2.1

该项目为 [**创建 MVC Web 应用**] 这一章节的源代码

------------------------------
### **初始化数据库构架**
项目使用了EF，无需自己在数据库建表

(1)vs 2017 下使用PMC
[![英文](https://docs.microsoft.com/zh-cn/aspnet/core/tutorials/first-mvc-app/adding-model/_static/pmc.png?view=aspnetcore-2.1 "英文")](https://docs.microsoft.com/zh-cn/aspnet/core/tutorials/first-mvc-app/adding-model/_static/pmc.png?view=aspnetcore-2.1 "英文")
---
在 PMC 中，输入以下命令：
`Add-Migration Initial`  
`Update-Database`

----
`Add-Migration `命令创建代码以创建初始数据库架构。  
此架构基于（Data/MvcMovieContext.cs 文件中的）DbContext 中指定的模型。 Initial 参数用于为迁移命名。   
可以使用任意名称，但是按照惯例应选择描述迁移的名称。 有关详细信息，请参阅迁移简介。
`Update-Database `命令在用于创建数据库的 Migrations/<time-stamp>_Initial.cs 文件中运行 Up 方法。
还可以使用命令行接口 (CLI) 来执行前面的步骤，而不使用 PMC：
将 EF Core 工具添加到 .csproj 文件。
从控制台（在项目目录中）运行以下命令：
`dotnet ef migrations add Initial`  
`dotnet ef database update`
