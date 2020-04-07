# eventlog-stream-console
A tool, in the form of a NuGet package, that allows streaming of Microsoft EventLog messages to the console.

# Overview
Many .NET legacy apps make use of the Windows Event Log for persisting errors and warnings raised at runtime.  Until recently, the common wisdom for running code that references the Event Log on Cloud Foundry has been, "don't do it".  In other words, refactor all of your calls to EventLog to something more cloudy, like ILogger.Log, or Console.WriteLine.  Now we have a third option:  just use a shim.

By installing this NuGet package to an ASP Framework 4.x app, all calls to the `System.Diagnostics.EventLog.WriteEvent` and `System.Diagnostics.EventLog.WriteEntry` static methods will instead write to console.  As with all shims, this behavior will extend only to your app domain. 

This shim leverages the <a target="tab" href="https://github.com/pardeike/Harmony/wiki">Lib.Harmony</a> NuGet package.

## Contributing

The eventlog-stream-console project team welcomes contributions from the community. Before you start working with eventlog-stream-console, please
read our [Developer Certificate of Origin](https://cla.vmware.com/dco). All contributions to this repository must be
signed as described on that page. Your signature certifies that you wrote the patch or have the right to pass it on
as an open-source patch. For more detailed information, refer to [CONTRIBUTING.md](CONTRIBUTING.md).

## License

eventlog-stream-console is available under the [BSD-2 license](https://github.com/vmware/eventlog-stream-console/blob/master/LICENSE.txt).

