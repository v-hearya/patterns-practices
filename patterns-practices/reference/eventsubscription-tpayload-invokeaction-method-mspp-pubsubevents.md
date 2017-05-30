---
TOCTitle: InvokeAction Method
Title: 'EventSubscription(TPayload).InvokeAction Method (Microsoft.Practices.Prism.PubSubEvents)'
ms:assetid: 'M:Microsoft.Practices.Prism.PubSubEvents.EventSubscription\`1.InvokeAction(System.Action{\`0},\`0)'
ms:mtpsurl: 'eventsubscription-tpayload-invokeaction-method-mspp-pubsubevents.md'
---

# EventSubscription&lt;TPayload&gt;.InvokeAction Method

Invokes the specified [Action&lt;T&gt;](http://msdn.microsoft.com/en-us/library/018hxwa8) synchronously when not overridden.

**Namespace:** [Microsoft.Practices.Prism.PubSubEvents](mspp-pubsubevents-namespace.md)

**Assembly:** Microsoft.Practices.Prism.PubSubEvents (in Microsoft.Practices.Prism.PubSubEvents.dll)

**Version:** 1.0.0.0 (1.0.0.0)

## Syntax

```C#
public virtual void InvokeAction(
	Action<TPayload> action,
	TPayload argument
)
```


### Parameters

*action*  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Type: [System.Action](http://msdn.microsoft.com/en-us/library/018hxwa8)&lt;[TPayload](eventsubscription-tpayload-class-mspp-pubsubevents.md)&gt;

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The action to execute.

*argument*  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Type: [TPayload](eventsubscription-tpayload-class-mspp-pubsubevents.md)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The payload to pass action while invoking it.

## Exceptions

| Exception                                                                             | Condition                                                                                                  |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [System.ArgumentNullException](http://msdn.microsoft.com/en-us/library/27426hcy) | An [ArgumentNullException](http://msdn.microsoft.com/en-us/library/27426hcy) is thrown if action is null. |

## See Also

[EventSubscription&lt;TPayload&gt; Class](eventsubscription-tpayload-class-mspp-pubsubevents.md)

EventSubscription&lt;TPayload&gt; 

[Microsoft.Practices.Prism.PubSubEvents Namespace](mspp-pubsubevents-namespace.md)

# EventSubscription(Of TPayload).InvokeAction Method 

Invokes the specified [Action(Of T)](http://msdn.microsoft.com/en-us/library/018hxwa8) synchronously when not overridden.

**Namespace:** [Microsoft.Practices.Prism.PubSubEvents](mspp-pubsubevents-namespace.md)

**Assembly:** Microsoft.Practices.Prism.PubSubEvents (in Microsoft.Practices.Prism.PubSubEvents.dll) Version: 1.0.0.0 (1.0.0.0)

## Syntax

```VB
'Declaration
Public Overridable Sub InvokeAction ( 
	action As Action(Of TPayload),
	argument As TPayload
)
```


### Parameters

*action*  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Type: [System.Action](http://msdn.microsoft.com/en-us/library/018hxwa8)(Of [TPayload](eventsubscription-tpayload-class-mspp-pubsubevents.md))

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The action to execute.

*argument*  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Type: [TPayload](eventsubscription-tpayload-class-mspp-pubsubevents.md)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The payload to pass action while invoking it.

## Exceptions

| Exception                                                                             | Condition                                                                                                  |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [System.ArgumentNullException](http://msdn.microsoft.com/en-us/library/27426hcy) | An [ArgumentNullException](http://msdn.microsoft.com/en-us/library/27426hcy) is thrown if action is null. |

## See Also

[EventSubscription(Of TPayload) Class](eventsubscription-tpayload-class-mspp-pubsubevents.md)

EventSubscription(Of TPayload) Members

[Microsoft.Practices.Prism.PubSubEvents Namespace](mspp-pubsubevents-namespace.md)
