# webapi_serilog
logging with serilog - web api dotnet core 5.0

Application log files play an important role in analyzing the bugs and for troubleshooting issues in an application, Serilog is a popular third party diagnostic logging library for .NET applications.

you to segregate information from the file easily using Serilog

Below are the required nuget package
  - Serilog.AspNetCore
  - Serilog.Sinks.Async
  - Serilog.Sinks.RollingFile

you can add below code snap to register serilog without registering it on Startup.cs

Go to Program.cs --> IHostBuilder

  UseSerilog((hostingContext, loggerConfig) =>
  loggerConfig.ReadFrom.Configuration(hostingContext.Configuration));


