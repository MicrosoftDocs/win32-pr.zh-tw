---
title: '顯示工作名稱和狀態 (腳本) '
description: 此腳本範例示範如何列舉工作資料夾中的工作，並顯示每項工作的屬性值。
ms.assetid: 2a84a752-fbf3-4041-8b0a-304f89a49354
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6f3ec036b1d9d61c387495b48874bf742a9479ae0608f0e5c728a029df24709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002486"
---
# <a name="displaying-task-names-and-states-scripting"></a>顯示工作名稱和狀態 (腳本) 

此腳本範例示範如何列舉工作資料夾中的工作，並顯示每項工作的屬性值。

下列程式說明如何顯示工作資料夾中所有工作的工作名稱和狀態。

**顯示工作資料夾中所有工作的工作名稱和狀態**

1.  建立 [**TaskService**](taskservice.md) 物件。

    此物件可讓您連接到工作排程器服務，並存取特定的工作資料夾。

2.  取得工作資料夾，其中包含您想要的相關資訊。

    使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法來取得資料夾。

3.  從資料夾中取得工作的集合。

    您可以使用 [**TaskFolder GetTasks**](taskfolder-gettasks.md) 方法，取得工作 ([**RegisteredTaskCollection**](registeredtaskcollection.md)) 的集合。

4.  取得集合中的工作數目，並列舉集合中的每個工作。

    使用物件的 [**RegisteredTaskCollection**](registeredtaskcollection.md) 集合來取得 [**RegisteredTask**](registeredtask.md) 物件實例。 每個實例都會包含集合中的工作。 然後，您可以從每個已註冊的工作中，顯示 (屬性值) 的資訊。

下列 VBScript 範例顯示如何列舉根工作資料夾中已註冊的工作集合，並顯示每項工作的名稱和狀態。


```VB
'---------------------------------------------------------
' This sample enumerates through the tasks on the local computer and
' displays their name and state.
'---------------------------------------------------------


' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

' Get the task folder that contains the tasks. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")
 
Dim taskCollection
Set taskCollection = rootFolder.GetTasks(0)

Dim numberOfTasks
numberOfTasks = taskCollection.Count

If numberOfTasks = 0 Then 
    Wscript.Echo "No tasks are registered."
Else
    WScript.Echo "Number of tasks registered: " & numberOfTasks
    
    Dim registeredTask
    For Each registeredTask In taskCollection
        WScript.Echo "Task Name: " & registeredTask.Name
    
        Dim taskState 
        Select Case registeredTask.State 
            Case "0"
                taskState = "Unknown"
            Case "1"
                taskState = "Disabled"
            Case "2"
                taskState = "Queued"
            Case "3"
                taskState = "Ready"
            Case "4"
                taskState = "Running"
        End Select

        WScript.Echo "    Task State: " & taskState
    Next
End If

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




