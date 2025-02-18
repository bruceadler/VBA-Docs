---
title: ValidationRuleSets.Stat property (Visio)
keywords: vis_sdr.chm18114420
f1_keywords:
- vis_sdr.chm18114420
ms.prod: visio
api_name:
- Visio.ValidationRuleSets.Stat
ms.assetid: 16bbcc14-a537-622f-438a-3707f956e31c
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# ValidationRuleSets.Stat property (Visio)

Returns status information for an object. Read-only.


## Syntax

_expression_.**Stat**

_expression_ A variable that represents a **[ValidationRuleSets](Visio.ValidationRuleSets.md)** object.


## Return value

**[VisStatCodes](Visio.visstatcodes.md)**


## Remarks

If an object is a reference to an entity in a document, and if that document closes, the **Stat** property returns a value in which the **visStatClosed** bit is set.

If an object is a reference to an entity that has been deleted, the **Stat** property returns a value in which the **visStatDeleted** bit is set.

A Component Object Model (COM) object, such as a Microsoft Visio **[Document](Visio.Document.md)** object, lives as long as it is held (pointed to) by a client, even if the object is logically in a deleted or closed state.


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]