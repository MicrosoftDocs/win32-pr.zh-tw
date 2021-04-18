---
title: 正在抓取工作屬性範例
description: 若要抓取工作的屬性，請呼叫 ITaskScheduler Activate 來取得工作物件的介面，然後呼叫適當的 ITask 方法來取出您感興趣的工作屬性。
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- 正在工作排程器中抓取工作屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316048"
---
# <a name="retrieving-task-property-examples"></a><span data-ttu-id="1d43b-104">正在抓取工作屬性範例</span><span class="sxs-lookup"><span data-stu-id="1d43b-104">Retrieving Task Property Examples</span></span>

<span data-ttu-id="1d43b-105">若要抓取工作的屬性，請呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得工作物件的介面，然後呼叫適當的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 方法來取出您感興趣的工作屬性。</span><span class="sxs-lookup"><span data-stu-id="1d43b-105">To retrieve the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the task property that you are interested in.</span></span> <span data-ttu-id="1d43b-106">頁面底部所列的程式碼範例會顯示如何取出不同的工作屬性。</span><span class="sxs-lookup"><span data-stu-id="1d43b-106">The code examples listed at the bottom of the page show how to retrieve the different task properties.</span></span>

<span data-ttu-id="1d43b-107">頁面底部所列的程式碼範例會顯示如何抓取工作物件特有的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d43b-107">The code examples listed at the bottom of the page show how to retrieve the properties that are unique to task objects.</span></span> <span data-ttu-id="1d43b-108">針對也適用于工作的其他 [*工作專案*](w.md) 屬性，請參閱抓取 [工作專案範例](retrieving-work-item-property-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="1d43b-108">For other [*work item*](w.md) properties that also apply to tasks, see [Retrieving Work Item Examples](retrieving-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="1d43b-109">在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。</span><span class="sxs-lookup"><span data-stu-id="1d43b-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="1d43b-110">請注意，如果您要抓取 (的字串屬性，例如應用程式名稱、參數或工作目錄) ，您必須呼叫 [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放為傳回字串所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1d43b-110">Note that if you are retrieving a string property (such as the application name, parameters, or working directory), you must call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="1d43b-111">下列程式描述如何取出工作屬性。</span><span class="sxs-lookup"><span data-stu-id="1d43b-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="1d43b-112">**若要取出 task 屬性**</span><span class="sxs-lookup"><span data-stu-id="1d43b-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="1d43b-113">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="1d43b-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="1d43b-114"> (這些範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="1d43b-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="1d43b-115">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="1d43b-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="1d43b-116"> (請注意，此範例會取得 "Test Task" 工作。 ) </span><span class="sxs-lookup"><span data-stu-id="1d43b-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="1d43b-117">呼叫適當的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 方法，以取得您感興趣的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d43b-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="1d43b-118">視需要處理屬性。</span><span class="sxs-lookup"><span data-stu-id="1d43b-118">Process the property as needed.</span></span> <span data-ttu-id="1d43b-119"> (這些範例會將屬性列印到畫面。 ) </span><span class="sxs-lookup"><span data-stu-id="1d43b-119">(These examples print the property to the screen.)</span></span>
5.  <span data-ttu-id="1d43b-120">如果傳回的屬性是字串，請呼叫 [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來釋放針對傳回字串所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1d43b-120">If the returned property is a string, call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="1d43b-121">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="1d43b-121">For a code example of</span></span>                                                                                                                           | <span data-ttu-id="1d43b-122">請參閱</span><span class="sxs-lookup"><span data-stu-id="1d43b-122">See</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d43b-123">抓取與指定工作相關聯之應用程式的名稱</span><span class="sxs-lookup"><span data-stu-id="1d43b-123">Retrieving the name of the application associated with a given task</span></span>                                                                             | [<span data-ttu-id="1d43b-124">C/c + + 程式碼範例：正在抓取工作應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="1d43b-124">C/C++ Code Example: Retrieving the Task Application Name</span></span>](c-c-code-example-retrieving-the-task-application-name.md)   |
| <span data-ttu-id="1d43b-125">抓取工作可執行檔最大時間量，並在畫面上顯示該數位</span><span class="sxs-lookup"><span data-stu-id="1d43b-125">Retrieving the maximum amount of time the task can run and displaying that number on the screen</span></span>                                                 | [<span data-ttu-id="1d43b-126">C/c + + 程式碼範例：正在抓取工作 MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="1d43b-126">C/C++ Code Example: Retrieving the Task MaxRunTime</span></span>](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| <span data-ttu-id="1d43b-127">抓取工作執行時所執行的參數字串，並在畫面上顯示該字串</span><span class="sxs-lookup"><span data-stu-id="1d43b-127">Retrieving the parameter string that is executed when the task is run and displaying that string on the screen</span></span>                                  | [<span data-ttu-id="1d43b-128">C/c + + 程式碼範例：正在抓取工作參數</span><span class="sxs-lookup"><span data-stu-id="1d43b-128">C/C++ Code Example: Retrieving Task Parameters</span></span>](c-c-code-example-retrieving-task-parameters.md)                       |
| <span data-ttu-id="1d43b-129">正在抓取工作的 [*優先權層級*](p.md)</span><span class="sxs-lookup"><span data-stu-id="1d43b-129">Retrieving the [*priority level*](p.md) of the task</span></span>                                                                    | [<span data-ttu-id="1d43b-130">C/c + + 程式碼範例：正在抓取工作優先順序</span><span class="sxs-lookup"><span data-stu-id="1d43b-130">C/C++ Code Example: Retrieving Task Priority</span></span>](c-c-code-example-retrieving-task-priority.md)                           |
| <span data-ttu-id="1d43b-131">抓取 [*工作的工作目錄*](w.md) ，並顯示幕幕上工作目錄的路徑</span><span class="sxs-lookup"><span data-stu-id="1d43b-131">Retrieving the [*working directory*](w.md) of a task and displaying the path to the working directory on the screen</span></span> | [<span data-ttu-id="1d43b-132">C/c + + 程式碼範例：取出工作工作目錄</span><span class="sxs-lookup"><span data-stu-id="1d43b-132">C/C++ Code Example: Retrieving the Task Working Directory</span></span>](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="1d43b-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d43b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d43b-134">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="1d43b-134">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 