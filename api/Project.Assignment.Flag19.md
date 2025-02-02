---
title: Assignment.Flag19 property (Project)
ms.prod: project-server
api_name:
- Project.Assignment.Flag19
ms.assetid: aaa6e052-743c-ca3d-78c9-2a1ae6881e01
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Assignment.Flag19 property (Project)

 **True** if the flag associated with an **Assignment** is set. Read/write **Variant**.


## Syntax

_expression_. `Flag19`

_expression_ A variable that represents an [Assignment](./Project.Assignment.md) object.


## Example

The following example deletes all the tasks that have the **Flag1** set to **True**.


```vb
Sub DeleteNonEssentialTasks() 
 
 Dim T As Task ' Task object used in For Each loop 
 
 ' Delete nonessential tasks in the active project. 
 For Each T In ActiveProject.Tasks 
 If Not (T Is Nothing) Then 
 If T.Flag1 = True Then T.Delete 
 End If 
 Next T 
 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]