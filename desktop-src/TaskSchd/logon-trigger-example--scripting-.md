---
title: '登入觸發程式範例 (腳本) '
description: 這個腳本範例會示範如何建立排定在使用者登入時執行「記事本」的工作。
ms.assetid: f25e105f-9439-4646-bdfd-609ee99a5d55
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72a8c4b5d0d67b59160eb3ed0b13885ee7e0eb51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183281"
---
# <a name="logon-trigger-example-scripting"></a>登入觸發程式範例 (腳本) 

這個腳本範例會示範如何建立排定在使用者登入時執行「記事本」的工作。 此工作包含登入觸發程式，可指定開始工作的開始界限，以及指定使用者的使用者識別碼。 此工作會使用 Administrators 群組作為安全性內容來執行工作，以進行註冊。

下列程式描述如何排程可執行檔（例如 [記事本]），以便在指定的使用者登入時啟動。

**排定在使用者登入時啟動 [記事本]**

1.  建立 [**TaskService**](taskservice.md) 物件。 此物件可讓您在指定的資料夾中建立工作。
2.  取得工作資料夾並建立工作。 使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法取得儲存工作的資料夾，以及使用 [**TaskService. NewTask**](taskservice-newtask.md) 方法來建立代表工作的 [**TaskDefinition**](taskdefinition.md) 物件。
3.  使用 [**TaskDefinition**](taskdefinition.md) 物件定義工作的相關資訊。 您可以使用 [ [**TaskDefinition**](taskdefinition-settings.md) ] 屬性來定義決定工作排程器服務如何執行工作的設定，以及使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md) 屬性來定義描述工作的資訊。
4.  使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性建立登入觸發程式。 這個屬性會提供 [**TriggerCollection**](triggercollection.md) 物件的存取權。 使用 [**TriggerCollection**](triggercollection-create.md) 方法 (指定您要建立的觸發程式類型) 建立登入觸發程式。 當您建立觸發程式時，請設定觸發程式的開始界限和結束界限，以啟動並停用觸發程式。 您必須設定觸發程式的 [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) 屬性，如此一來，當指定的使用者在開始界限之後登入時，就會排定工作的動作執行。
5.  使用 [ [**TaskDefinition**](taskdefinition-actions.md) ] 屬性，建立要執行之工作的動作。 這個屬性會提供 [**actioncollection 動作**](actioncollection.md) 物件的存取權。 使用 [**actioncollection 動作**](actioncollection-create.md) 方法來指定您要建立的動作類型。 這個範例會使用 [**ExecAction**](execaction.md) 物件，此物件代表啟動可執行檔的動作。
6.  使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法註冊工作。 此範例會註冊工作，讓它使用系統管理員群組做為執行工作的安全性內容。

下列 VBScript 範例示範如何排程工作，以在使用者登入時執行 [記事本]。


```VB
'---------------------------------------------------------
' This sample schedules a task to start notepad.exe when a user logs on.
'---------------------------------------------------------

' A constant that specifies a logon trigger.
const TriggerTypeLogon = 9
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
regInfo.Description = "Task will execute Notepad when a " & _
    "specified user logs on."
regInfo.Author = "Author Name"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.StartWhenAvailable = True

'********************************************************
' Create a logon trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeLogon)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime
startTime = "2006-05-02T10:49:02"
endTime = "2006-05-02T10:52:02"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    ' Five minutes
trigger.Id = "LogonTriggerId"
trigger.UserId = "DOMAIN\UserName"   ' Must be a valid user account   

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task. The action executes notepad.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExecutable )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.
const createOrUpdateTask = 6
call rootFolder.RegisterTaskDefinition( _
    "Test Logon Trigger", taskDefinition, createOrUpdateTask, _
    "Builtin\Administrators", , 4)

WScript.Echo "Task submitted."
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




