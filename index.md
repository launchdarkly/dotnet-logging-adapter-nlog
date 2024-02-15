This .NET package provides integration from the [`LaunchDarkly.Logging`](https://launchdarkly.github.io/dotnet-logging) API that is used by the LaunchDarkly [.NET SDK](https://github.com/launchdarkly/dotnet-server-sdk), [Xamarin SDK](https://github.com/launchdarkly/xamarin-client-sdk), and other LaunchDarkly libraries, to [NLog](https://nlog-project.org/).

This adapter is published as a separate NuGet package to avoid unwanted dependencies on NLog in the LaunchDarkly SDKs and in applications that do not use that framework.

## Usage

The **<xref:LaunchDarkly.Logging.LdNLog>** adapter is provided by the NuGet package [**`LaunchDarkly.Logging.NLog`**](https://nuget.org/packages/LaunchDarkly.Logging.NLog). It provides integration with [NLog](https://nlog-project.org/) version 4.5.0 and higher. Earlier versions of NLog are not supported because they only had a .NET Standard 1.6 target framework, and LaunchDarkly libraries do not support .NET Standard 1.6.

NLog has a rich configuration system that allows log behavior to be controlled in many ways. The LaunchDarkly adapter does not define any specific logging behavior itself, so the actual behavior will be determined by how you have configured NLog.

To use the adapter:

1. Add the NuGet package `LaunchDarkly.Logging.NLog` to your project. Make sure you also have a dependency on a compatible version of [NLog](https://nlog-project.org/).

2. Use the property [**LdNLog.Adapter**](xref:LaunchDarkly.Logging.LdNLog.Adapter) in any LaunchDarkly library configuration that accepts a `LaunchDarkly.Logging.ILogAdapter` object. For instance, if you are configuring the LaunchDarkly .NET SDK:

```csharp
using LaunchDarkly.Logging;
using LaunchDarkly.Sdk.Server;

var config = Configuration.Builder("my-sdk-key")
    .Logging(LdNLog.Adapter)
    .Build();
var client = new LdClient(config);
```
