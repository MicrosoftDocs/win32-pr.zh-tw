---
title: " (XML) 的註冊觸發程式範例"
description: 此範例中的 XML 會定義工作在註冊時啟動 [記事本]。
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2020
ms.locfileid: "106966435"
---
# <a name="registration-trigger-example-xml"></a><span data-ttu-id="72a91-103"> (XML) 的註冊觸發程式範例</span><span class="sxs-lookup"><span data-stu-id="72a91-103">Registration Trigger Example (XML)</span></span>

<span data-ttu-id="72a91-104">此範例中的 XML 會定義工作在註冊時啟動 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="72a91-104">The XML in this example defines a task that starts Notepad when the task is registered.</span></span>

<span data-ttu-id="72a91-105">若要註冊 XML 中定義的工作，您可以使用 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 函數 ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) 來撰寫腳本) 或 Schtasks.exe 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="72a91-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="72a91-106">如果您使用位於 C： \\ Windows System32 目錄) 的 Schtasks.exe 工具 (\\ ，則可以使用下列命令來註冊工作： **schtasks.exe/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* 。</span><span class="sxs-lookup"><span data-stu-id="72a91-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

> [!Note]  
> <span data-ttu-id="72a91-107">更新註冊觸發程式的工作時，工作會在更新發生之後執行。</span><span class="sxs-lookup"><span data-stu-id="72a91-107">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a><span data-ttu-id="72a91-108">定義在註冊時啟動「記事本」的工作</span><span class="sxs-lookup"><span data-stu-id="72a91-108">To define a task to start Notepad on registration</span></span>

<span data-ttu-id="72a91-109">下列 XML 範例示範如何使用單一執行動作來定義工作 (啟動 [記事本]) 、在註冊工作時啟動工作的單一註冊觸發程式，以及其他會影響工作排程器處理工作方式的其他工作設定。</span><span class="sxs-lookup"><span data-stu-id="72a91-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single registration trigger that starts the task when it is registered, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="72a91-110">更新註冊觸發程式的工作時，工作會在更新發生之後執行。</span><span class="sxs-lookup"><span data-stu-id="72a91-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="72a91-111">TaskScheduler 架構元素</span><span class="sxs-lookup"><span data-stu-id="72a91-111">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="72a91-112">以下是使用此範例時要牢記在心的一些重要元素。</span><span class="sxs-lookup"><span data-stu-id="72a91-112">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="72a91-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)：包含工作的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="72a91-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="72a91-114">[**觸發**](taskschedulerschema-triggers-tasktype-element.md)程式：定義啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="72a91-114">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="72a91-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md)：定義註冊觸發程式。</span><span class="sxs-lookup"><span data-stu-id="72a91-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): Defines the registration trigger.</span></span> <span data-ttu-id="72a91-116">在此情況下，只會使用兩個子項目：指定啟動和停用觸發程式的時間和結束界限。</span><span class="sxs-lookup"><span data-stu-id="72a91-116">In this case, only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="72a91-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md)：定義工作執行所在的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="72a91-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="72a91-118">[**設定**](taskschedulerschema-settings-tasktype-element.md)：定義工作排程器用來執行工作的工作設定。</span><span class="sxs-lookup"><span data-stu-id="72a91-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="72a91-119">[**動作**](taskschedulerschema-actions-tasktype-element.md)：定義工作執行的動作。</span><span class="sxs-lookup"><span data-stu-id="72a91-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="72a91-120">在此情況下，執行「記事本」。</span><span class="sxs-lookup"><span data-stu-id="72a91-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72a91-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="72a91-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72a91-122">使用工作排程器</span><span class="sxs-lookup"><span data-stu-id="72a91-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




