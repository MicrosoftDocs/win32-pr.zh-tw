---
title: 設定工作屬性範例
description: 若要設定工作的屬性，請呼叫 ITaskScheduler Activate 來取出工作物件的介面，然後呼叫適當的 ITask 方法來設定您感興趣的工作屬性。
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- 設定工作屬性工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966259"
---
# <a name="setting-task-property-examples"></a><span data-ttu-id="35d74-104">設定工作屬性範例</span><span class="sxs-lookup"><span data-stu-id="35d74-104">Setting Task Property Examples</span></span>

<span data-ttu-id="35d74-105">若要設定工作的屬性，請呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取出工作物件的介面，然後呼叫適當的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 方法來設定您感興趣的工作屬性。</span><span class="sxs-lookup"><span data-stu-id="35d74-105">To set the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the task property you are interested in.</span></span>

<span data-ttu-id="35d74-106">頁面底部所列的程式碼範例會顯示如何設定工作物件的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="35d74-106">The code examples listed at the bottom of the page show how to set the properties that are unique to task objects.</span></span> <span data-ttu-id="35d74-107">針對也適用于工作的其他 [*工作專案*](w.md) 屬性，請參閱 [設定工作專案屬性範例](setting-work-item-property-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="35d74-107">For other [*work item*](w.md) properties that also apply to tasks, see [Setting Work Item Property Examples](setting-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="35d74-108">在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。</span><span class="sxs-lookup"><span data-stu-id="35d74-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="35d74-109">在下列範例中，修改後的工作物件一律會藉由呼叫 [**IPersistFile：： Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="35d74-109">In the following examples, the modified task object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="35d74-110"> ([**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面是 task 物件所繼承的標準 COM 介面。 ) </span><span class="sxs-lookup"><span data-stu-id="35d74-110">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="35d74-111">下列程式描述如何設定 task 屬性。</span><span class="sxs-lookup"><span data-stu-id="35d74-111">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="35d74-112">**若要設定 task 屬性**</span><span class="sxs-lookup"><span data-stu-id="35d74-112">**To set a task property**</span></span>

1.  <span data-ttu-id="35d74-113">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="35d74-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="35d74-114"> (這些範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="35d74-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="35d74-115">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="35d74-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="35d74-116"> (請注意，此範例會取得 "Test Task" 工作。 ) </span><span class="sxs-lookup"><span data-stu-id="35d74-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="35d74-117">呼叫適當的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 方法，以設定您感興趣的屬性。</span><span class="sxs-lookup"><span data-stu-id="35d74-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the property you are interested in.</span></span>
4.  <span data-ttu-id="35d74-118">呼叫 [**IPersistFile：： Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 可將修改過的工作物件儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="35d74-118">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="35d74-119">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="35d74-119">For a code example of</span></span>                                                                                                                                | <span data-ttu-id="35d74-120">請參閱</span><span class="sxs-lookup"><span data-stu-id="35d74-120">See</span></span>                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35d74-121">設定與已知工作相關聯的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="35d74-121">Setting the name of the application associated with a known task</span></span>                                                                                     | [<span data-ttu-id="35d74-122">C/c + + 程式碼範例：設定應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="35d74-122">C/C++ Code Example: Setting Application Name</span></span>](c-c-code-example-setting-application-name.md)   |
| <span data-ttu-id="35d74-123">設定已知工作的執行時間上限</span><span class="sxs-lookup"><span data-stu-id="35d74-123">Setting the maximum run time of a known task</span></span>                                                                                                         | [<span data-ttu-id="35d74-124">C/c + + 程式碼範例：設定 MaxRunTime</span><span class="sxs-lookup"><span data-stu-id="35d74-124">C/C++ Code Example: Setting MaxRunTime</span></span>](c-c-code-example-setting-maxruntime.md)               |
| <span data-ttu-id="35d74-125">清除與已知工作相關聯的所有命令列參數</span><span class="sxs-lookup"><span data-stu-id="35d74-125">Clearing all command-line parameters associated with a known task</span></span>                                                                                    | [<span data-ttu-id="35d74-126">C/c + + 程式碼範例：設定工作參數</span><span class="sxs-lookup"><span data-stu-id="35d74-126">C/C++ Code Example: Setting Task Parameters</span></span>](c-c-code-example-setting-task-parameters.md)     |
| <span data-ttu-id="35d74-127">此範例會設定測試工作的優先順序，然後儲存工作。</span><span class="sxs-lookup"><span data-stu-id="35d74-127">This example sets the priority of a test task and then saves the task.</span></span> <span data-ttu-id="35d74-128">此範例假設本機電腦上已有測試工作。</span><span class="sxs-lookup"><span data-stu-id="35d74-128">This example assumes that the test task already exists on the local computer.</span></span> | [<span data-ttu-id="35d74-129">C/c + + 程式碼範例：設定工作優先順序</span><span class="sxs-lookup"><span data-stu-id="35d74-129">C/C++ Code Example: Setting Task Priority</span></span>](c-c-code-example-setting-task-priority.md)         |
| <span data-ttu-id="35d74-130">設定已知 [*工作的工作目錄*](w.md)</span><span class="sxs-lookup"><span data-stu-id="35d74-130">Setting the [*working directory*](w.md) of a known task</span></span>                                                                  | [<span data-ttu-id="35d74-131">C/c + + 程式碼範例：設定工作目錄</span><span class="sxs-lookup"><span data-stu-id="35d74-131">C/C++ Code Example: Setting Working Directory</span></span>](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="35d74-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="35d74-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35d74-133">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="35d74-133">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 