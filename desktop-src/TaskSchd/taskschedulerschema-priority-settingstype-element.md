---
title: 優先權 (settingsType) 元素
description: 指定工作的優先權層級。
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Priority 元素工作排程器
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384098"
---
# <a name="priority-settingstype-element"></a><span data-ttu-id="87cde-104">優先權 (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="87cde-104">Priority (settingsType) Element</span></span>

<span data-ttu-id="87cde-105">指定工作的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="87cde-105">Specifies the priority level for the task.</span></span>

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

<span data-ttu-id="87cde-106">**Priority** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="87cde-106">The **Priority** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="87cde-107">父元素</span><span class="sxs-lookup"><span data-stu-id="87cde-107">Parent element</span></span>



| <span data-ttu-id="87cde-108">元素</span><span class="sxs-lookup"><span data-stu-id="87cde-108">Element</span></span>                                                           | <span data-ttu-id="87cde-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="87cde-109">Derived from</span></span>                                                         | <span data-ttu-id="87cde-110">Description</span><span class="sxs-lookup"><span data-stu-id="87cde-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="87cde-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="87cde-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="87cde-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="87cde-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="87cde-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="87cde-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="87cde-114">備註</span><span class="sxs-lookup"><span data-stu-id="87cde-114">Remarks</span></span>

<span data-ttu-id="87cde-115">優先權層級0是最高優先順序，而優先順序層級10是最低優先順序。</span><span class="sxs-lookup"><span data-stu-id="87cde-115">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="87cde-116">預設值為 7。</span><span class="sxs-lookup"><span data-stu-id="87cde-116">The default value is 7.</span></span> <span data-ttu-id="87cde-117">最小值和最大值是由 [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) 簡單類型所設定。</span><span class="sxs-lookup"><span data-stu-id="87cde-117">The minimum and maximum values are set by the [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) simple type.</span></span> <span data-ttu-id="87cde-118">優先權層級7和8用於背景工作，而優先順序層級4、5和6則用於互動式工作。</span><span class="sxs-lookup"><span data-stu-id="87cde-118">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="87cde-119">工作的動作會在具有以優先權類別值為基礎之優先權的進程中啟動。</span><span class="sxs-lookup"><span data-stu-id="87cde-119">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="87cde-120">優先權層級值 (執行緒優先順序) 用於 COM 處理常式、訊息方塊，以及電子郵件工作動作。</span><span class="sxs-lookup"><span data-stu-id="87cde-120">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="87cde-121">如需優先順序類別和優先權層級值的詳細資訊，請參閱 [排程優先順序](/windows/desktop/ProcThread/scheduling-priorities)。</span><span class="sxs-lookup"><span data-stu-id="87cde-121">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="87cde-122">下表列出 **priority** 元素的可能值，以及對應的 priority 類別和優先權層級值。</span><span class="sxs-lookup"><span data-stu-id="87cde-122">The following table lists the possible values for the **Priority** element, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="87cde-123">工作優先順序</span><span class="sxs-lookup"><span data-stu-id="87cde-123">Task Priority</span></span> | <span data-ttu-id="87cde-124">Priority 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-124">Priority Class</span></span>                 | <span data-ttu-id="87cde-125">優先權層級</span><span class="sxs-lookup"><span data-stu-id="87cde-125">Priority Level</span></span>                   |
|---------------|--------------------------------|----------------------------------|
| <span data-ttu-id="87cde-126">0</span><span class="sxs-lookup"><span data-stu-id="87cde-126">0</span></span>             | <span data-ttu-id="87cde-127">即時 \_ 優先權 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-127">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="87cde-128">執行緒 \_ 優先順序 \_ 時間 \_ 嚴重不足</span><span class="sxs-lookup"><span data-stu-id="87cde-128">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="87cde-129">1</span><span class="sxs-lookup"><span data-stu-id="87cde-129">1</span></span>             | <span data-ttu-id="87cde-130">高 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-130">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="87cde-131">執行緒 \_ 優先順序 \_ 最高</span><span class="sxs-lookup"><span data-stu-id="87cde-131">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="87cde-132">2</span><span class="sxs-lookup"><span data-stu-id="87cde-132">2</span></span>             | <span data-ttu-id="87cde-133">高於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-133">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="87cde-134">\_ \_ 高於 \_ 一般的執行緒優先順序</span><span class="sxs-lookup"><span data-stu-id="87cde-134">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="87cde-135">3</span><span class="sxs-lookup"><span data-stu-id="87cde-135">3</span></span>             | <span data-ttu-id="87cde-136">高於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-136">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="87cde-137">\_ \_ 高於 \_ 一般的執行緒優先順序</span><span class="sxs-lookup"><span data-stu-id="87cde-137">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="87cde-138">4</span><span class="sxs-lookup"><span data-stu-id="87cde-138">4</span></span>             | <span data-ttu-id="87cde-139">一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-139">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="87cde-140">執行緒 \_ 優先順序 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="87cde-140">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="87cde-141">5</span><span class="sxs-lookup"><span data-stu-id="87cde-141">5</span></span>             | <span data-ttu-id="87cde-142">一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-142">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="87cde-143">執行緒 \_ 優先順序 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="87cde-143">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="87cde-144">6</span><span class="sxs-lookup"><span data-stu-id="87cde-144">6</span></span>             | <span data-ttu-id="87cde-145">一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-145">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="87cde-146">執行緒 \_ 優先順序 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="87cde-146">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="87cde-147">7</span><span class="sxs-lookup"><span data-stu-id="87cde-147">7</span></span>             | <span data-ttu-id="87cde-148">低於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-148">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="87cde-149">一般的執行緒 \_ 優先順序 \_ \_</span><span class="sxs-lookup"><span data-stu-id="87cde-149">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="87cde-150">8</span><span class="sxs-lookup"><span data-stu-id="87cde-150">8</span></span>             | <span data-ttu-id="87cde-151">低於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-151">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="87cde-152">一般的執行緒 \_ 優先順序 \_ \_</span><span class="sxs-lookup"><span data-stu-id="87cde-152">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="87cde-153">9</span><span class="sxs-lookup"><span data-stu-id="87cde-153">9</span></span>             | <span data-ttu-id="87cde-154">閒置 \_ 優先權 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-154">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="87cde-155">執行緒 \_ 優先順序 \_ 最低</span><span class="sxs-lookup"><span data-stu-id="87cde-155">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="87cde-156">10</span><span class="sxs-lookup"><span data-stu-id="87cde-156">10</span></span>            | <span data-ttu-id="87cde-157">閒置 \_ 優先權 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="87cde-157">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="87cde-158">執行緒 \_ 優先順序 \_ 閒置</span><span class="sxs-lookup"><span data-stu-id="87cde-158">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="87cde-159">針對 c + + 開發，請參閱 [**ITaskSettings 的 Priority 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority)。</span><span class="sxs-lookup"><span data-stu-id="87cde-159">For C++ development, see [**Priority Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span></span>

<span data-ttu-id="87cde-160">如需腳本開發，請參閱 [**TaskSettings。**](tasksettings-priority.md)</span><span class="sxs-lookup"><span data-stu-id="87cde-160">For script development, see [**TaskSettings.Priority**](tasksettings-priority.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87cde-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="87cde-161">Requirements</span></span>



| <span data-ttu-id="87cde-162">需求</span><span class="sxs-lookup"><span data-stu-id="87cde-162">Requirement</span></span> | <span data-ttu-id="87cde-163">值</span><span class="sxs-lookup"><span data-stu-id="87cde-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87cde-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87cde-164">Minimum supported client</span></span><br/> | <span data-ttu-id="87cde-165">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87cde-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87cde-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87cde-166">Minimum supported server</span></span><br/> | <span data-ttu-id="87cde-167">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87cde-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87cde-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87cde-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cde-169">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="87cde-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

