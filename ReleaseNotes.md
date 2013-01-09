v1.2
* Refactored for easier reuse by offering two static entry points: 
     - DevEnv.Get: gets the IDevEnv entry point API. This can be 
       used from anywhere you can import an IServiceProvider. By 
       default the instance is reused.
     - Host.Initialize: initializes a hosting package and its components
       (i.e. commands, filters, tool windows, etc.).
* Single assembly now can be used for both VS2010 and VS2012: this means 
  you no longer have to fork your extension for either IDE just because 
  you use Clide (you may because of other dependencies, like VSMSDK).

v1.1
* ISolutionExplorer API, with full solution traversal, behaviors
  for selecting, expanding and collapsing nodes, etc.
* Integration with Adapter pattern for pluggable conversion of 
  solution explorer nodes (i.e. projectNode.As&lt;EnvDTE.Project&gt;())
* Improved diagnostics and debug-time rendering of nodes
* Improved reporting of composition errors in the Clide output window

v1.0
* Full support for MEF-exported commands (ICommandExtension) and command filters
* ToolWindow support
* Tools options pages support