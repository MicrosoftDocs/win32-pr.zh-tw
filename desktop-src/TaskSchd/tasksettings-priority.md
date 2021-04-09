---
title: TaskSettings Priority 屬性
description: 針對腳本，取得或設定工作的優先權層級。
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Priority 屬性工作排程器
- Priority 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器，Priority 屬性
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934011"
---
# <a name="tasksettingspriority-property"></a><span data-ttu-id="68ac5-106">TaskSettings Priority 屬性</span><span class="sxs-lookup"><span data-stu-id="68ac5-106">TaskSettings.Priority property</span></span>

<span data-ttu-id="68ac5-107">針對腳本，取得或設定工作的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="68ac5-107">For scripting, gets or sets the priority level of the task.</span></span>

<span data-ttu-id="68ac5-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="68ac5-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ac5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ac5-109">Syntax</span></span>


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a><span data-ttu-id="68ac5-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="68ac5-110">Property value</span></span>

<span data-ttu-id="68ac5-111">工作的優先權層級 (0-10) 。</span><span class="sxs-lookup"><span data-stu-id="68ac5-111">The priority level (0-10) of the task.</span></span> <span data-ttu-id="68ac5-112">預設值為 7。</span><span class="sxs-lookup"><span data-stu-id="68ac5-112">The default is 7.</span></span>

## <a name="remarks"></a><span data-ttu-id="68ac5-113">備註</span><span class="sxs-lookup"><span data-stu-id="68ac5-113">Remarks</span></span>

<span data-ttu-id="68ac5-114">優先權層級0是最高優先順序，而優先順序層級10是最低優先順序。</span><span class="sxs-lookup"><span data-stu-id="68ac5-114">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="68ac5-115">預設值為 7。</span><span class="sxs-lookup"><span data-stu-id="68ac5-115">The default value is 7.</span></span> <span data-ttu-id="68ac5-116">優先權層級7和8用於背景工作，而優先順序層級4、5和6則用於互動式工作。</span><span class="sxs-lookup"><span data-stu-id="68ac5-116">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="68ac5-117">工作的動作會在具有以優先權類別值為基礎之優先權的進程中啟動。</span><span class="sxs-lookup"><span data-stu-id="68ac5-117">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="68ac5-118">優先權層級值 (執行緒優先順序) 用於 COM 處理常式、訊息方塊，以及電子郵件工作動作。</span><span class="sxs-lookup"><span data-stu-id="68ac5-118">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="68ac5-119">如需優先順序類別和優先權層級值的詳細資訊，請參閱 [排程優先順序](/windows/desktop/ProcThread/scheduling-priorities)。</span><span class="sxs-lookup"><span data-stu-id="68ac5-119">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="68ac5-120">下表列出 *priority* 參數的可能值，以及對應的 priority 類別和優先權層級值。</span><span class="sxs-lookup"><span data-stu-id="68ac5-120">The following table lists the possible values for the *priority* parameter, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="68ac5-121">工作 *優先順序*</span><span class="sxs-lookup"><span data-stu-id="68ac5-121">Task *priority*</span></span> | <span data-ttu-id="68ac5-122">Priority 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-122">Priority Class</span></span>                 | <span data-ttu-id="68ac5-123">優先權層級</span><span class="sxs-lookup"><span data-stu-id="68ac5-123">Priority Level</span></span>                   |
|-----------------|--------------------------------|----------------------------------|
| <span data-ttu-id="68ac5-124">0</span><span class="sxs-lookup"><span data-stu-id="68ac5-124">0</span></span>               | <span data-ttu-id="68ac5-125">即時 \_ 優先權 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-125">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="68ac5-126">執行緒 \_ 優先順序 \_ 時間 \_ 嚴重不足</span><span class="sxs-lookup"><span data-stu-id="68ac5-126">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="68ac5-127">1</span><span class="sxs-lookup"><span data-stu-id="68ac5-127">1</span></span>               | <span data-ttu-id="68ac5-128">高 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-128">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="68ac5-129">執行緒 \_ 優先順序 \_ 最高</span><span class="sxs-lookup"><span data-stu-id="68ac5-129">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="68ac5-130">2</span><span class="sxs-lookup"><span data-stu-id="68ac5-130">2</span></span>               | <span data-ttu-id="68ac5-131">高於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-131">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="68ac5-132">\_ \_ 高於 \_ 一般的執行緒優先順序</span><span class="sxs-lookup"><span data-stu-id="68ac5-132">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="68ac5-133">3</span><span class="sxs-lookup"><span data-stu-id="68ac5-133">3</span></span>               | <span data-ttu-id="68ac5-134">高於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-134">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="68ac5-135">\_ \_ 高於 \_ 一般的執行緒優先順序</span><span class="sxs-lookup"><span data-stu-id="68ac5-135">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="68ac5-136">4</span><span class="sxs-lookup"><span data-stu-id="68ac5-136">4</span></span>               | <span data-ttu-id="68ac5-137">一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-137">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="68ac5-138">執行緒 \_ 優先順序 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="68ac5-138">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="68ac5-139">5</span><span class="sxs-lookup"><span data-stu-id="68ac5-139">5</span></span>               | <span data-ttu-id="68ac5-140">一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-140">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="68ac5-141">執行緒 \_ 優先順序 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="68ac5-141">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="68ac5-142">6</span><span class="sxs-lookup"><span data-stu-id="68ac5-142">6</span></span>               | <span data-ttu-id="68ac5-143">一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-143">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="68ac5-144">執行緒 \_ 優先順序 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="68ac5-144">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="68ac5-145">7</span><span class="sxs-lookup"><span data-stu-id="68ac5-145">7</span></span>               | <span data-ttu-id="68ac5-146">低於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-146">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="68ac5-147">一般的執行緒 \_ 優先順序 \_ \_</span><span class="sxs-lookup"><span data-stu-id="68ac5-147">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="68ac5-148">8</span><span class="sxs-lookup"><span data-stu-id="68ac5-148">8</span></span>               | <span data-ttu-id="68ac5-149">低於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-149">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="68ac5-150">一般的執行緒 \_ 優先順序 \_ \_</span><span class="sxs-lookup"><span data-stu-id="68ac5-150">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="68ac5-151">9</span><span class="sxs-lookup"><span data-stu-id="68ac5-151">9</span></span>               | <span data-ttu-id="68ac5-152">閒置 \_ 優先權 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-152">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="68ac5-153">執行緒 \_ 優先順序 \_ 最低</span><span class="sxs-lookup"><span data-stu-id="68ac5-153">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="68ac5-154">10</span><span class="sxs-lookup"><span data-stu-id="68ac5-154">10</span></span>              | <span data-ttu-id="68ac5-155">閒置 \_ 優先權 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="68ac5-155">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="68ac5-156">執行緒 \_ 優先順序 \_ 閒置</span><span class="sxs-lookup"><span data-stu-id="68ac5-156">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="68ac5-157">在讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="68ac5-157">When reading or writing XML for a task, this setting is specified in the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ac5-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="68ac5-158">Requirements</span></span>



| <span data-ttu-id="68ac5-159">需求</span><span class="sxs-lookup"><span data-stu-id="68ac5-159">Requirement</span></span> | <span data-ttu-id="68ac5-160">值</span><span class="sxs-lookup"><span data-stu-id="68ac5-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68ac5-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68ac5-161">Minimum supported client</span></span><br/> | <span data-ttu-id="68ac5-162">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68ac5-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="68ac5-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68ac5-163">Minimum supported server</span></span><br/> | <span data-ttu-id="68ac5-164">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68ac5-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68ac5-165">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="68ac5-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="68ac5-166"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="68ac5-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="68ac5-167">DLL</span><span class="sxs-lookup"><span data-stu-id="68ac5-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68ac5-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68ac5-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68ac5-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68ac5-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ac5-170">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="68ac5-170">**TaskSettings**</span></span>](tasksettings.md)
</dt> </dl>

 

