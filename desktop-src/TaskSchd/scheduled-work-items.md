---
title: 排程的工作專案
description: 工作排程器會使用兩個詞彙來描述其可以排程工作專案和工作的內容。
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- 工作專案工作排程器
- 工作專案工作排程器，相較于工作
- 工作工作排程器
- 工作工作排程器，相較于工作專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300543"
---
# <a name="scheduled-work-items"></a><span data-ttu-id="73e38-107">排程的工作專案</span><span class="sxs-lookup"><span data-stu-id="73e38-107">Scheduled Work Items</span></span>

<span data-ttu-id="73e38-108">工作排程器會使用兩個詞彙來描述它可以排程的內容：工作專案和工作。</span><span class="sxs-lookup"><span data-stu-id="73e38-108">The Task Scheduler uses two terms to describe what it can schedule: work items and tasks.</span></span> <span data-ttu-id="73e38-109">在這兩個詞彙中， [*工作專案*](w.md) 是更一般的詞彙，描述可排程的任何專案類型。</span><span class="sxs-lookup"><span data-stu-id="73e38-109">Of these two terms, [*work item*](w.md) is a more general term that describes any type of item that can be scheduled.</span></span> <span data-ttu-id="73e38-110">*工作專案* 可以是工作排程器服務在專案觸發程式 () 所指定的時間執行的任何專案。</span><span class="sxs-lookup"><span data-stu-id="73e38-110">A *work item* can be any item that the Task Scheduler service runs at a time that is specified by the item's trigger(s).</span></span>

<span data-ttu-id="73e38-111">相反地，工作 [*是特定*](t.md) 類型的工作專案。</span><span class="sxs-lookup"><span data-stu-id="73e38-111">In contrast, a [*task*](t.md) is a specific type of work item.</span></span> <span data-ttu-id="73e38-112">目前唯一支援的排程工作專案類型是工作。</span><span class="sxs-lookup"><span data-stu-id="73e38-112">Currently, the only type of scheduled work item that is supported is a task.</span></span>

<span data-ttu-id="73e38-113">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面包含所有類型的已排程工作專案所支援的方法。</span><span class="sxs-lookup"><span data-stu-id="73e38-113">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface contains methods that are supported by all types of scheduled work items.</span></span> <span data-ttu-id="73e38-114">例如，帳戶資訊、執行時間和應用程式定義的批註都是可套用至所有工作專案類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="73e38-114">For example, account information, run times, and application-defined comments are properties that may apply to all types of work items.</span></span> <span data-ttu-id="73e38-115">這些屬性可以透過 **IScheduledWorkItem** 介面設定和抓取。</span><span class="sxs-lookup"><span data-stu-id="73e38-115">These properties can be set and retrieved through the **IScheduledWorkItem** interface.</span></span>

<span data-ttu-id="73e38-116">[**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面只包含工作所支援的方法。</span><span class="sxs-lookup"><span data-stu-id="73e38-116">The [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface contains methods that are supported only by tasks.</span></span>

<span data-ttu-id="73e38-117">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面的方法目前是由 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面所繼承，未來將會由其他工作專案介面繼承。</span><span class="sxs-lookup"><span data-stu-id="73e38-117">The methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface are currently inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface and in the future will be inherited by other work item interfaces.</span></span>

| <span data-ttu-id="73e38-118">範例</span><span class="sxs-lookup"><span data-stu-id="73e38-118">For examples of</span></span>                                              | <span data-ttu-id="73e38-119">請參閱</span><span class="sxs-lookup"><span data-stu-id="73e38-119">See</span></span>                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e38-120">建立新的工作。</span><span class="sxs-lookup"><span data-stu-id="73e38-120">Creating a new task.</span></span>                                         | [<span data-ttu-id="73e38-121">使用 NewWorkItem 範例建立工作</span><span class="sxs-lookup"><span data-stu-id="73e38-121">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |
| <span data-ttu-id="73e38-122">正在執行現有的工作。</span><span class="sxs-lookup"><span data-stu-id="73e38-122">Running an existing task.</span></span>                                    | [<span data-ttu-id="73e38-123">啟動工作範例</span><span class="sxs-lookup"><span data-stu-id="73e38-123">Starting a Task Example</span></span>](starting-a-task-example.md)                                     |
| <span data-ttu-id="73e38-124">正在抓取適用于所有工作專案類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="73e38-124">Retrieving properties that apply to all types of work items.</span></span> | [<span data-ttu-id="73e38-125">正在抓取工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="73e38-125">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="73e38-126">設定適用于所有工作專案類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="73e38-126">Setting properties that apply to all types of work items.</span></span>    | [<span data-ttu-id="73e38-127">設定工作專案屬性範例</span><span class="sxs-lookup"><span data-stu-id="73e38-127">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |



 

 

 




