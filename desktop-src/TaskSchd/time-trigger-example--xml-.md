---
title: " (XML) 的時間觸發程式範例"
description: 此範例中的 XML 會定義在特定時間啟動「記事本」的工作。
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c683c831aa3a07eeb3a41db9cd2768caeb6307a
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2020
ms.locfileid: "104314049"
---
# <a name="time-trigger-example-xml"></a><span data-ttu-id="d4f12-103"> (XML) 的時間觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="d4f12-103">Time Trigger Example (XML)</span></span>

<span data-ttu-id="d4f12-104">此範例中的 XML 會定義在特定時間啟動「記事本」的工作。</span><span class="sxs-lookup"><span data-stu-id="d4f12-104">The XML in this example defines a task that starts Notepad at a specific time.</span></span>

<span data-ttu-id="d4f12-105">若要註冊 XML 中定義的工作，您可以使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 函數 ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) 來撰寫腳本) 或 Schtasks.exe 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="d4f12-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="d4f12-106">如果您使用位於 C： \\ Windows System32 目錄) 的 Schtasks.exe 工具 (\\ ，則可以使用下列命令來註冊工作： **schtasks.exe/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* 。</span><span class="sxs-lookup"><span data-stu-id="d4f12-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a><span data-ttu-id="d4f12-107">定義工作以在特定時間啟動記事本</span><span class="sxs-lookup"><span data-stu-id="d4f12-107">To define a task to start Notepad at a specific time</span></span>

<span data-ttu-id="d4f12-108">下列 XML 範例示範如何使用單一執行動作來定義工作 (啟動 [記事本]) 、在指定的時間啟動工作的單一時間觸發程式，以及其他會影響工作排程器處理工作方式的其他工作設定。</span><span class="sxs-lookup"><span data-stu-id="d4f12-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single time trigger that starts the task at a specified time, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe at a specific time.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after at a specified time.</Description>
    </RegistrationInfo>
    <Triggers>
        <TimeTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </TimeTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="d4f12-109">TaskScheduler 架構元素</span><span class="sxs-lookup"><span data-stu-id="d4f12-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="d4f12-110">以下是使用此範例時要牢記在心的一些重要元素：</span><span class="sxs-lookup"><span data-stu-id="d4f12-110">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="d4f12-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)：包含工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="d4f12-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="d4f12-112">[**觸發**](taskschedulerschema-triggers-tasktype-element.md)程式：定義啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d4f12-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="d4f12-113">[**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)：定義時間觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d4f12-113">[**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): Defines the time trigger.</span></span> <span data-ttu-id="d4f12-114">在此情況下，會使用三個子項目：指定觸發程式啟動和停用時間的開始和結束界限，以及指定觸發程式可啟動工作的最大時間量的執行時間限制。</span><span class="sxs-lookup"><span data-stu-id="d4f12-114">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the execution time limit that specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="d4f12-115">[**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是時間觸發程式的必要元素。</span><span class="sxs-lookup"><span data-stu-id="d4f12-115">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time triggers.</span></span>
-   <span data-ttu-id="d4f12-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md)：定義工作執行所在的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="d4f12-116">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="d4f12-117">[**設定**](taskschedulerschema-settings-tasktype-element.md)：定義工作排程器用來執行工作的工作設定。</span><span class="sxs-lookup"><span data-stu-id="d4f12-117">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="d4f12-118">[**動作**](taskschedulerschema-actions-tasktype-element.md)：定義工作執行的動作 (在此案例中，執行 [記事本]) 。</span><span class="sxs-lookup"><span data-stu-id="d4f12-118">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions that the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4f12-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4f12-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4f12-120">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="d4f12-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




