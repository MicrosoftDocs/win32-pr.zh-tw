---
title: TaskService. GetRunningTasks 方法
description: 針對腳本，會取得正在執行之工作的集合。
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- GetRunningTasks 方法工作排程器
- GetRunningTasks 方法工作排程器，TaskService 物件
- TaskService 物件工作排程器，GetRunningTasks 方法
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686547"
---
# <a name="taskservicegetrunningtasks-method"></a><span data-ttu-id="6b1d7-106">TaskService. GetRunningTasks 方法</span><span class="sxs-lookup"><span data-stu-id="6b1d7-106">TaskService.GetRunningTasks method</span></span>

<span data-ttu-id="6b1d7-107">針對腳本，會取得正在執行之工作的集合。</span><span class="sxs-lookup"><span data-stu-id="6b1d7-107">For scripting, gets a collection of running tasks.</span></span>

> [!Note]  
> <span data-ttu-id="6b1d7-108">**TaskService** 只會傳回執行中工作的集合，而這些工作是在使用者的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="6b1d7-108">**TaskService.GetRunningTasks** will only return a collection of running tasks that are running at or below a user's security context.</span></span> <span data-ttu-id="6b1d7-109">例如，針對 Administrators 群組的成員， **GetRunningTasks** 會傳回所有執行中工作的集合，但是針對 users 群組的成員， **GetRunningTasks** 只會傳回在 users 群組安全性內容下執行的工作集合。</span><span class="sxs-lookup"><span data-stu-id="6b1d7-109">For example, for members of the Administrators group, **GetRunningTasks** will return a collection of all running tasks, but for members of the Users group, **GetRunningTasks** will only return a collection of tasks that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6b1d7-110">語法</span><span class="sxs-lookup"><span data-stu-id="6b1d7-110">Syntax</span></span>


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="6b1d7-111">參數</span><span class="sxs-lookup"><span data-stu-id="6b1d7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b1d7-112">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b1d7-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b1d7-113">傳入1以傳回所有執行中的工作，包括隱藏的工作。</span><span class="sxs-lookup"><span data-stu-id="6b1d7-113">Pass in 1 to return all running tasks, including hidden tasks.</span></span> <span data-ttu-id="6b1d7-114">傳入0以傳回非隱藏工作的執行中工作集合。</span><span class="sxs-lookup"><span data-stu-id="6b1d7-114">Pass in 0 to return a collection of running tasks that are not hidden tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b1d7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b1d7-115">Return value</span></span>

<span data-ttu-id="6b1d7-116">包含目前正在執行之工作的 [**RunningTaskCollection**](runningtaskcollection.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6b1d7-116">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains the currently running tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b1d7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b1d7-117">Requirements</span></span>



| <span data-ttu-id="6b1d7-118">需求</span><span class="sxs-lookup"><span data-stu-id="6b1d7-118">Requirement</span></span> | <span data-ttu-id="6b1d7-119">值</span><span class="sxs-lookup"><span data-stu-id="6b1d7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1d7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b1d7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b1d7-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b1d7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6b1d7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b1d7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b1d7-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b1d7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b1d7-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6b1d7-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b1d7-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b1d7-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b1d7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6b1d7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b1d7-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b1d7-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b1d7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b1d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b1d7-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="6b1d7-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





