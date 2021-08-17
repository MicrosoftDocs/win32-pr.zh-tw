---
title: " (腳本) 的每日觸發程式範例"
description: 這個腳本範例會示範如何建立在每天上午 8 00 執行記事本的工作。
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 530d687264af9d2e7dbd4e9d05cf7dde39a449d3249c3576a35edc8a9e9f088d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139531"
---
# <a name="daily-trigger-example-scripting"></a> (腳本) 的每日觸發程式範例

這個腳本範例會示範如何建立在每天上午8:00 執行記事本的工作。 此工作包含每日觸發程式，指定啟動觸發程式的起始界限，以及指定工作執行的當日時間、指定工作每天執行的觸發程式間隔，以及用來停用觸發程式的結束界限。 此範例也會顯示如何設定觸發程式的重複模式，以重複執行工作。 此工作也包含執行記事本的可執行動作。

下列程式描述如何排程工作，以在每天上午8:00 啟動可執行檔。  (這些步驟對應至範例程式碼中所含的程式碼批註。 ) 

**排定在每天上午8:00 開始記事本**

1.  建立 [**TaskService**](taskservice.md) 物件。 此物件可讓您在指定的資料夾中建立工作。
2.  取得工作資料夾並建立工作。 使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法取得儲存工作的資料夾，以及使用 [**TaskService. NewTask**](taskservice-newtask.md) 方法來建立代表工作的 [**TaskDefinition**](taskdefinition.md) 物件。
3.  使用 [**TaskDefinition**](taskdefinition.md) 物件定義工作的相關資訊。 您可以使用 [**設定 TaskDefinition**](taskdefinition-settings.md)屬性來定義決定工作排程器服務如何執行工作的設定，以及使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md)屬性來定義描述工作的資訊。
4.  使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性建立每日觸發程式。 這個屬性會提供用來建立觸發程式之 [**TriggerCollection**](triggercollection.md) 物件的存取權。 使用 [**TriggerCollection**](triggercollection-create.md) 方法 (指定您要建立的觸發程式類型) 建立每日觸發程式。 當您建立觸發程式時，請設定啟動界限來啟動觸發程式，並指定工作執行的時間、天數之間的間隔，以及結束界限以停用觸發程式。 下列範例顯示如何設定觸發程式的重複模式，以重複執行工作。
5.  使用 [ [**TaskDefinition**](taskdefinition-actions.md) ] 屬性，建立要執行之工作的動作。 這個屬性會提供用來建立動作之 [**actioncollection 動作**](actioncollection.md) 物件的存取權。 使用 [**actioncollection 動作**](actioncollection-create.md) 方法來指定您要建立的動作類型。 這個範例會使用 [**ExecAction**](execaction.md) 物件，代表執行命令列操作的動作。
6.  使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法註冊工作。 在此範例中，工作會在每天上午8:00 開始記事本。

下列 VBScript 範例示範如何排程工作，以便每天上午8:00 執行記事本。


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a daily basis.
'------------------------------------------------------------------

' A constant that specifies a daily trigger.
const TriggerTypeDaily = 2
' A constant that specifies an executable action.
const ActionTypeExec = 0

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
regInfo.Description = "Start notepad at 8:00AM daily"
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a daily trigger. Note that the start boundary 
' specifies the time of day that the task starts and the 
' interval specifies what days the task is run.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeDaily)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this time is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysInterval = 1    'Task runs every day.
trigger.Id = "DailyTriggerId"
trigger.Enabled = True

' Set the task repetition pattern for the task.
' This will repeat the task 5 times.
Dim repetitionPattern
Set repetitionPattern = trigger.Repetition
repetitionPattern.Duration = "PT4M"
repetitionPattern.Interval = "PT1M"

'***********************************************************
' Create the action for the task to execute.

' Add an action to the task to run notepad.exe.
Dim Action
Set Action = taskDefinition.Actions.Create( ActionTypeExec )
Action.Path = "C:\Windows\System32\notepad.exe"

WScript.Echo "Task definition created. About to submit the task..."

'***********************************************************
' Register (create) the task.

call rootFolder.RegisterTaskDefinition( _
    "Test Daily Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




