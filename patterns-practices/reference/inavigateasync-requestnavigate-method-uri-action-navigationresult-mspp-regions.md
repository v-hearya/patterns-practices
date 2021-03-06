---
TOCTitle: 'RequestNavigate Method (Uri, Action(NavigationResult))'
Title: 'INavigateAsync.RequestNavigate Method (Uri, Action(NavigationResult)) (Microsoft.Practices.Prism.Regions)'
ms:assetid: 'M:Microsoft.Practices.Prism.Regions.INavigateAsync.RequestNavigate(System.Uri,System.Action{Microsoft.Practices.Prism.Regions.NavigationResult})'
ms:mtpsurl: 'inavigateasync-requestnavigate-method-mspp-regions.md'
---

# INavigateAsync.RequestNavigate Method (Uri, Action&lt;NavigationResult&gt;)

Initiates navigation to the target specified by the [Uri](http://msdn.microsoft.com/en-us/library/txt7706a).

**Namespace:** [Microsoft.Practices.Prism.Regions](/patterns-practices/reference/mspp-regions-namespace)  
**Assembly:** Microsoft.Practices.Prism.Composition (in Microsoft.Practices.Prism.Composition.dll)  
**Version:** 5.0.0.0 (5.0.0.0)

## Syntax

```C#
void RequestNavigate(
	Uri target,
	Action<NavigationResult> navigationCallback
)
```

### Parameters

*target*  
Type: [System.Uri](http://msdn.microsoft.com/en-us/library/txt7706a)  
The navigation target

*navigationCallback*  
Type: [System.Action](http://msdn.microsoft.com/en-us/library/018hxwa8)&lt;[NavigationResult](/patterns-practices/reference/navigationresult-class-mspp-regions)&gt;  
The callback executed when the navigation request is completed.



# INavigateAsync.RequestNavigate Method (Uri, Action(Of NavigationResult))

Initiates navigation to the target specified by the [Uri](http://msdn.microsoft.com/en-us/library/txt7706a).

**Namespace:** [Microsoft.Practices.Prism.Regions](/patterns-practices/reference/mspp-regions-namespace)  
**Assembly:** Microsoft.Practices.Prism.Composition (in Microsoft.Practices.Prism.Composition.dll)  
**Version:** 5.0.0.0 (5.0.0.0)

## Syntax

```VB
'Declaration
Sub RequestNavigate ( 
	target As Uri,
	navigationCallback As Action(Of NavigationResult)
)
```

### Parameters

*target*  
Type: [System.Uri](http://msdn.microsoft.com/en-us/library/txt7706a)  
The navigation target

*navigationCallback*  
Type: [System.Action](http://msdn.microsoft.com/en-us/library/018hxwa8)(Of [NavigationResult](/patterns-practices/reference/navigationresult-class-mspp-regions))  
The callback executed when the navigation request is completed.

## Remarks

 Convenience overloads for this method can be found as extension methods on the [NavigationAsyncExtensions](/patterns-practices/reference/navigationasyncextensions-class-mspp-regions) class.

## See Also

[INavigateAsync Interface](/patterns-practices/reference/inavigateasync-interface-mspp-regions)  
[INavigateAsync Members](/patterns-practices/reference/inavigateasync-members-mspp-regions)  
[RequestNavigate Overload](/patterns-practices/reference/inavigateasync-requestnavigate-method-mspp-regions)  
[Microsoft.Practices.Prism.Regions Namespace](/patterns-practices/reference/mspp-regions-namespace)  