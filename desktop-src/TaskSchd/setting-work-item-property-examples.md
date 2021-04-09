---
title: 設定工作專案屬性範例
description: 若要設定工作專案的屬性，請呼叫 ITaskScheduler Activate 來取出工作專案物件的介面，然後呼叫適當的方法來設定您感興趣的工作屬性。 目前，唯一有效的工作專案是 tasks。
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- 設定工作專案屬性工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933454"
---
# <a name="setting-work-item-property-examples"></a><span data-ttu-id="dcf26-105">設定工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="dcf26-105">Setting Work Item Property Examples</span></span>

<span data-ttu-id="dcf26-106">若要設定工作專案的屬性，請呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 來取出工作專案物件的介面，然後呼叫適當的方法來設定您感興趣的工作屬性。</span><span class="sxs-lookup"><span data-stu-id="dcf26-106">To set the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to set the task property you are interested in.</span></span> <span data-ttu-id="dcf26-107">目前，唯一有效的工作專案是 tasks。</span><span class="sxs-lookup"><span data-stu-id="dcf26-107">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="dcf26-108">頁面底部所列的程式碼範例會顯示如何設定適用于所有工作專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="dcf26-108">The code examples listed at the bottom of the page show how to set the properties that apply to all work items.</span></span> <span data-ttu-id="dcf26-109">如需工作特有的其他屬性，請參閱 [設定工作屬性範例](setting-task-property-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="dcf26-109">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="dcf26-110">在下列程式碼範例中，不再需要所有介面之後，就會釋放它們。</span><span class="sxs-lookup"><span data-stu-id="dcf26-110">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="dcf26-111">在下列範例中，修改過的物件一律會藉由呼叫 [**IPersistFile：： Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="dcf26-111">In the following examples, the modified object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="dcf26-112"> ([**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面是 task 物件所繼承的標準 COM 介面。 ) </span><span class="sxs-lookup"><span data-stu-id="dcf26-112">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="dcf26-113">下列程式描述如何設定 task 屬性。</span><span class="sxs-lookup"><span data-stu-id="dcf26-113">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="dcf26-114">**若要設定 task 屬性**</span><span class="sxs-lookup"><span data-stu-id="dcf26-114">**To set a task property**</span></span>

1.  <span data-ttu-id="dcf26-115">呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。</span><span class="sxs-lookup"><span data-stu-id="dcf26-115">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="dcf26-116"> (這些範例假設工作排程器服務正在執行。 ) </span><span class="sxs-lookup"><span data-stu-id="dcf26-116">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="dcf26-117">呼叫 [**ITaskScheduler：： Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) 以取得 task 物件的 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面。</span><span class="sxs-lookup"><span data-stu-id="dcf26-117">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="dcf26-118"> (請注意，工作是目前唯一有效的工作專案類型。 ) </span><span class="sxs-lookup"><span data-stu-id="dcf26-118">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="dcf26-119">呼叫適當的 [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) 方法，以設定您感興趣的屬性。</span><span class="sxs-lookup"><span data-stu-id="dcf26-119">Call the appropriate [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method to set the property you are interested in.</span></span> <span data-ttu-id="dcf26-120">請注意， [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面會繼承 **IScheduledWorkItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="dcf26-120">Note that **IScheduledWorkItem** methods are inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="dcf26-121">呼叫 [**IPersistFile：： Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 可將修改過的工作物件儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="dcf26-121">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="dcf26-122">如需的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="dcf26-122">For a code example of</span></span>                            | <span data-ttu-id="dcf26-123">請參閱</span><span class="sxs-lookup"><span data-stu-id="dcf26-123">See</span></span>                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf26-124">設定已知工作的帳戶資訊</span><span class="sxs-lookup"><span data-stu-id="dcf26-124">Setting the account information for a known task</span></span> | [<span data-ttu-id="dcf26-125">C/c + + 程式碼範例：設定工作帳戶資訊</span><span class="sxs-lookup"><span data-stu-id="dcf26-125">C/C++ Code Example: Setting Task Account Information</span></span>](c-c-code-example-setting-task-account-information.md) |
| <span data-ttu-id="dcf26-126">設定已知工作的批註</span><span class="sxs-lookup"><span data-stu-id="dcf26-126">Setting the comment of a known task</span></span>              | [<span data-ttu-id="dcf26-127">C/c + + 程式碼範例：設定工作批註</span><span class="sxs-lookup"><span data-stu-id="dcf26-127">C/C++ Code Example: Setting Task Comment</span></span>](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a><span data-ttu-id="dcf26-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="dcf26-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcf26-129">工作排程器1.0 範例</span><span class="sxs-lookup"><span data-stu-id="dcf26-129">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 