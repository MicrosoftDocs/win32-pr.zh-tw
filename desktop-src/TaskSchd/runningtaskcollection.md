---
title: RunningTaskCollection 物件
description: 腳本物件，提供用來控制執行中工作的集合。
ms.assetid: b137fcf3-634c-4ac6-908d-357f54da3025
keywords:
- RunningTaskCollection 物件工作排程器
- RunningTaskCollection 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RunningTaskCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c28d75cee0ba4b19751ba1e4c5a5c3061a1dad64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466032"
---
# <a name="runningtaskcollection-object"></a><span data-ttu-id="204e3-105">RunningTaskCollection 物件</span><span class="sxs-lookup"><span data-stu-id="204e3-105">RunningTaskCollection object</span></span>

<span data-ttu-id="204e3-106">腳本物件，提供用來控制執行中工作的集合。</span><span class="sxs-lookup"><span data-stu-id="204e3-106">Scripting object that provides a collection that is used to control running tasks.</span></span>

## <a name="members"></a><span data-ttu-id="204e3-107">成員</span><span class="sxs-lookup"><span data-stu-id="204e3-107">Members</span></span>

<span data-ttu-id="204e3-108">**RunningTaskCollection** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="204e3-108">The **RunningTaskCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="204e3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="204e3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="204e3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="204e3-110">Properties</span></span>

<span data-ttu-id="204e3-111">**RunningTaskCollection** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="204e3-111">The **RunningTaskCollection** object has these properties.</span></span>



| <span data-ttu-id="204e3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="204e3-112">Property</span></span>                                                | <span data-ttu-id="204e3-113">描述</span><span class="sxs-lookup"><span data-stu-id="204e3-113">Description</span></span>                                                    |
|:--------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="204e3-114">**計數**</span><span class="sxs-lookup"><span data-stu-id="204e3-114">**Count**</span></span>](runningtaskcollection-count.md)<br/> | <span data-ttu-id="204e3-115">取得集合中執行中的工作數目。</span><span class="sxs-lookup"><span data-stu-id="204e3-115">Gets the number of running tasks in the collection.</span></span><br/> |
| [<span data-ttu-id="204e3-116">**項目**</span><span class="sxs-lookup"><span data-stu-id="204e3-116">**Item**</span></span>](runningtaskcollection-item.md)<br/>   | <span data-ttu-id="204e3-117">從集合中取得指定的工作。</span><span class="sxs-lookup"><span data-stu-id="204e3-117">Gets the specified task from the collection.</span></span> <br/>       |



 

## <a name="requirements"></a><span data-ttu-id="204e3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="204e3-118">Requirements</span></span>



| <span data-ttu-id="204e3-119">需求</span><span class="sxs-lookup"><span data-stu-id="204e3-119">Requirement</span></span> | <span data-ttu-id="204e3-120">值</span><span class="sxs-lookup"><span data-stu-id="204e3-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="204e3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="204e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="204e3-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="204e3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="204e3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="204e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="204e3-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="204e3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="204e3-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="204e3-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="204e3-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="204e3-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="204e3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="204e3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="204e3-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="204e3-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="204e3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="204e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="204e3-130">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="204e3-130">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="204e3-131">工作排程器</span><span class="sxs-lookup"><span data-stu-id="204e3-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="204e3-132">**RunningTask**</span><span class="sxs-lookup"><span data-stu-id="204e3-132">**RunningTask**</span></span>](runningtask.md)
</dt> <dt>

[<span data-ttu-id="204e3-133">**TaskService. GetRunningTasks**</span><span class="sxs-lookup"><span data-stu-id="204e3-133">**TaskService.GetRunningTasks**</span></span>](taskservice-getrunningtasks.md)
</dt> <dt>

[<span data-ttu-id="204e3-134">**RegisteredTask.GetInstances**</span><span class="sxs-lookup"><span data-stu-id="204e3-134">**RegisteredTask.GetInstances**</span></span>](registeredtask-getinstances.md)
</dt> </dl>

 

 





