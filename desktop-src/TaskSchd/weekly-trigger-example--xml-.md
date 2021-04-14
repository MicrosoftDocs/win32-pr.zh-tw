---
title: " (XML) 的每週觸發程式範例"
description: 此範例中的 XML 會定義以每週為基礎啟動 [記事本] 的工作。
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2020
ms.locfileid: "104374166"
---
# <a name="weekly-trigger-example-xml"></a><span data-ttu-id="a2972-103"> (XML) 的每週觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="a2972-103">Weekly Trigger Example (XML)</span></span>

<span data-ttu-id="a2972-104">此範例中的 XML 會定義以每週為基礎啟動 [記事本] 的工作。</span><span class="sxs-lookup"><span data-stu-id="a2972-104">The XML in this example defines a task that starts Notepad on a bi-weekly basis.</span></span>

<span data-ttu-id="a2972-105">若要註冊 XML 中定義的工作，您可以使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 函數 ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) 來撰寫腳本) 或 Schtasks.exe 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="a2972-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="a2972-106">如果您使用位於 C： \\ Windows System32 目錄) 的 Schtasks.exe 工具 (\\ ，則可以使用下列命令來註冊工作： **schtasks.exe/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* 。</span><span class="sxs-lookup"><span data-stu-id="a2972-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a><span data-ttu-id="a2972-107">將工作定義為在星期一上午8:00 點開始每隔一周啟動記事本</span><span class="sxs-lookup"><span data-stu-id="a2972-107">To define a task to start Notepad every other week on Monday at 8:00 AM</span></span>

<span data-ttu-id="a2972-108">下列 XML 範例示範如何使用單一執行動作來定義工作 (啟動 [記事本]) 、單一行事曆觸發程式 (在星期一的上午8:00 點開始每隔一周進行工作) ，以及其他會影響工作排程器處理工作方式的其他工作設定。</span><span class="sxs-lookup"><span data-stu-id="a2972-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every other week on Monday at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="a2972-109">TaskScheduler 架構元素</span><span class="sxs-lookup"><span data-stu-id="a2972-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="a2972-110">以下是使用此範例時要牢記在心的一些重要元素。</span><span class="sxs-lookup"><span data-stu-id="a2972-110">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="a2972-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="a2972-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="a2972-112">包含工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="a2972-112">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="a2972-113">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="a2972-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="a2972-114">定義啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="a2972-114">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="a2972-115">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="a2972-115">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="a2972-116">定義每週行事曆觸發程式。</span><span class="sxs-lookup"><span data-stu-id="a2972-116">Defines the weekly calendar trigger.</span></span> <span data-ttu-id="a2972-117">在此情況下，只會使用四個子項目：指定啟動和停用觸發程式的時間、每週排程，以及執行工作的星期幾。</span><span class="sxs-lookup"><span data-stu-id="a2972-117">In this case, only four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the weekly schedule, and the days of the week that the task will run on.</span></span> <span data-ttu-id="a2972-118">[**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是行事曆觸發程式的必要元素。</span><span class="sxs-lookup"><span data-stu-id="a2972-118">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="a2972-119">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="a2972-119">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    <span data-ttu-id="a2972-120">定義每週排程。</span><span class="sxs-lookup"><span data-stu-id="a2972-120">Defines the weekly schedule.</span></span> <span data-ttu-id="a2972-121">在此情況下，間隔設定為在星期一每隔一周執行工作。</span><span class="sxs-lookup"><span data-stu-id="a2972-121">In this case, the interval is set to perform the task every other week on a Monday.</span></span>

-   [<span data-ttu-id="a2972-122">**主要**</span><span class="sxs-lookup"><span data-stu-id="a2972-122">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md)

    <span data-ttu-id="a2972-123">定義工作執行所在的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="a2972-123">Defines the security context that a task runs under.</span></span>

-   [<span data-ttu-id="a2972-124">**設定**</span><span class="sxs-lookup"><span data-stu-id="a2972-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="a2972-125">定義工作排程器用來執行工作的工作設定。</span><span class="sxs-lookup"><span data-stu-id="a2972-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="a2972-126">**動作**</span><span class="sxs-lookup"><span data-stu-id="a2972-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="a2972-127">定義工作執行的動作 (在此案例中，執行 [記事本]) 。</span><span class="sxs-lookup"><span data-stu-id="a2972-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2972-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2972-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2972-129">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="a2972-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




