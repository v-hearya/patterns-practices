---
TOCTitle: MVVM Reference Implementation
Title: MVVM Reference Implementation
ms:assetid: 'e45042f5-e710-4a6b-843e-9b65cb6bde19'
ms:mtpsurl: 'https://msdn.microsoft.com/en-us/library/Gg405492(v=PandP.40)'
---

# MVVM Reference Implementation


The Model-View-ViewModel Reference Implementation (MVVM RI) demonstrates how to build an application that implements the MVVM presentation pattern and shows how to address some advanced challenges that you might face when using this pattern.

You should first review the "Basic MVVM QuickStart" and the "MVVM QuickStart" topics in the [Prism4.pdf](http://compositewpf.codeplex.com/releases/view/55580) before using this reference implementation because many concepts and challenges explained in them are not repeated in this topic.

## Business Scenario

The MVVM RI represents a survey application. In the main window, a list of available questionnaires is displayed, when the **Take Survey** button is clicked for a particular questionnaire, an empty survey with different types of questions is shown; after the questionnaire is completed, it can be submitted. After that, the list of available questionnaires is displayed to the user.

The following illustration shows the reference implementation main window.

![](https://msdn.microsoft.com/en-us/Gg405492.8BA9C0D3658DC25EEDECBB80481CB6C0(en-us,PandP.40).png "MVVM RI user interface")

MVVM RI user interface

## Building and Running the Reference Implementation

This reference implementation requires Visual Studio 2010, [Microsoft Silverlight 4](http://www.microsoft.com/silverlight/) and [Microsoft Silverlight 4 Tools for Visual Studio 2010](http://www.microsoft.com/downloads/en/details.aspx?familyid=b3deb194-ca86-4fb6-a716-b67c2604a139&displaylang=en) to run.

**To build and run the MVVM RI**

1. In Visual Studio, open the solution file MVVM RI\\MVVM.sln.
2. Verify that the MVVM.Web project is set as the startup project.
3. On the **Build** menu, click **Rebuild Solution**.
4. Press F5.

## Walkthrough

To explore the scenario, perform the following steps to build and run the QuickStart:

1. The main window is composed of a view that shows a list of the different questionnaires that can be taken. Click the **Take Survey** button of the Food questionnaire item to display it.

  > [!NOTE]
> Notice that in the user interface of the reference implementation there are information icons; you can click them to display/hide information and implementation notes about the different pieces of the reference implementation.

  ![](https://msdn.microsoft.com/en-us/Gg405492.42FE42CF511A163DF296BD4DE31D7621(en-us,PandP.40).png "Reference implementation main window")

  Reference implementation main window

2. The Food Questionnaire will be displayed. Complete the **Name** and **Age** fields, and then complete the questions of the questionnaire. Notice that when you complete open questions, the remaining chars count decreases. Also, note that the number of remaining questions, located at the lower-left of the screen, decreases with each completed question.
3. Complete the first question with some letters. A validation error will be displayed, because this question type is numeric. If there are validation errors shown as you complete the questionnaire, you need to fix those before you click **Submit**.

  ![](https://msdn.microsoft.com/en-us/Gg405492.65E2C8F1071FD527304FCEE1328034BD(en-us,PandP.40).png "Validation errors being displayed")

  Validation errors being displayed

  > [!NOTE]
> Note that if you choose more than two answers for the multiple-selection question, a validation error displays.

4. Click **Cancel**. A confirmation dialog box appears. Click **Cancel** to return to the questionnaire.

  ![](https://msdn.microsoft.com/en-us/Gg405492.A1658212F2EDC262770FF89F6CD14F9E(en-us,PandP.40).png "Confirmation dialog box")

  Confirmation dialog box

5. After the questionnaire is completed without validation errors, the **Submit** button is enabled. Select the **Force failure** check box, located next to the **Submit** button, and then click **Submit**. The questionnaire will be submitted, but it will fail and an error dialog box will be displayed.

  ![](https://msdn.microsoft.com/en-us/Gg405492.53C204652A196F09E48ACD00C3C13D3A(en-us,PandP.40).png "Error dialog box")

  Error dialog box

6. Clear the **Force failure** check box, and then click **Submit**. An animation that simulates the processing of the submitted questionnaire is triggered; after that, the questionnaire list page displays again.

  ![](https://msdn.microsoft.com/en-us/Gg405492.D1B2E9EA0B909667894882D9214BA1EF(en-us,PandP.40).png "A questionnaire being submitted")

  A questionnaire being submitted

## Solution Overview

The MVVM RI solution includes the following projects:

-  **MVVM.Client**. This project contains the code that will run on the client side (the browser). It contains the views, view models, the repository and infrastructure classes. The repository is an abstraction layer for interacting with the questionnaire service. And the infrastructure folder contains the behaviors, the classes that support state management, the view model base class, interaction classes, among other things.
-  **MVVM.Client.Tests**. This project contains the unit tests for the Client project.
-  **MVVM.Questionnaires**. This project contains the domain model for the application, including entities, services, and service interfaces. The framework folder contains the base class for model objects and provides support for the **INotifyDataErrorInfo** and **INotifyPropertyChanged** interfaces.
-  **MVVM.Questionnaires.Tests**. This project contains the unit tests for the Client project.
-  **MVVM.TestSupport**. This project contains helper methods for running the unit tests.
-  **MVVM.Web**. This is the Web project that hosts the Silverlight application.

The following illustration shows the solution structure of the MVVM RI.

![](https://msdn.microsoft.com/en-us/Gg405492.24B59BE16F0196995C5E7DE53552C365(en-us,PandP.40).png "MVVM RI solution structure")

MVVM RI solution structure

## Implementation Details

The reference implementation highlights the key elements, considerations, and challenges when implementing the MVVM pattern in a complex application. For more information about implementing the MVVM pattern, see "Implementing the MVVM Pattern," in the [Prism4.pdf](http://compositewpf.codeplex.com/releases/view/55580).

This section describes the key artifacts of the reference implementation, which are shown in the following illustration. Most concepts of the MVVM RI are shared with the MVVM QuickStart. For more information, see [MVVM QuickStart](https://msdn.microsoft.com/en-us/library/gg430869(v=pandp.40)).

![](https://msdn.microsoft.com/en-us/Gg405492.C1C498204EFDB6E753EC8164CD18F023(en-us,PandP.40).png "MVVM RI conceptual view")

MVVM RI conceptual view

## How to Instantiate the View Models in the View's DataContext Using MEF

In this reference implementation, both the views and the view models are created with Managed Extensibility Framework (MEF). MEF is asked for the view by using a **ViewFactory** class (this is to avoid composing the container in itself); as a result, the view model for the view gets created. To wire up the model to the view model, the state support described in the [State Management](https://msdn.microsoft.com/en-us/library/Gg405492(v=PandP.40)#State_Management) section is used.

View models are set to the view's **DataContext** in the view's code behind file. Views have the **ViewModel** property with the **Import** attribute applied to be imported by MEF. Because the **PartCreationPolicy(CreationPolicy.NonShared)** attribute is applied to view model classes, whenever a view model is imported by MEF, a new instance of the corresponding view model class is created. The following code shows the **AvailableQuestionnaireTemplatesListViewModel** class that is exported using the aforementioned creation policy.

```C#
  [Export][PartCreationPolicy(CreationPolicy.NonShared)]
  public class AvailableQuestionnaireTemplatesListViewModel : ViewModel
  {
    private readonly ISingleViewUIService uiService;
    private readonly IQuestionnaireRepository questionnaireRepository;

    public AvailableQuestionnaireTemplatesListViewModel()
    {
      this.QuestionnaireTemplates = new ObservableCollection<QuestionnaireTemplate>();
    }

    [ImportingConstructor]
    public AvailableQuestionnaireTemplatesListViewModel(IQuestionnaireRepository questionnaireRepository, ISingleViewUIService uiService)
    {
      ...
    }
    ...
  }
```

The following code shows declaratively how the view model property on the view should be composed.

```C#
  [Export(ViewNames.QuestionnaireTemplatesList, typeof(UserControl))]
  [PartCreationPolicy(CreationPolicy.NonShared)]
  public partial class AvailableQuestionnaireTemplatesListView : UserControl
  {
    public AvailableQuestionnaireTemplatesListView()
    {
      InitializeComponent();
    }

    [Import]
    public AvailableQuestionnaireTemplatesListViewModel ViewModel
    {
      set { this.DataContext = value; }
    }
  }
```

The preceding is a very simple approach for wiring up views and view models using MEF; there are other mechanisms that are discussed in "Implementing the MVVM Pattern," in the [Prism4.pdf](http://compositewpf.codeplex.com/releases/view/55580) and could involve MEF (for example, the view is created using MEF, but the view model is retrieved from a view model locator).

## Master-Details

The reference implementation shows a simple Master-Detail scenario. On the main page of the application, the questionnaire list is shown. That view also contains the **QuestionnaireSummary** details view, which displays information about the selected questionnaire.

The following code shows how the **AvailableQuestionnaireTemplatesListViewModel** view model contains a property of **QuestionnaireTemplateSummaryViewModel** type. This property is needed because the details for the selected questionnaire are retrieved from a service; therefore, a separate view model is required to manage this operation.

```C#
  public class AvailableQuestionnaireTemplatesListViewModel : ViewModel
  {
    private readonly ISingleViewUIService uiService;
    private readonly IQuestionnaireRepository questionnaireRepository;

    public AvailableQuestionnaireTemplatesListViewModel()
    {
      this.QuestionnaireTemplates = new ObservableCollection<QuestionnaireTemplate>();
    }

    public ObservableCollection<QuestionnaireTemplate> QuestionnaireTemplates { get; private set; }

    public ICommand TakeSurveyCommand { get; private set; }

    public QuestionnaireTemplateSummaryViewModel QuestionnaireTemplateSummary { get; private set; }

    private void TakeSurvey(QuestionnaireTemplate questionnaireTemplate)
    {

    ...

  }
```

Whenever a questionnaire of the questionnaire list is selected, the summary view model obtains the questionnaire summary and shows it. The following XAML code shows how the selected template is set on the summary view model and reacts to changes from it.

```XAML
  <UserControl x:Class="MVVM.Client.Views.AvailableQuestionnaireTemplatesListView"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:i="http://schemas.microsoft.com/expression/2010/interactivity" 
    xmlns:ei="http://schemas.microsoft.com/expression/2010/interactions"
    xmlns:vm="clr-namespace:MVVM.Client.ViewModels"
    xmlns:model="clr-namespace:MVVM.Questionnaires.Model;assembly=MVVM.Questionnaires"
    xmlns:views="clr-namespace:MVVM.Client.Views"
    mc:Ignorable="d"
    d:DesignHeight="300" d:DesignWidth="400">

    <Border BorderBrush="{StaticResource PrimaryBrush}" BorderThickness="2" Margin="2,2,2,10">
      <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
          <RowDefinition Height="*"/>
          <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>

        <ListBox x:Name="QuestionnaireTemplates" HorizontalAlignment="Stretch" VerticalAlignment="Stretch"
             ItemsSource="{Binding QuestionnaireTemplates}"
             SelectedItem="{Binding QuestionnaireTemplateSummary.CurrentlySelectedQuestionnaireTemplate, Mode=TwoWay}"
             Grid.Row="0">
          ...
        </ListBox>

        <views:QuestionnaireTemplateSummaryView DataContext="{Binding QuestionnaireTemplateSummary}" Grid.Row="1"/>
      </Grid>
    </Border>
  </UserControl>
```

The **QuestionnaireTemplateSummaryViewModel** retrieves the corresponding summary each time a questionnaire is selected; this is because the **CurrentlySelectedQuestionnaireTemplate** property is set by the binding for the **SelectedItem** property on the template's list box.

## Services

The following services are used in the MVVM RI:

-  **QuestionnaireService**. This service implements the [IAsyncResult](http://msdn.microsoft.com/en-us/library/ms228963.aspx) design pattern. It is used to retrieve the different questionnaires data and its summary data asynchronously. However, in the reference implementation, the view model accesses the **QuestionnaireService** service through a repository layer.
-  **SingleViewUIService**. This service is a simple user interface (UI) service that maps a view name to a view implementation and shows it as the current view. This service is used by view models to indicate which view should be shown without dealing with the actual views, while observing the constraints of the MVVM pattern. For example, this service allows the main view to show the different views of the application. The following code from the **AvailableQuestionnaireTemplatesListViewModel** class demonstrates its usage.

```C#
    private void TakeSurvey(QuestionnaireTemplate questionnaireTemplate)
    {
      this.uiService.ShowView(ViewNames.CompleteQuestionnaire, questionnaireTemplate);
    }
```

In the preceding code, when the **Take Survey** button is clicked, the preceding method from the view model is invoked. In this method, the UI service will show the **CompleteQuestionnaire** view, providing the selected template as the context for the view. The **ShowView** method of the service is used for this.

## State Management

In the reference implementation, the actual questionnaire data (questions and options) needs to be passed to the questionnaire view model. Because MEF is being used to import the view models (parts), parameters (such as context) cannot be passed. If you need to pass state for an object that will be created by MEF, you need to set the value for the current state for the type of the context object. The receiving part imports the matching **IState**, which is non-shared and captures the current state when created, to isolate the consumer from any changes to the current value that might occur later.

> [!NOTE]
> The reference implementation has the **StateHandler** class that provides access to state management objects in the container and handles setting state while returning previous values; therefore, the user avoids dealing with the current state directly.

For this reason, the state management classes have been created. These are the **State** and **CurrentState** classes and their corresponding interfaces. The interfaces are shown in the following code.

```C#
  [InheritedExport]
  public interface IState<T>
  {
    /// <summary>
    /// Gets the value for the snapshot.
    /// </summary>
    T Value { get; }
  }
```

```C#
  [InheritedExport]
  public interface ICurrentState<T>
  {
    /// <summary>
    /// Gets and sets the current value.
    /// </summary>
    T Value { get; set; }
  }
```

> [!NOTE]
> The preceding code takes advantage of the **InheritedExport** attribute in the interfaces to avoid explicitly exporting each concrete non-generic state management class.

The following classes are concrete and non-generic implementations of the **State** and **CurrentState** abstract classes. These classes must be defined because classes that inherit from the generic classes exported with MEF do not satisfy imports because it creates closed generic types.

```C#
  [PartCreationPolicy(CreationPolicy.NonShared)]
  public class QuestionnaireTemplateState : State<QuestionnaireTemplate>
  {
  }
```
```C#
  public class QuestionnaireTemplateCurrentState : CurrentState<QuestionnaireTemplate>
  {
  }
```

Notice that the **QuestionnaireTemplateState** class is defined as **NonShared**, whereas the **QuestionnaireTemplateCurrentState** is defaulted to **Shared**. This means that whenever the **QuestionnaireTemplateState** class is imported, a new instance will be created; and when an instance of the **QuestionnaireTemplateCurrentState** class is required, the same singleton instance will be returned. When rendering a questionnaire, this singleton instance (current state) will hold the data (questions and options) to render it correctly.

The following methods of the **SingleViewUIService** service shows how a view is displayed using some context.

```C#
  public void ShowView<T>(string viewName, T context)
  {
    var previousValue = StateHandler.SetState(context);

    try
    {
      this.ShowView(viewName);
    }
    finally
    {
      StateHandler.SetState(previousValue);
    }
  }
```

The overload of the **ShowView** method in the preceding code passes the view name and a context to render the specified view. The previous state is saved and the new context is applied; after that, the view is rendered with the new context, and then the old context is restored.

This is done to solve the challenge of MEF not being able to pass parameters/context when importing a part; the current context is a singleton instance and is updated with context (parameters); when a new instance of the state for a view is imported, the singleton instance (where the new context was stored) is also imported.

## Repository

The reference implementation contains a thin repository layer to simplify the interaction with the Questionnaire service. The **QuestionnaireRepository** class implements the **IQuestionnaireRepository** interface that is shown in the following code.

```C#
  public interface IQuestionnaireRepository
  {
    void GetQuestionnaireTemplatesAsync(Action<IOperationResult<IEnumerable<QuestionnaireTemplate>>> callback);

    void SubmitQuestionnaireAsync(Questionnaire questionnaire, Action<IOperationResult> callback);

    void GetQuestionnaireTemplateSummaryAsync(QuestionnaireTemplate questionnaireTemplate, Action<IOperationResult<QuestionnaireTemplateSummary>> callback);
  }
```

This interface defines the following methods:

-  **GetQuestionnaireTemplatesAsync**. This method gets the data of a questionnaire template.
-  **SubmitQuestionnaireAsync**. This method submits a questionnaire.
-  **GetQuestionnaireTemplateSummaryAsync**. This method gets the summary data for a particular questionnaire.

When creating a new instance of the repository class, an instance of the **QuestionnaireService** is created or injected. Every method passes to the supplied callback an object of **OperationResult** type that represents the outcome of the operation and includes the exceptions that could have occurred on the operation. This type is used, for example, when forcing the failure of the submitting of a questionnaire. This is done in the reference implementation instead of using the standard Async pattern because it offers a simplified programming model: it allows for a continuation-based API, while avoiding the need to invoke two methods (the **Begin** and **End** methods from the IAsyncResult pattern), and provides automatic dispatching to the UI thread.

## Service Calls

In the reference implementation, service calls are implemented asynchronously because Silverlight does not support synchronous service calls.

The **AsyncResult** class of the QuickStart (located in the Infrastructure/Model folder) is an implementation of the **IAsyncResult** interface of the **System** namespace. This class encapsulates the results of an asynchronous operation.

The Questionnaire service provides operations; the processing and returning of the results of an operation are asynchronous. The view model asks the Questionnaire repository, which in turn asks the service to retrieve the questionnaire data, as shown in the following code.

```C#
  public void GetQuestionnaireTemplatesAsync(Action<IOperationResult<IEnumerable<QuestionnaireTemplate>>> callback)
  {
    this.service.BeginGetQuestionnaireTemplates(
      (ar) =>
      {
        OperationResult<IEnumerable<QuestionnaireTemplate>> operationResult = new OperationResult<IEnumerable<QuestionnaireTemplate>>();
        try
        {
          operationResult.Result = service.EndGetQuestionnaireTemplates(ar);
        }
        catch (Exception ex)
        {
          operationResult.Error = ex;
        }

        synchronizationContext.Post(
          (state) =>
          {
            callback(operationResult);
          },
          null);
      },
      null);
  }
```

The preceding code shows a method of the **QuestionnaireRepository** class that calls the service's **BeginGetQuestionnaireTemplates** method, which starts retrieving the questions in a worker thread. When the service completes retrieving the **QuestionnaireTemplate**, the callback provided by the repository (the one that is passed as a parameter to the **BeginGetQuestionnaireTemplates** method) posts actual processing to the UI thread. As shown in the code sample, the callback completes the Async operation using the **EndGetQuestionnaireTemplates** method, storing the operation results and the errors (if occurred) in an **OperationResult** instance.

## Validation

In the reference implementation, the **INotifyDataErrorInfo** interface is implemented in the same way as in the MVVM QuickStart, which implements the interface in a **DomainObject** abstract class. However, to specify the conditions that a property must fulfill to be valid and the validation errors, the reference implementation uses data annotations attributes. Both the standard attributes (such as **Required**, **Range**, and **StringLength**) and the custom validation attribute are used to invoke custom validation methods.

> [!NOTE]
> There are slight differences between the **DomainObject** class of the reference implementation and the one of the QuickStart.

The following code shows the Questionnaire partial class, located in the file MVVM.Questionnaires\\Model\\DomainObjects.cs.

In this file, you can see that each class from the model inherits from the **DomainObject** abstract class, and that the condition that each property must fulfill to be valid is set with data annotations attributes. Finally, note that the validations are triggered in the setter of each property whether or not there are validation rules for it.

> [!NOTE]
> The partial classes located in the DomainObjects.cs file implements the **INotifyPropertyChanged** and the **INotifyDataErrorInfo** interfaces. Ideally, this repetitive code could be generated by a tool.

```C#
  public sealed partial class Questionnaire : DomainObject
  {
    private int? age;

    private string name;

    private ICollection<Question> questions;

    private QuestionnaireTemplate template;

    public Questionnaire()
    {
    }

    [Range(21, 100)]
    public int? Age
    {
      get
      {
        return this.age;
      }

      set
      {
        if (this.age != value)
        {
          this.ValidateProperty("Age", value);
          this.age = value;
          this.RaisePropertyChanged("Age");
        }
      }
    }


    [Required()]
		[StringLength(50)]
    public string Name
    {
      get
      {
        return this.name;
      }

      set
      {
        if (this.name != value)
        {
          this.ValidateProperty("Name", value);
          this.name = value;
          this.RaisePropertyChanged("Name");
        }
      }
    }

    ...

  }
```

In the preceding code, some of the data annotations built in validations are used (they are **Required**, **Range**, and **StringLength**). Additionally, you can have custom validations by defining your own validation attributes or by using the standard **CustomValidation** attribute and configuring it with the name of a static method that performs the validationcan be created for more complex validations. The following code example shows how to apply a custom validation.

```C#
  [CustomValidation(typeof(CommonValidation), "ValidationOpenQuestionResponseLength")]
  [Required()]
  public string Response
  {
    get
    {
      return this.response;
    }

    set
    {
      if (this.response != value)
      {
        this.ValidateProperty("Response", value);
        this.response = value;
        this.RaisePropertyChanged("Response");
      }
    }
  }
```

## Custom Behaviors

The following are custom behaviors specific to this reference implementation (these behaviors are used specifically for displaying pop-up windows):

-  **InteractionRequestTrigger**. This custom **EventTrigger** automatically connects to the appropriate **Raised** event of an object that implements the **IInteractionRequest** interface. This reduces the amount of XAML needed and reduces the chance of entering the event name incorrectly. The following code shows an example of its usage.
```XAML
    <behaviors:InteractionRequestTrigger SourceObject="{Binding CancelConfirmationInteractionRequest}">
    </behaviors:InteractionRequestTrigger>
```

  A trigger action that matches the desired action can be associated to this trigger.

-  **PopupChildWindowAction**. To initiate the interaction, a trigger action that matches the desired interaction mechanism can be associated to the trigger behavior explained earlier. The custom **PopupChildWindowAction** class is used to pop up the child window specified through its properties. The following code shows an example of this.

```XAML
    <behaviors:InteractionRequestTrigger SourceObject="{Binding CancelConfirmationInteractionRequest}">
      <behaviors:PopupChildWindowAction ContentTemplate="{StaticResource ConfirmWindowTemplate}"/>
    </behaviors:InteractionRequestTrigger>
```

For more information about these behaviors, see the section, "Using Behaviors to Implement the Interaction User Experience," in "Advanced MVVM Scenarios" in the [Prism4.pdf](http://compositewpf.codeplex.com/releases/view/55580).

## Unit and Acceptance Tests

The MVVM RI includes unit tests within the solution. Unit tests verify if individual units of source code work as expected.

**To run the MVVM RI unit tests**

1. In Solution Explorer, right-click **MVVM.Test**, and then click **Set as StartUp Project**.
2. Press F5. A browser window will open, and the tests will run after a couple of seconds.

The MVVM RI includes a separate solution that includes acceptance tests. The acceptance tests describe how the application should perform when you follow a series of steps; you can use the acceptance tests to explore the functional behavior of the application in a variety of scenarios.

**To run the MVVM RI acceptance tests**

1. In Visual Studio, open the solution file MVVMRI\\MVVMRI.Tests.AcceptanceTest\\MVVMRI.Tests.AcceptanceTest.sln.
2. Right-click **MVVM.Tests.AcceptanceTest**, and then click **Set as StartUp Project**.
3. Press F5.

### Outcome

You should see the reference implementation window and the tests automatically interact with the application. At the end of the test run, you should see that all tests have passed.

## More Information


To learn more about the MVVM pattern, see the following topics in the [Prism4.pdf](http://compositewpf.codeplex.com/releases/view/55580):

-  Chapter 5, "Implementing the MVVM Pattern"
-  Chapter 6, "Advanced MVVM Scenarios"
-  Basic MVVM QuickStart
-  MVVM QuickStart

