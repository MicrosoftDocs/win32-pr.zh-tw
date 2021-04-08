---
title: " (腳本) 的每日觸發程式範例"
description: 此腳本範例會示範如何建立在每天上午 8 00 執行「記事本」的工作。
ms.assetid: a13bd54d-b45a-46e5-8281-d080f50f6bef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3399934786e1cd0f95ca020c92027ccafafa5272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839847"
---
# <a name="daily-trigger-example-scripting"></a><span data-ttu-id="6d23c-103"> (腳本) 的每日觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="6d23c-103">Daily Trigger Example (Scripting)</span></span>

<span data-ttu-id="6d23c-104">此腳本範例會示範如何建立在每天上午8:00 執行「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="6d23c-104">This scripting example shows how to create a task that runs Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="6d23c-105">此工作包含每日觸發程式，指定啟動觸發程式的起始界限，以及指定工作執行的當日時間、指定工作每天執行的觸發程式間隔，以及用來停用觸發程式的結束界限。</span><span class="sxs-lookup"><span data-stu-id="6d23c-105">The task contains a daily trigger that specifies a start boundary to activate the trigger and to specify the time of day that the task runs, a trigger interval to specify that the task runs every day, and an end boundary to deactivates the trigger.</span></span> <span data-ttu-id="6d23c-106">此範例也會顯示如何設定觸發程式的重複模式，以重複執行工作。</span><span class="sxs-lookup"><span data-stu-id="6d23c-106">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span> <span data-ttu-id="6d23c-107">此工作也包含執行「記事本」的可執行動作。</span><span class="sxs-lookup"><span data-stu-id="6d23c-107">The task also contains an executable action that runs Notepad.</span></span>

<span data-ttu-id="6d23c-108">下列程式描述如何排程工作，以在每天上午8:00 啟動可執行檔。</span><span class="sxs-lookup"><span data-stu-id="6d23c-108">The following procedure describes how to schedule a task to start an executable at 8:00 AM every day.</span></span> <span data-ttu-id="6d23c-109"> (這些步驟對應至範例程式碼中所含的程式碼批註。 ) </span><span class="sxs-lookup"><span data-stu-id="6d23c-109">(These steps correspond to the code comments included in the example code.)</span></span>

<span data-ttu-id="6d23c-110">**將 [記事本] 排定在每天上午8:00 開始**</span><span class="sxs-lookup"><span data-stu-id="6d23c-110">**To schedule Notepad to start at 8:00 AM every day**</span></span>

1.  <span data-ttu-id="6d23c-111">建立 [**TaskService**](taskservice.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6d23c-111">Create a [**TaskService**](taskservice.md) object.</span></span> <span data-ttu-id="6d23c-112">此物件可讓您在指定的資料夾中建立工作。</span><span class="sxs-lookup"><span data-stu-id="6d23c-112">This object allows you to create the task in a specified folder.</span></span>
2.  <span data-ttu-id="6d23c-113">取得工作資料夾並建立工作。</span><span class="sxs-lookup"><span data-stu-id="6d23c-113">Get a task folder and create a task.</span></span> <span data-ttu-id="6d23c-114">使用 [**TaskService. GetFolder**](taskservice-getfolder.md) 方法取得儲存工作的資料夾，以及使用 [**TaskService. NewTask**](taskservice-newtask.md) 方法來建立代表工作的 [**TaskDefinition**](taskdefinition.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6d23c-114">Use the [**TaskService.GetFolder**](taskservice-getfolder.md) method to get the folder where the task is stored and the [**TaskService.NewTask**](taskservice-newtask.md) method to create the [**TaskDefinition**](taskdefinition.md) object that represents the task.</span></span>
3.  <span data-ttu-id="6d23c-115">使用 [**TaskDefinition**](taskdefinition.md) 物件定義工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6d23c-115">Define information about the task using the [**TaskDefinition**](taskdefinition.md) object.</span></span> <span data-ttu-id="6d23c-116">您可以使用 [ [**TaskDefinition**](taskdefinition-settings.md) ] 屬性來定義決定工作排程器服務如何執行工作的設定，以及使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md) 屬性來定義描述工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="6d23c-116">Use the [**TaskDefinition.Settings**](taskdefinition-settings.md) property to define the settings that determine how the Task Scheduler service performs the task and the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property to define the information that describes the task.</span></span>
4.  <span data-ttu-id="6d23c-117">使用 [**TaskDefinition**](taskdefinition-triggers.md) 屬性建立每日觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6d23c-117">Create a daily trigger using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span> <span data-ttu-id="6d23c-118">這個屬性會提供用來建立觸發程式之 [**TriggerCollection**](triggercollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="6d23c-118">This property provides access to the [**TriggerCollection**](triggercollection.md) object that is used to create the trigger.</span></span> <span data-ttu-id="6d23c-119">使用 [**TriggerCollection**](triggercollection-create.md) 方法 (指定您要建立的觸發程式類型) 建立每日觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6d23c-119">Use the [**TriggerCollection.Create**](triggercollection-create.md) method (specifying the type of trigger you want to create) to create a daily trigger.</span></span> <span data-ttu-id="6d23c-120">當您建立觸發程式時，請設定啟動界限來啟動觸發程式，並指定工作執行的時間、天數之間的間隔，以及結束界限以停用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6d23c-120">As you create the trigger, set the start boundary to activate the trigger and specify the time of day that the task runs, the interval between the days, and the end boundary to deactivate the trigger.</span></span> <span data-ttu-id="6d23c-121">下列範例顯示如何設定觸發程式的重複模式，以重複執行工作。</span><span class="sxs-lookup"><span data-stu-id="6d23c-121">The example below shows how to set a repetition pattern for the trigger to repeat the task.</span></span>
5.  <span data-ttu-id="6d23c-122">使用 [ [**TaskDefinition**](taskdefinition-actions.md) ] 屬性，建立要執行之工作的動作。</span><span class="sxs-lookup"><span data-stu-id="6d23c-122">Create an action for the task to execute by using the [**TaskDefinition.Actions**](taskdefinition-actions.md) property.</span></span> <span data-ttu-id="6d23c-123">這個屬性會提供用來建立動作之 [**actioncollection 動作**](actioncollection.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="6d23c-123">This property provides access to the [**ActionCollection**](actioncollection.md) object used to create the action.</span></span> <span data-ttu-id="6d23c-124">使用 [**actioncollection 動作**](actioncollection-create.md) 方法來指定您要建立的動作類型。</span><span class="sxs-lookup"><span data-stu-id="6d23c-124">Use the [**ActionCollection.Create**](actioncollection-create.md) method to specify the type of action you want to create.</span></span> <span data-ttu-id="6d23c-125">這個範例會使用 [**ExecAction**](execaction.md) 物件，代表執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="6d23c-125">This example uses an [**ExecAction**](execaction.md) object, which represents an action that executes a command-line operation.</span></span>
6.  <span data-ttu-id="6d23c-126">使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法註冊工作。</span><span class="sxs-lookup"><span data-stu-id="6d23c-126">Register the task using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span> <span data-ttu-id="6d23c-127">在此範例中，工作會在每天上午8:00 啟動「記事本」。</span><span class="sxs-lookup"><span data-stu-id="6d23c-127">For this example the task will start Notepad at 8:00 AM every day.</span></span>

<span data-ttu-id="6d23c-128">下列 VBScript 範例示範如何排程工作每天上午8:00 執行 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="6d23c-128">The following VBScript example shows how to schedule a task to execute Notepad every day at 8:00 AM.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6d23c-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d23c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d23c-130">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="6d23c-130">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




