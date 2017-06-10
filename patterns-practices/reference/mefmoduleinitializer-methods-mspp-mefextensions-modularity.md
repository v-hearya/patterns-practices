---
TOCTitle: MefModuleInitializer Methods
Title: 'MefModuleInitializer Methods (Microsoft.Practices.Prism.MefExtensions.Modularity)'
ms:assetid: 'Methods.T:Microsoft.Practices.Prism.MefExtensions.Modularity.MefModuleInitializer'
ms:mtpsurl: 'mefmoduleinitializer-methods-mspp-mefextensions-modularity.md'
---

# MefModuleInitializer Methods

The [MefModuleInitializer](/patterns-practices/reference/mefmoduleinitializer-class-mspp-mefextensions-modularity) type exposes the following members.

## Methods

<table>

<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[CreateModule(String)](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.moduleinitializer.createmodule(system.string))</td>
<td><div class="summary">
Uses the container to resolve a new [IModule](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.imodule) by specifying its [Type](http://msdn.microsoft.com/en-us/library/42892f65).
</div>
(Inherited from [ModuleInitializer](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.moduleinitializer).)</td>
</tr>
<tr class="even">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[CreateModule(ModuleInfo)](https://msdn.microsoft.com/library/microsoft.practices.prism.mefextensions.modularity.mefmoduleinitializer.createmodule(microsoft.practices.prism.modularity.moduleinfo))</td>
<td><div class="summary">
Uses the container to resolve a new [IModule](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.imodule) by specifying its [Type](http://msdn.microsoft.com/en-us/library/42892f65).
</div>
(Overrides [ModuleInitializer..::.CreateModule(ModuleInfo)](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.moduleinitializer.createmodule(microsoft.practices.prism.modularity.moduleinfo)).)</td>
</tr>
<tr class="odd">
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[Equals](http://msdn.microsoft.com/en-us/library/bsc2ak47)</td>
<td><div class="summary">
Determines whether the specified [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b) is equal to the current [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).
</div>
(Inherited from [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).)</td>
</tr>
<tr class="even">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[Finalize](http://msdn.microsoft.com/en-us/library/4k87zsw7)</td>
<td><div class="summary">
Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.
</div>
(Inherited from [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).)</td>
</tr>
<tr class="odd">
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[GetHashCode](http://msdn.microsoft.com/en-us/library/zdee4b3y)</td>
<td><div class="summary">
Serves as a hash function for a particular type.
</div>
(Inherited from [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).)</td>
</tr>
<tr class="even">
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[GetType](http://msdn.microsoft.com/en-us/library/dfwy45w9)</td>
<td><div class="summary">
Gets the [Type](http://msdn.microsoft.com/en-us/library/42892f65) of the current instance.
</div>
(Inherited from [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).)</td>
</tr>
<tr class="odd">
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[HandleModuleInitializationError](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.moduleinitializer.handlemoduleinitializationerror(microsoft.practices.prism.modularity.moduleinfo%2csystem.string%2csystem.exception))</td>
<td><div class="summary">
Handles any exception occurred in the module Initialization process, logs the error using the [ILoggerFacade](https://msdn.microsoft.com/library/microsoft.practices.prism.logging.iloggerfacade) and throws a [ModuleInitializeException](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.moduleinitializeexception). This method can be overridden to provide a different behavior.
</div>
(Inherited from [ModuleInitializer](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.moduleinitializer).)</td>
</tr>
<tr class="even">
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[Initialize](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.moduleinitializer.initialize(microsoft.practices.prism.modularity.moduleinfo))</td>
<td><div class="summary">
Initializes the specified module.
</div>
(Inherited from [ModuleInitializer](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.moduleinitializer).)</td>
</tr>
<tr class="odd">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[MemberwiseClone](http://msdn.microsoft.com/en-us/library/57ctke0a)</td>
<td><div class="summary">
Creates a shallow copy of the current [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).
</div>
(Inherited from [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).)</td>
</tr>
<tr class="even">
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[ToString](http://msdn.microsoft.com/en-us/library/7bxwbwt2)</td>
<td><div class="summary">
Returns a string that represents the current object.
</div>
(Inherited from [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).)</td>
</tr>
</tbody>
</table>

## See Also
[MefModuleInitializer Class](/patterns-practices/reference/mefmoduleinitializer-class-mspp-mefextensions-modularity)

[Microsoft.Practices.Prism.MefExtensions.Modularity Namespace](/patterns-practices/reference/mspp-mefextensions-modularity-namespace)
