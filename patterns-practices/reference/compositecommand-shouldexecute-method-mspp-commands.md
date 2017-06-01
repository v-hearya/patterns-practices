---
TOCTitle: ShouldExecute Method
Title: 'CompositeCommand.ShouldExecute Method (Microsoft.Practices.Prism.Commands)'
ms:assetid: 'M:Microsoft.Practices.Prism.Commands.CompositeCommand.ShouldExecute(System.Windows.Input.ICommand)'
ms:mtpsurl: 'compositecommand-shouldexecute-method-mspp-commands.md'
---

# CompositeCommand.ShouldExecute Method

Evaluates if a command should execute.

**Namespace:** [Microsoft.Practices.Prism.Commands](https://msdn.microsoft.com/library/microsoft.practices.prism.commands)

**Assembly:** Microsoft.Practices.Prism.Mvvm (in Microsoft.Practices.Prism.Mvvm.dll) 

**Version:** 1.0.0.0 (1.0.0.0)

## Syntax

```C#
protected virtual bool ShouldExecute(
	ICommand command
)
```

```VB
'Declaration
Protected Overridable Function ShouldExecute ( 
	command As ICommand
) As 
```

### Parameters

*command*<br/> 
Type: [System.Windows.Input.ICommand](http://msdn.microsoft.com/en-us/library/ms616869)
The command to evaluate.

### Return Value

Type: [Boolean](http://msdn.microsoft.com/en-us/library/a28wyd50)<br/>
A [Boolean](http://msdn.microsoft.com/en-us/library/a28wyd50) value indicating whether the command should be used when evaluating [CanExecute(Object)](https://msdn.microsoft.com/library/microsoft.practices.prism.commands.compositecommand.canexecute(system.object)) and [Execute(Object)](https://msdn.microsoft.com/library/microsoft.practices.prism.commands.compositecommand.execute(system.object)).

## Remarks

 If this command is set to monitor command activity, and command implements the [!:IActiveAwareCommand] interface, this method will return **falsefalse** (**False** in Visual Basic) if the command's [!:IActiveAwareCommand.IsActive] property is **falsefalse** (**False** in Visual Basic); otherwise it always returns **truetrue** (**True** in Visual Basic).

## See Also

[CompositeCommand Class](https://msdn.microsoft.com/library/microsoft.practices.prism.commands.compositecommand)

[CompositeCommand Members](https://msdn.microsoft.com/en-us/library/microsoft.practices.prism.commands.compositecommand_members(v=pandp.50))

[Microsoft.Practices.Prism.Commands Namespace](https://msdn.microsoft.com/library/microsoft.practices.prism.commands)
