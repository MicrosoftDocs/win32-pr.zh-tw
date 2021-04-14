---
title: RegisteredTask. GetRunTimes 方法
description: 針對腳本，取得已註冊的工作排定在指定時間執行的時間。
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- GetRunTimes 方法工作排程器
- GetRunTimes 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，GetRunTimes 方法
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509059"
---
# <a name="registeredtaskgetruntimes-method"></a><span data-ttu-id="60be6-106">RegisteredTask. GetRunTimes 方法</span><span class="sxs-lookup"><span data-stu-id="60be6-106">RegisteredTask.GetRunTimes method</span></span>

<span data-ttu-id="60be6-107">針對腳本，取得已註冊的工作排定在指定時間執行的時間。</span><span class="sxs-lookup"><span data-stu-id="60be6-107">For scripting, gets the times that the registered task is scheduled to run during a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="60be6-108">語法</span><span class="sxs-lookup"><span data-stu-id="60be6-108">Syntax</span></span>


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a><span data-ttu-id="60be6-109">參數</span><span class="sxs-lookup"><span data-stu-id="60be6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60be6-110">*開始* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60be6-110">*begin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60be6-111">查詢的開始時間。</span><span class="sxs-lookup"><span data-stu-id="60be6-111">The starting time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="60be6-112">*結束* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60be6-112">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60be6-113">查詢的結束時間。</span><span class="sxs-lookup"><span data-stu-id="60be6-113">The ending time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="60be6-114">*計數* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="60be6-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60be6-115">工作將執行的排程時間數目。</span><span class="sxs-lookup"><span data-stu-id="60be6-115">The number of scheduled times the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="60be6-116">*rgstTaskTimes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="60be6-116">*rgstTaskTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60be6-117">工作將執行的排程時間。</span><span class="sxs-lookup"><span data-stu-id="60be6-117">The scheduled times that the task will run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60be6-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="60be6-118">Return value</span></span>

<span data-ttu-id="60be6-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="60be6-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60be6-120">備註</span><span class="sxs-lookup"><span data-stu-id="60be6-120">Remarks</span></span>

<span data-ttu-id="60be6-121">如果已註冊的工作包含個別停用的觸發程式，這些觸發程式仍會影響下一次所傳回的排程執行時間（即使已停用）。</span><span class="sxs-lookup"><span data-stu-id="60be6-121">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="60be6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="60be6-122">Requirements</span></span>



| <span data-ttu-id="60be6-123">需求</span><span class="sxs-lookup"><span data-stu-id="60be6-123">Requirement</span></span> | <span data-ttu-id="60be6-124">值</span><span class="sxs-lookup"><span data-stu-id="60be6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60be6-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60be6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60be6-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60be6-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="60be6-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60be6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60be6-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60be6-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="60be6-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="60be6-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="60be6-130"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="60be6-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="60be6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="60be6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60be6-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60be6-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60be6-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60be6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60be6-134">工作排程器</span><span class="sxs-lookup"><span data-stu-id="60be6-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="60be6-135">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="60be6-135">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





