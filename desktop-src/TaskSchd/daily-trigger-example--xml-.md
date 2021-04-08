---
title: " (XML) 的每日觸發程式範例"
description: 此範例中的 XML 會定義一項工作，該工作會在每天上午 8 00 啟動「記事本」。
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2020
ms.locfileid: "103679524"
---
# <a name="daily-trigger-example-xml"></a><span data-ttu-id="9fa2a-103"> (XML) 的每日觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="9fa2a-103">Daily Trigger Example (XML)</span></span>

<span data-ttu-id="9fa2a-104">此範例中的 XML 會定義一項工作，該工作會在每天上午8:00 啟動「記事本」。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-104">The XML in this example defines a task that starts Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="9fa2a-105">此範例也會顯示如何設定觸發程式的重複模式，以重複執行工作。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-105">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span>

<span data-ttu-id="9fa2a-106">若要註冊 XML 中定義的工作，您可以使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 函數 ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) 來撰寫腳本) 或 Schtasks.exe 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-106">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="9fa2a-107">如果您使用位於 C： \\ Windows System32 目錄) 的 Schtasks.exe 工具 (\\ ，則可以使用下列命令來註冊工作： **schtasks.exe/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* 。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-107">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a><span data-ttu-id="9fa2a-108">定義在每天上午8:00 啟動「記事本」的工作</span><span class="sxs-lookup"><span data-stu-id="9fa2a-108">To define a task to start Notepad every day at 8:00 AM</span></span>

<span data-ttu-id="9fa2a-109">下列 XML 範例示範如何使用單一執行動作來定義工作 (啟動 [記事本]) 、單一行事曆觸發程式 (在每天上午8:00 點啟動工作) ，以及其他數個會影響工作如何由工作排程器處理的工作設定。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every day at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
        </CalendarTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="9fa2a-110">TaskScheduler 架構元素</span><span class="sxs-lookup"><span data-stu-id="9fa2a-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="9fa2a-111">以下是使用此範例時要牢記在心的一些重要元素。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-111">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="9fa2a-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="9fa2a-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="9fa2a-113">包含工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-113">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="9fa2a-114">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="9fa2a-114">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="9fa2a-115">定義啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-115">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="9fa2a-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="9fa2a-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="9fa2a-117">定義每日行事曆觸發程式。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-117">Defines the daily calendar trigger.</span></span> <span data-ttu-id="9fa2a-118">在此情況下，會使用四個子項目：指定觸發程式啟動和停用時間、每日排程，以及工作的重複模式的開始和結束界限。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-118">In this case, four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the daily schedule, and the repetition pattern for the task.</span></span> <span data-ttu-id="9fa2a-119">[**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是行事曆觸發程式的必要元素。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-119">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="9fa2a-120">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="9fa2a-120">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    <span data-ttu-id="9fa2a-121">定義每日排程。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-121">Defines the daily schedule.</span></span> <span data-ttu-id="9fa2a-122">在此情況下，間隔會設定為每天執行工作。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-122">In this case, the interval is set to perform the task every day.</span></span>

-   <span data-ttu-id="9fa2a-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md)：定義工作執行所在的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   [<span data-ttu-id="9fa2a-124">**設定**</span><span class="sxs-lookup"><span data-stu-id="9fa2a-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="9fa2a-125">定義工作排程器用來執行工作的工作設定。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="9fa2a-126">**動作**</span><span class="sxs-lookup"><span data-stu-id="9fa2a-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="9fa2a-127">定義工作執行的動作 (在此案例中，執行 [記事本]) 。</span><span class="sxs-lookup"><span data-stu-id="9fa2a-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fa2a-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fa2a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fa2a-129">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="9fa2a-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




