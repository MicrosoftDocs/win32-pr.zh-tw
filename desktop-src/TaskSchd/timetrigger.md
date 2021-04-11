---
title: 'TimeTrigger 物件 (Windows. applicationmodel) '
description: 代表觸發程式的腳本物件，此觸發程式會在特定的日期和時間啟動工作。
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- 時間觸發程式工作排程器，物件
- TimeTrigger 物件工作排程器
- TimeTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317328"
---
# <a name="timetrigger-object"></a><span data-ttu-id="8d928-106">TimeTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="8d928-106">TimeTrigger object</span></span>

<span data-ttu-id="8d928-107">代表觸發程式的腳本物件，此觸發程式會在特定的日期和時間啟動工作。</span><span class="sxs-lookup"><span data-stu-id="8d928-107">Scripting object that represents a trigger that starts a task at a specific date and time.</span></span>

## <a name="members"></a><span data-ttu-id="8d928-108">成員</span><span class="sxs-lookup"><span data-stu-id="8d928-108">Members</span></span>

<span data-ttu-id="8d928-109">**TimeTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8d928-109">The **TimeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="8d928-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8d928-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d928-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8d928-111">Properties</span></span>

<span data-ttu-id="8d928-112">**TimeTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8d928-112">The **TimeTrigger** object has these properties.</span></span>



| <span data-ttu-id="8d928-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8d928-113">Property</span></span>                                                            | <span data-ttu-id="8d928-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="8d928-114">Access type</span></span>           | <span data-ttu-id="8d928-115">Description</span><span class="sxs-lookup"><span data-stu-id="8d928-115">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d928-116">**已啟用**</span><span class="sxs-lookup"><span data-stu-id="8d928-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="8d928-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d928-117">Read/write</span></span><br/> | <span data-ttu-id="8d928-118">繼承自 [**觸發**](trigger.md)程式。</span><span class="sxs-lookup"><span data-stu-id="8d928-118">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="8d928-119">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8d928-119">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="8d928-120">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="8d928-120">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="8d928-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d928-121">Read/write</span></span><br/> | <span data-ttu-id="8d928-122">繼承自 [**觸發**](trigger.md)程式。</span><span class="sxs-lookup"><span data-stu-id="8d928-122">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="8d928-123">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8d928-123">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="8d928-124">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="8d928-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="8d928-125">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="8d928-125">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="8d928-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d928-126">Read/write</span></span><br/> | <span data-ttu-id="8d928-127">繼承自 [**觸發**](trigger.md)程式。</span><span class="sxs-lookup"><span data-stu-id="8d928-127">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="8d928-128">取得或設定允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="8d928-128">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="8d928-129">**Id**</span><span class="sxs-lookup"><span data-stu-id="8d928-129">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="8d928-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d928-130">Read/write</span></span><br/> | <span data-ttu-id="8d928-131">繼承自 [**觸發**](trigger.md)程式。</span><span class="sxs-lookup"><span data-stu-id="8d928-131">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="8d928-132">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d928-132">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="8d928-133">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="8d928-133">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="8d928-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d928-134">Read/write</span></span><br/> | <span data-ttu-id="8d928-135">取得或設定隨機加入至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="8d928-135">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                    |
| [<span data-ttu-id="8d928-136">**重複**</span><span class="sxs-lookup"><span data-stu-id="8d928-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="8d928-137">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d928-137">Read/write</span></span><br/> | <span data-ttu-id="8d928-138">繼承自 [**觸發**](trigger.md)程式。</span><span class="sxs-lookup"><span data-stu-id="8d928-138">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="8d928-139">取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="8d928-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="8d928-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="8d928-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="8d928-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d928-141">Read/write</span></span><br/> | <span data-ttu-id="8d928-142">繼承自 [**觸發**](trigger.md)程式。</span><span class="sxs-lookup"><span data-stu-id="8d928-142">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="8d928-143">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8d928-143">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="8d928-144">這個元素是必要的。</span><span class="sxs-lookup"><span data-stu-id="8d928-144">This element is required.</span></span><br/>                                    |
| [<span data-ttu-id="8d928-145">**類型**</span><span class="sxs-lookup"><span data-stu-id="8d928-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="8d928-146">唯讀</span><span class="sxs-lookup"><span data-stu-id="8d928-146">Read-only</span></span><br/>  | <span data-ttu-id="8d928-147">繼承自 [**觸發**](trigger.md)程式。</span><span class="sxs-lookup"><span data-stu-id="8d928-147">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="8d928-148">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="8d928-148">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="8d928-149">備註</span><span class="sxs-lookup"><span data-stu-id="8d928-149">Remarks</span></span>

<span data-ttu-id="8d928-150">[**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是時間和行事曆觸發程式的必要元素， ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)和 [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)) 。</span><span class="sxs-lookup"><span data-stu-id="8d928-150">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="8d928-151">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) 元素來指定閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8d928-151">When reading or writing XML for a task, an idle trigger is specified using the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="8d928-152">範例</span><span class="sxs-lookup"><span data-stu-id="8d928-152">Examples</span></span>

<span data-ttu-id="8d928-153">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="8d928-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d928-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d928-154">Requirements</span></span>



| <span data-ttu-id="8d928-155">需求</span><span class="sxs-lookup"><span data-stu-id="8d928-155">Requirement</span></span> | <span data-ttu-id="8d928-156">值</span><span class="sxs-lookup"><span data-stu-id="8d928-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d928-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d928-157">Minimum supported client</span></span><br/> | <span data-ttu-id="8d928-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d928-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="8d928-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d928-159">Minimum supported server</span></span><br/> | <span data-ttu-id="8d928-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d928-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8d928-161">標頭</span><span class="sxs-lookup"><span data-stu-id="8d928-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d928-162"><dt>Applicationmodel.。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d928-162"><dt>Windows.applicationmodel.background.h</dt></span></span> </dl> |
| <span data-ttu-id="8d928-163">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8d928-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d928-164"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d928-164"><dt>Taskschd.tlb</dt></span></span> </dl>                          |
| <span data-ttu-id="8d928-165">DLL</span><span class="sxs-lookup"><span data-stu-id="8d928-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d928-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d928-166"><dt>Taskschd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8d928-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d928-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d928-168">**觸發**</span><span class="sxs-lookup"><span data-stu-id="8d928-168">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="8d928-169">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="8d928-169">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="8d928-170">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="8d928-170">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





