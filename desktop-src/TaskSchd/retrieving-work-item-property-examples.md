---
title: 正在抓取工作專案屬性範例
description: 若要抓取工作專案的屬性，請呼叫 ITaskScheduler Activate 來取出工作專案物件的介面，然後呼叫適當的方法來取出您感興趣的工作屬性。
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- 正在工作排程器中抓取工作專案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a51c623301a4a3b53369713abe95ea1dafba80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375864"
---
# <a name="retrieving-work-item-property-examples"></a><span data-ttu-id="59133-104">正在抓取工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="59133-104">Retrieving Work Item Property Examples</span></span>

<span data-ttu-id="59133-105">若要抓取工作專案的屬性，請呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以抓取工作專案物件的介面，然後呼叫適當的方法來取出您感興趣的工作屬性。</span><span class="sxs-lookup"><span data-stu-id="59133-105">To retrieve the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to retrieve the task property you are interested in.</span></span> <span data-ttu-id="59133-106">目前，唯一有效的工作專案是 tasks。</span><span class="sxs-lookup"><span data-stu-id="59133-106">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="59133-107">此頁面底部所列的程式碼範例會示範如何取得套用至所有工作專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="59133-107">The code examples listed at the bottom of this page show how to retrieve the properties that apply to all work items.</span></span> <span data-ttu-id="59133-108">如需工作特有的其他屬性，請參閱 [設定工作屬性範例](setting-task-property-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="59133-108">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="59133-109">在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。</span><span class="sxs-lookup"><span data-stu-id="59133-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="59133-110">請注意，如果您要抓取字串屬性 (例如) 的工作專案批註，則必須呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放為傳回字串所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="59133-110">Note that if you are retrieving a string property (such as comment for a work item), you must call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="59133-111">下列程式描述如何取出工作屬性。</span><span class="sxs-lookup"><span data-stu-id="59133-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="59133-112">**若要取出 task 屬性**</span><span class="sxs-lookup"><span data-stu-id="59133-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="59133-113">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="59133-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="59133-114"> (這些範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="59133-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="59133-115">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="59133-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="59133-116"> (請注意，工作是目前唯一有效的工作專案類型。 ) </span><span class="sxs-lookup"><span data-stu-id="59133-116">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="59133-117">呼叫適當的方法，以取得您感興趣的屬性。</span><span class="sxs-lookup"><span data-stu-id="59133-117">Call the appropriate method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="59133-118">視需要處理屬性。</span><span class="sxs-lookup"><span data-stu-id="59133-118">Process the property as needed.</span></span> <span data-ttu-id="59133-119"> (這些範例只會將屬性列印到畫面。 ) </span><span class="sxs-lookup"><span data-stu-id="59133-119">(These examples simply print the property to the screen.)</span></span>
5.  <span data-ttu-id="59133-120">如果傳回的屬性是字串，請呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放針對傳回字串所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="59133-120">If the returned property is a string, call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="59133-121">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="59133-121">For a code example of</span></span>                                                                        | <span data-ttu-id="59133-122">請參閱</span><span class="sxs-lookup"><span data-stu-id="59133-122">See</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59133-123">取出已知工作的帳戶資訊</span><span class="sxs-lookup"><span data-stu-id="59133-123">Retrieving the account information of a known task</span></span>                                           | [<span data-ttu-id="59133-124">C/c + + 程式碼範例：正在抓取工作帳戶資訊</span><span class="sxs-lookup"><span data-stu-id="59133-124">C/C++ Code Example: Retrieving Task Account Information</span></span>](c-c-code-example-retrieving-task-account-information.md)       |
| <span data-ttu-id="59133-125">取出已知工作的批註字串</span><span class="sxs-lookup"><span data-stu-id="59133-125">Retrieving the comment string of a known task</span></span>                                                | [<span data-ttu-id="59133-126">C/c + + 程式碼範例：抓取工作批註</span><span class="sxs-lookup"><span data-stu-id="59133-126">C/C++ Code Example: Retrieving a Task Comment</span></span>](c-c-code-example-retrieving-a-task-comment.md)                           |
| <span data-ttu-id="59133-127">抓取工作建立者的名稱，並將它顯示在畫面上</span><span class="sxs-lookup"><span data-stu-id="59133-127">Retrieving the name of the creator of the task and displaying it on the screen</span></span>               | [<span data-ttu-id="59133-128">C/c + + 程式碼範例：正在抓取工作建立者</span><span class="sxs-lookup"><span data-stu-id="59133-128">C/C++ Code Example: Retrieving the Task Creator</span></span>](c-c-code-example-retrieving-the-task-creator.md)                       |
| <span data-ttu-id="59133-129">取出已知工作所傳回的最後一個結束代碼</span><span class="sxs-lookup"><span data-stu-id="59133-129">Retrieving the last exit code returned by a known task</span></span>                                       | [<span data-ttu-id="59133-130">C/c + + 程式碼範例：正在抓取工作結束代碼</span><span class="sxs-lookup"><span data-stu-id="59133-130">C/C++ Code Example: Retrieving Task Exit Code</span></span>](c-c-code-example-retrieving-task-exit-code.md)                           |
| <span data-ttu-id="59133-131">抓取工作的閒置等待時間，並將它顯示在螢幕上</span><span class="sxs-lookup"><span data-stu-id="59133-131">Retrieving the idle-wait time of the task and displaying it on the screen</span></span>                    | [<span data-ttu-id="59133-132">C/c + + 程式碼範例：正在抓取工作閒置-等候時間</span><span class="sxs-lookup"><span data-stu-id="59133-132">C/C++ Code Example: Retrieving Task Idle-wait Time</span></span>](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| <span data-ttu-id="59133-133">取出工作上次執行的時間，並將它顯示在螢幕上</span><span class="sxs-lookup"><span data-stu-id="59133-133">Retrieving the time the task was last run and displaying it on the screen</span></span>                    | [<span data-ttu-id="59133-134">C/c + + 程式碼範例：取出工作 MostRecentRun 時間</span><span class="sxs-lookup"><span data-stu-id="59133-134">C/C++ Code Example: Retrieving the Task MostRecentRun Time</span></span>](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| <span data-ttu-id="59133-135">在下一次工作排程執行，並在畫面上顯示該時間時，正在進行抓取</span><span class="sxs-lookup"><span data-stu-id="59133-135">Retrieving the next time the task is scheduled to run and displaying that time on the screen</span></span> | [<span data-ttu-id="59133-136">C/c + + 程式碼範例：取出工作 NextRun 時間</span><span class="sxs-lookup"><span data-stu-id="59133-136">C/C++ Code Example: Retrieving the Task NextRun Time</span></span>](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| <span data-ttu-id="59133-137">抓取工作的執行時間，並將其顯示在畫面上</span><span class="sxs-lookup"><span data-stu-id="59133-137">Retrieving the run times of the task and displaying them on the screen</span></span>                       | [<span data-ttu-id="59133-138">C/c + + 程式碼範例：正在抓取工作執行時間</span><span class="sxs-lookup"><span data-stu-id="59133-138">C/C++ Code Example: Retrieving Task Run Times</span></span>](c-c-code-example-retrieving-task-run-times.md)                           |
| <span data-ttu-id="59133-139">抓取工作的目前狀態，並將其顯示在畫面上</span><span class="sxs-lookup"><span data-stu-id="59133-139">Retrieving the current status of the task and displaying it on the screen</span></span>                    | [<span data-ttu-id="59133-140">C/c + + 程式碼範例：正在抓取工作狀態</span><span class="sxs-lookup"><span data-stu-id="59133-140">C/C++ Code Example: Retrieving Task Status</span></span>](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a><span data-ttu-id="59133-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="59133-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59133-142">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="59133-142">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 