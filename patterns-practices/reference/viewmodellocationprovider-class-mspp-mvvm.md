---
TOCTitle: ViewModelLocationProvider Class
Title: 'ViewModelLocationProvider Class (Microsoft.Practices.Prism.Mvvm)'
ms:assetid: 'T:Microsoft.Practices.Prism.Mvvm.ViewModelLocationProvider'
ms:mtpsurl: 'viewmodellocationprovider-class-mspp-mvvm.md'
---

# ViewModelLocationProvider Class

The ViewModelLocationProvider class locates the view model for the view that has the AutoWireViewModelChanged attached property set to true. The view model will be located and injected into the view's DataContext. To locate the view, two strategies are used: First the ViewModelLocationProvider will look to see if there is a view model factory registered for that view, if not it will try to infer the view model using a convention based approach. This class also provide methods for registering the view model factories, and also to override the default view model factory and the default view type to view model type resolver. 

**Namespace:** [Microsoft.Practices.Prism.Mvvm](mspp-mvvm-namespace.md)

**Assembly:** Microsoft.Practices.Prism.Mvvm (in Microsoft.Practices.Prism.Mvvm.dll) Version: 1.0.0.0 (1.0.0.0)

## Syntax

```C#
public static class ViewModelLocationProvider
```

```VB
'Declaration
Public NotInheritable Class ViewModelLocationProvider
```

## Inheritance Hierarchy

[System.Object](http://msdn.microsoft.com/en-us/library/e5kfa45b)

  Microsoft.Practices.Prism.Mvvm.ViewModelLocationProvider

## See Also
[ViewModelLocationProvider Members](viewmodellocationprovider-members-mspp-mvvm.md)