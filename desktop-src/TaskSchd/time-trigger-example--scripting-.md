---
title: 腳本)  (時間觸發程式範例
description: 此腳本範例示範如何建立在特定時間執行「記事本」的工作。
ms.assetid: 8511ffcd-166f-4c63-9cd2-ead53dde9ed8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77cbf9eab12f5ca027fbb6c48ade37a9f57d9beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967815"
---
# <a name="time-trigger-example-scripting"></a><span data-ttu-id="edf74-103">腳本)  (時間觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="edf74-103">Time Trigger Example (Scripting)</span></span>

<span data-ttu-id="edf74-104">此腳本範例示範如何建立在特定時間執行「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="edf74-104">This scripting example shows how to create a task that runs Notepad at a specific time.</span></span> <span data-ttu-id="edf74-105">此工作包含以時間為基礎的觸發程式，此觸發程式會指定啟動工作的起始界限、執行「記事本」的可執行動作，以及停用工作的結束界限。</span><span class="sxs-lookup"><span data-stu-id="edf74-105">The task contains a time-based trigger that specifies a start boundary to activate the task, an executable action that runs Notepad, and an end boundary that deactivates the task.</span></span>

<span data-ttu-id="edf74-106">下列程式描述如何排程工作，以便在特定時間啟動可執行檔。</span><span class="sxs-lookup"><span data-stu-id="edf74-106">The following procedure describes how to schedule a task to start an executable at a specific time.</span></span>

<span data-ttu-id="edf74-107">**將記事本排定在特定時間啟動**</span><span class="sxs-lookup"><span data-stu-id="edf74-107">**To Schedule Notepad to start at a Specific Time**</span></span>

1.  <span data-ttu-id="edf74-108">建立 [**TaskService**](taskservice.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="edf74-108">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="edf74-109">此物件可讓您在指定的資料夾中建立工作。</span><span class="sxs-lookup"><span data-stu-id="edf74-109">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="edf74-110">取得工作資料夾並建立工作。</span><span class="sxs-lookup"><span data-stu-id="edf74-110">Get a task folder and create a task.</span></span> <span data-ttu-id="edf74-111">使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法取得儲存工作的資料夾，以及使用 [**TaskService. NewTask**](taskservice-newtask.md) 方法來建立代表工作的 [**TaskDefinition**](taskdefinition.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="edf74-111">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="edf74-112">使用 [**TaskDefinition**](taskdefinition.md) 物件定義工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="edf74-112">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="edf74-113">您可以使用 [ [**TaskDefinition**](taskdefinition-settings.md) ] 屬性來定義決定工作排程器服務如何執行工作的設定，以及使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md) 屬性來定義描述工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="edf74-113">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="edf74-114">使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性建立以時間為基礎的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="edf74-114">Create a time-based trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="edf74-115">這個屬性會提供 [**TriggerCollection**](triggercollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="edf74-115">This property provides access to the [**TriggerCollection**](triggercollection.md) object.</span></span> <span data-ttu-id="edf74-116">使用 [**TriggerCollection**](triggercollection-create.md) 方法 (指定您要建立的觸發程式類型) 建立以時間為基礎的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="edf74-116">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a time-based trigger.</span></span> <span data-ttu-id="edf74-117">當您建立觸發程式時，請設定觸發程式的開始界限和結束界限，以啟動並停用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="edf74-117">As you create the trigger, set the start boundary and end boundary of the trigger to activate and deactivate the trigger.</span></span> <span data-ttu-id="edf74-118">開始界限會指定何時執行工作的動作。</span><span class="sxs-lookup"><span data-stu-id="edf74-118">The start boundary specifies when the task's action will be performed.</span></span>
5.  <span data-ttu-id="edf74-119">使用 [ [**TaskDefinition**](taskdefinition-actions.md) ] 屬性，建立要執行之工作的動作。</span><span class="sxs-lookup"><span data-stu-id="edf74-119">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="edf74-120">這個屬性會提供 [**actioncollection 動作**](actioncollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="edf74-120">This property provides access to the [**ActionCollection**](actioncollection.md) object.</span></span> <span data-ttu-id="edf74-121">使用 [**actioncollection 動作**](actioncollection-create.md) 方法來指定您要建立的動作類型。</span><span class="sxs-lookup"><span data-stu-id="edf74-121">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="edf74-122">這個範例會使用 [**ExecAction**](execaction.md) 物件，代表執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="edf74-122">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="edf74-123">使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法註冊工作。</span><span class="sxs-lookup"><span data-stu-id="edf74-123">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="edf74-124">在此範例中，工作將會在目前的時間加上30秒來啟動 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="edf74-124">For this example the task will start Notepad at the current time plus 30 seconds.</span></span>

<span data-ttu-id="edf74-125">下列 VBScript 範例示範如何排程工作，以便在工作註冊後的30秒內執行「記事本」。</span><span class="sxs-lookup"><span data-stu-id="edf74-125">The following VBScript example shows how to schedule a task to execute Notepad 30 seconds after the task is registered.</span></span>


```VB
'------------------------------------------------------------------
' This sample schedules a task to start notepad.exe 30 seconds
' from the time the task is registered.
'------------------------------------------------------------------

' A constant that specifies a time-based trigger.
const TriggerTypeTime = 1
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
regInfo.Description = "Start notepad at a certain time"
regInfo.Author = "Author Name"

'********************************************************
' Set the principal for the task
Dim principal
Set principal = taskDefinition.Principal

' Set the logon type to interactive logon
principal.LogonType = 3


' Set the task setting info for the Task Scheduler by
' creating a TaskSettings object.
Dim settings
Set settings = taskDefinition.Settings
settings.Enabled = True
settings.StartWhenAvailable = True
settings.Hidden = False

'********************************************************
' Create a time-based trigger.
Dim triggers
Set triggers = taskDefinition.Triggers

Dim trigger
Set trigger = triggers.Create(TriggerTypeTime)

' Trigger variables that define when the trigger is active.
Dim startTime, endTime

Dim time
time = DateAdd("s", 30, Now)  'start time = 30 seconds from now
startTime = XmlTime(time)

time = DateAdd("n", 5, Now) 'end time = 5 minutes from now
endTime = XmlTime(time)

WScript.Echo "startTime :" & startTime
WScript.Echo "endTime :" & endTime

trigger.StartBoundary = startTime
trigger.EndBoundary = endTime
trigger.ExecutionTimeLimit = "PT5M"    'Five minutes
trigger.Id = "TimeTriggerId"
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
    "Test TimeTrigger", taskDefinition, 6, , , 3)

WScript.Echo "Task submitted."



'------------------------------------------------------------------
' Used to get the time for the trigger 
' startBoundary and endBoundary.
' Return the time in the correct format: 
' YYYY-MM-DDTHH:MM:SS. 
'------------------------------------------------------------------
Function XmlTime(t)
    Dim cSecond, cMinute, CHour, cDay, cMonth, cYear
    Dim tTime, tDate

    cSecond = "0" & Second(t)
    cMinute = "0" & Minute(t)
    cHour = "0" & Hour(t)
    cDay = "0" & Day(t)
    cMonth = "0" & Month(t)
    cYear = Year(t)

    tTime = Right(cHour, 2) & ":" & Right(cMinute, 2) & _
        ":" & Right(cSecond, 2)
    tDate = cYear & "-" & Right(cMonth, 2) & "-" & Right(cDay, 2)
    XmlTime = tDate & "T" & tTime 
End Function

```



## <a name="related-topics"></a><span data-ttu-id="edf74-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="edf74-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edf74-127">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="edf74-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




