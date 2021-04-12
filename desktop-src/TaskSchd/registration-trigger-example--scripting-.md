---
title: " (腳本) 的註冊觸發程式範例"
description: 這個腳本範例會示範如何建立工作，而該工作已排程在工作註冊時執行「記事本」。
ms.assetid: 956b3a21-7d36-4d06-be84-690884ba653a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bce6271927e74e31f25b3ac86783b35899bbd862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311420"
---
# <a name="registration-trigger-example-scripting"></a> (腳本) 的註冊觸發程式範例

這個腳本範例會示範如何建立工作，而該工作已排程在工作註冊時執行「記事本」。 此工作包含指定工作開始界限和結束界限的註冊觸發程式。 啟動界限會指定觸發程式的啟動時間。 此工作也包含指定工作以執行 [記事本] 的動作。

> [!Note]  
> 更新註冊觸發程式的工作時，工作會在更新發生之後執行。

 

下列程式描述如何排程可執行檔（例如「記事本」）在註冊工作時啟動。

**排定在註冊工作時啟動 [記事本]**

1.  建立 [**TaskService**](taskservice.md) 物件。 此物件可讓您在指定的資料夾中建立工作。
2.  取得工作資料夾並建立工作。 使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法取得儲存工作的資料夾，以及使用 [**TaskService. NewTask**](taskservice-newtask.md) 方法來建立代表工作的 [**TaskDefinition**](taskdefinition.md) 物件。
3.  使用 [**TaskDefinition**](taskdefinition.md) 物件定義工作的相關資訊。 您可以使用 [ [**TaskDefinition**](taskdefinition-settings.md) ] 屬性來定義決定工作排程器服務如何執行工作的設定，以及使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md) 屬性來定義描述工作的資訊。
4.  使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性建立註冊觸發程式。 這個屬性會提供 [**TriggerCollection**](triggercollection.md) 物件的存取權。 使用 [**TriggerCollection**](triggercollection-create.md) 方法 (指定您要建立的觸發程式類型) 建立註冊觸發程式。
5.  使用 [ [**TaskDefinition**](taskdefinition-actions.md) ] 屬性，建立要執行之工作的動作。 這個屬性會提供 [**actioncollection 動作**](actioncollection.md) 物件的存取權。 使用 [**actioncollection 動作**](actioncollection-create.md) 方法來指定您要建立的動作類型。 這個範例會使用 [**ExecAction**](execaction.md) 物件，此物件代表啟動可執行檔的動作。
6.  使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法註冊工作。

下列 VBScript 範例示範如何建立工作，以排定在註冊工作時執行「記事本」。


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when
' the task is registered.
'---------------------------------------------------------

' A constant that specifies a registration trigger.
const TriggerTypeRegistration = 7
' A constant that specifies an executable action.
const ActionTypeExecutable = 0   


'********************************************************
' Create the TaskService object.
Set service = CreateObject("Schedule.Service")
call service.Connect()

'********************************************************
' Get a folder to create a task definition in. 
Dim rootFolder
Set rootFolder = service.GetFolder("\")

' The taskDefinition variable is the TaskDefinition object.
Dim taskDefinition
' The flags parameter is 0 because it is not supported.
Set taskDefinition = service.NewTask(0) 

'********************************************************
' Define information about the task.

' Set the registration info for the task by 
' creating the RegistrationInfo object.
Dim regInfo
Set regInfo = taskDefinition.RegistrationInfo
regInfo.Description = "Start Notepad when the task is registered."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a registration trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeRegistration)

trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "RegistrationTriggerId"   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes Notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Registration Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




