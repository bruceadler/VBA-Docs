---
title: SharedWorkspaceTask object (Office)
keywords: vbaof11.chm264000
f1_keywords:
- vbaof11.chm264000
ms.prod: office
api_name:
- Office.SharedWorkspaceTask
ms.assetid: fbd82b03-53fa-12ff-9fb2-07bef012dde8
ms.date: 01/24/2019
ms.localizationpriority: medium
---


# SharedWorkspaceTask object (Office)

The **SharedWorkspaceTask** object represents a task in a shared document workspace. Member of the **SharedWorkspaceTasks** collection.

> [!NOTE] 
> Beginning with Microsoft Office 2010, this object or member has been deprecated and should not be used.


## Remarks

Use the **SharedWorkspaceTask** object to manage tasks assigned to the members who are collaborating on the documents in the shared workspace.

Use the **Item** (_index_) property of the **SharedWorkspaceTasks** collection to return a specific **SharedWorkspaceTask** object.

Use the **Title** property to set the text of the task that appears on the **Tasks** tab of the **Shared Workspace** task pane and on the shared workspace webpage. Use the **Description** property to supply additional information about the task.

Assign the task to a member of the workspace by using the **AssignedTo** property and the member's domain user name. Specify a due date for the task by using the **DueDate** property.

Use the enumerations for task **Priority** and **Status** to indicate the relative importance of the task and to update the task's status.

Use the **Save** method to upload changes to the server after you modify properties of the **SharedWorkspaceTask** object.

Use the **CreatedBy**, **CreatedDate**, **ModifiedBy**, and **ModifiedDate** properties to return information about the history of each task.


## Example

The following example returns the number of tasks in the shared workspace and information about each task.


```vb
    Dim swsTask As Office.SharedWorkspaceTask 
    Dim strTaskInfo As String 
    strTaskInfo = "The shared workspace contains " & _ 
    ActiveWorkbook.SharedWorkspace.Tasks.Count & " Task(s)." & vbCrLf 
    For Each swsTask In ActiveWorkbook.SharedWorkspace.Tasks 
        strTaskInfo = strTaskInfo & swsTask.Title & vbCrLf & _ 
            " - Description: " & swsTask.Description & vbCrLf & _ 
            " - Assigned to: " & swsTask.AssignedTo & vbCrLf & _ 
            " - Due date: " & swsTask.DueDate & vbCrLf & _ 
            " - Priority: " & swsTask.Priority & vbCrLf & _ 
            " - Status: " & swsTask.Status & vbCrLf 
    Next 
    MsgBox strTaskInfo, vbInformation + vbOKOnly, _ 
        "Tasks in Shared Workspace" 
    Set swsTask = Nothing 

```


## See also

- [SharedWorkspaceTask object members](overview/Library-Reference/sharedworkspacetask-members-office.md)
- [Object Model Reference](overview/Library-Reference/reference-object-library-reference-for-office.md)


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]