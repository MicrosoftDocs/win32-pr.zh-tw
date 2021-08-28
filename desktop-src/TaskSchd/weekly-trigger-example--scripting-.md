---
title: " (腳本) 的每週觸發程式範例"
description: 此腳本範例示範如何建立在每週星期一上午 8 00 執行記事本的工作。
ms.assetid: 68ef73b0-3780-480e-90fe-940b6e8a5340
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6500dae3c0444bc41b982acc06b0e331e63aa4fb821385b416dd0d3e079671d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001766"
---
# <a name="weekly-trigger-example-scripting"></a> (腳本) 的每週觸發程式範例

此腳本範例示範如何建立在每週星期一上午8:00 執行記事本的工作。 此工作包含每日觸發程式，以指定工作執行的時間，以及記事本執行的可執行動作。

下列程式描述如何排程工作，以在每週星期一的上午8:00 啟動可執行檔。

**排定在每週星期一上午8:00 開始記事本開始**

1.  建立 [**TaskService**](taskservice.md) 物件。 此物件可讓您在指定的資料夾中建立工作。
2.  取得工作資料夾並建立工作。 使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法取得儲存工作的資料夾，以及使用 [**TaskService. NewTask**](taskservice-newtask.md) 方法來建立代表工作的 [**TaskDefinition**](taskdefinition.md) 物件。
3.  使用 [**TaskDefinition**](taskdefinition.md) 物件定義工作的相關資訊。 您可以使用 [**設定 TaskDefinition**](taskdefinition-settings.md)屬性來定義決定工作排程器服務如何執行工作的設定，以及使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md)屬性來定義描述工作的資訊。
4.  使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性來建立每週觸發程式。 這個屬性會提供用來建立觸發程式之 [**TriggerCollection**](triggercollection.md) 物件的存取權。

    使用 [**TriggerCollection**](triggercollection-create.md) 方法 (指定您要建立的觸發程式類型) 建立每週觸發程式。

    設定 [**WeeklyTrigger StartBoundary**](trigger-startboundary.md) 屬性，以指定啟動觸發程式的時間，以及執行工作的當日時間。 在此範例中，會在2005年1月1日啟動觸發程式，且工作會在上午8:00 執行。

    設定 [**WeeklyTrigger EndBoundary**](trigger-endboundary.md)屬性，以指定何時停用觸發程式。 在此範例中，會在2015年1月1日停用觸發程式。

    設定 [**WeeklyTrigger DaysOfWeek**](weeklytrigger-daysofweek.md) 屬性，以指定工作執行的周間日。 在此範例中，工作會在星期一執行。

    設定 [**WeeklyTrigger WeeksInterval**](weeklytrigger-weeksinterval.md)屬性，以指定排程中周之間的間隔。 在此範例中，工作會每週執行一次。

5.  使用 [ [**TaskDefinition**](taskdefinition-actions.md) ] 屬性，建立要執行之工作的動作。 這個屬性會提供用來建立動作之 [**actioncollection 動作**](actioncollection.md) 物件的存取權。 使用 [**actioncollection 動作**](actioncollection-create.md) 方法來指定您要建立的動作類型。 這個範例會使用 [**ExecAction**](execaction.md) 物件，代表執行命令列操作的動作。
6.  使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法註冊工作。 在此範例中，工作會在每週星期一的上午8:00 開始記事本。

下列 VBScript 範例示範如何排程工作，以便每天上午8:00 執行記事本。


```VB
'------------------------------------------------------------------
' This sample schedules a task to start on a weekly basis.
'------------------------------------------------------------------

' A constant that specifies a weekly trigger.
const TriggerTypeWeekly = 3
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
regInfo.Description = "Start Notepad weekly."
regInfo.Author = "Administrator"

' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a weekly trigger. Note that the start boundary 
' specifies the time of day that the task starts, the 
' day-of-week specfies on what day of the week the task 
' runs, and the interval specifies what weeks the task runs.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeWeekly)

' Trigger variables that define when the trigger is active 
' and the time of day that the task is run. The format of 
' this tims is YYYY-MM-DDTHH:MM:SS
Dim startTime, endTime

Dim time
startTime = "2006-05-02T08:00:00"  'Task runs at 8:00 AM
endTime = "2015-05-02T08:00:00"

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.DaysOfWeek = 1
trigger.WeeksInterval = 1    'Task runs every week.
trigger.Id = "WeeklyTriggerId"
trigger.Enabled = True

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
    "Test Weekly Trigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




