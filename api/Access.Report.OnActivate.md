---
title: Report.OnActivate property (Access)
keywords: vbaac10.chm13765
f1_keywords:
- vbaac10.chm13765
ms.prod: access
api_name:
- Access.Report.OnActivate
ms.assetid: eb7f05e3-edba-ab9e-3708-5c3ee7b2ee18
ms.date: 03/15/2019
ms.localizationpriority: medium
---


# Report.OnActivate property (Access)

Sets or returns the value of the **On Activate** box in the Properties window of a form or report. Read/write **String**.


## Syntax

_expression_.**OnActivate**

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Remarks

This property is helpful for programmatically changing the action that Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered.

The **Activate** event occurs when the form or report receives the focus and becomes the active window.

The **OnActivate** value will be one of the following, depending on the selection chosen in the Choose Builder window (accessed by choosing the **Build** button next to the **On Activate** box in the object's Properties window):

- If you choose Expression Builder, the value will be =_expression_, where _expression_ is the expression from the Expression Builder window.
    
- If you choose Macro Builder, the value is the name of the macro. 
    
- If you choose Code Builder, the value will be [Event Procedure]. 
    
If the **On Activate** box is blank, the property value is an empty string.


## Example

The following example associates the **Activate** event with the macro Activate_Macro for the **Order Entry** form.

```vb
Forms("Order Entry").OnActivate = "Activate_Macro"
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]