---
TOCTitle: MefItemsControlRegionAdapter Methods
Title: 'MefItemsControlRegionAdapter Methods (Microsoft.Practices.Prism.MefExtensions.Regions)'
ms:assetid: 'Methods.T:Microsoft.Practices.Prism.MefExtensions.Regions.MefItemsControlRegionAdapter'
ms:mtpsurl: 'mefitemscontrolregionadapter-methods-mspp-mefextensions-regions.md'
---

# MefItemsControlRegionAdapter Methods

The [MefItemsControlRegionAdapter](https://msdn.microsoft.com/library/microsoft.practices.prism.mefextensions.regions.mefitemscontrolregionadapter) type exposes the following members.

## Methods


<table>

<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[Adapt](/patterns-practices/reference/itemscontrolregionadapter-adapt-method-mspp-regions)</td>
<td><div class="summary">
Adapts an [ItemsControl](http://msdn.microsoft.com/en-us/library/ms611045) to an [IRegion](/patterns-practices/reference/iregion-interface-mspp-regions).
</div>
(Inherited from [ItemsControlRegionAdapter](/patterns-practices/reference/itemscontrolregionadapter-class-mspp-regions).)</td>
</tr>
<tr class="even">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[AttachBehaviors](/patterns-practices/reference/regionadapterbase-t-attachbehaviors-method-mspp-regions)</td>
<td><div class="summary">
Template method to attach new behaviors.
</div>
(Inherited from [RegionAdapterBase&lt;T&gt;](/patterns-practices/reference/regionadapterbase-t-class-mspp-regions).)</td>
</tr>
<tr class="odd">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[AttachDefaultBehaviors](/patterns-practices/reference/regionadapterbase-attachdefaultbehaviors-t-method-mspp-regions)</td>
<td><div class="summary">
This method adds the default behaviors by using the [IRegionBehaviorFactory](/patterns-practices/reference/iregionbehaviorfactory-interface-mspp-regions) object.
</div>
(Inherited from [RegionAdapterBase&lt;T&gt;](/patterns-practices/reference/regionadapterbase-t-class-mspp-regions).)</td>
</tr>
<tr class="even">
<td>![Protected method](/patterns-practices/reference/images/protmethod.gif)</td>
<td>[CreateRegion](/patterns-practices/reference/itemscontrolregionadapter-createregion-method-mspp-regions)</td>
<td><div class="summary">
Creates a new instance of [AllActiveRegion](/patterns-practices/reference/allactiveregion-class-mspp-regions).
</div>
(Inherited from [ItemsControlRegionAdapter](/patterns-practices/reference/itemscontrolregionadapter-class-mspp-regions).)</td>
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
<td>[Initialize](/patterns-practices/reference/regionadapterbase-t-initialize-method-mspp-regions)</td>
<td><div class="summary">
Adapts an object and binds it to a new [IRegion](/patterns-practices/reference/iregion-interface-mspp-regions).
</div>
(Inherited from [RegionAdapterBase&lt;T&gt;](/patterns-practices/reference/regionadapterbase-class-mspp-regions).)</td>
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
<td>![Public method](/patterns-practices/reference/images/public-method.gif)</td>
<td>[ToString](http://msdn.microsoft.com/en-us/library/7bxwbwt2)</td>
<td><div class="summary">
Returns a string that represents the current object.
</div>
(Inherited from [Object](http://msdn.microsoft.com/en-us/library/e5kfa45b).)</td>
</tr>
</tbody>
</table>

## Explicit Interface Implementations

<table>
<tr class="header">
<th> </th>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>![Explicit interface implemetation](/patterns-practices/reference/images/public-interface.gif)![Private Method](/patterns-practices/reference/images/clear.gif)</td>
<td>[IRegionAdapter.Initialize](https://msdn.microsoft.com/en-us/library/gg418937(v=pandp.38))</td>
<td><div class="summary">
Adapts an object and binds it to a new [IRegion](/patterns-practices/reference/iregion-interface-mspp-regions).
</div>
(Inherited from [RegionAdapterBase&lt;T&gt;](https://msdn.microsoft.com/en-us/library/gg431546(v=pandp.38)).)</td>
</tr>
</tbody>
</table>

## See Also

[MefItemsControlRegionAdapter Class](/patterns-practices/reference/mefitemscontrolregionadapter-class-mspp-mefextensions-regions)<br/>
[Microsoft.Practices.Prism.MefExtensions.Regions Namespace](/patterns-practices/reference/mspp-mefextensions-regions-namespace)<br/>
