---
title: CodeProject.UpdateDependencyInfo method (Access)
keywords: vbaac10.chm12727
f1_keywords:
- vbaac10.chm12727
ms.prod: access
api_name:
- Access.CodeProject.UpdateDependencyInfo
ms.assetid: 52530a57-6246-d204-b317-0673f762f138
ms.date: 02/27/2019
ms.localizationpriority: medium
---


# CodeProject.UpdateDependencyInfo method (Access)

Updates the dependency information for the database.


## Syntax

_expression_.**UpdateDependencyInfo**

_expression_ A variable that represents a **[CodeProject](Access.CodeProject.md)** object.


## Return value

Nothing


## Remarks

The **UpdateDependencyInfo** method opens, saves, and then closes every table, query, form, and report in the database; no messages are presented to the user.

This method will return a run-time error if any of the following conditions are true:

- This method is being called from an Access project (.adp).
    
- Any database objects are open.
    



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]