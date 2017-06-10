---
TOCTitle: MefModuleManager Methods
Title: 'MefModuleManager Methods (Microsoft.Practices.Prism.MefExtensions.Modularity)'
ms:assetid: 'Methods.T:Microsoft.Practices.Prism.MefExtensions.Modularity.MefModuleManager'
ms:mtpsurl: 'mefmodulemanager-methods-mspp-mefextensions-modularity.md'
---

# MefModuleManager Methods

The [MefModuleManager](/patterns-practices/reference/mefmodulemanager-class-mspp-mefextensions-modularity) type exposes the following members.

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
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[Dispose()()()](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager.dispose)</td>
<td><div class="summary">
Performs application-defined tasks associated with freeing, releasing, or resetting unmanaged resources.
</div>
(Inherited from [ModuleManager](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager).)</td>
</tr>
<tr class="even">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[Dispose(Boolean)](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager.dispose(system.boolean))</td>
<td><div class="summary">
Disposes the associated [IModuleTypeLoader](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.imoduletypeloader)s.
</div>
(Inherited from [ModuleManager](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager).)</td>
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
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[HandleModuleTypeLoadingError](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager.handlemoduletypeloadingerror(microsoft.practices.prism.modularity.moduleinfo%2csystem.exception))</td>
<td><div class="summary">
Handles any exception occurred in the module typeloading process, logs the error using the [ILoggerFacade](https://msdn.microsoft.com/library/microsoft.practices.prism.logging.iloggerfacade) and throws a [ModuleTypeLoadingException](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.moduletypeloadingexception). This method can be overridden to provide a different behavior.
</div>
(Inherited from [ModuleManager](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager).)</td>
</tr>
<tr class="even">
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[LoadModule](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager.loadmodule(system.string))</td>
<td><div class="summary">
Loads and initializes the module on the [ModuleCatalog](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager.modulecatalog) with the name moduleName.
</div>
(Inherited from [ModuleManager](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager).)</td>
</tr>
<tr class="odd">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[LoadModulesThatAreReadyForLoad](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager.loadmodulesthatarereadyforload)</td>
<td><div class="summary">
Loads the modules that are not intialized and have their dependencies loaded.
</div>
(Inherited from [ModuleManager](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager).)</td>
</tr>
<tr class="even">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[MemberwiseClone](http://msdn.microsoft.com/en-us/library/57ctke0a)</td>
<td><div class="summary">
Creates a shallow copy of the current [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).
</div>
(Inherited from [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).)</td>
</tr>
<tr class="odd">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[ModuleNeedsRetrieval](https://msdn.microsoft.com/library/microsoft.practices.prism.mefextensions.modularity.mefmodulemanager.moduleneedsretrieval(microsoft.practices.prism.modularity.moduleinfo))</td>
<td><div class="summary">
Checks if the module needs to be retrieved before it's initialized.
</div>
(Overrides [ModuleManager..::.ModuleNeedsRetrieval(ModuleInfo)](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager.moduleneedsretrieval(microsoft.practices.prism.modularity.moduleinfo)).)</td>
</tr>
<tr class="even">
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[OnImportsSatisfied](https://msdn.microsoft.com/library/microsoft.practices.prism.mefextensions.modularity.mefmodulemanager.onimportssatisfied)</td>
<td><div class="summary">
Called when a part's imports have been satisfied and it is safe to use.
</div></td>
</tr>
<tr class="odd">
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[Run](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager.run)</td>
<td><div class="summary">
Initializes the modules marked as [WhenAvailable](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.initializationmode) on the [ModuleCatalog](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager.modulecatalog).
</div>
(Inherited from [ModuleManager](https://msdn.microsoft.com/library/microsoft.practices.prism.modularity.modulemanager).)</td>
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
[MefModuleManager Class](/patterns-practices/reference/mefmodulemanager-class-mspp-mefextensions-modularity)

[Microsoft.Practices.Prism.MefExtensions.Modularity Namespace](/patterns-practices/reference/mspp-mefextensions-modularity-namespace)
