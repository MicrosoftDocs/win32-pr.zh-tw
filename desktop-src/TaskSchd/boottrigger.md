---
title: BootTrigger 物件
description: 代表觸發程式的腳本物件，此觸發程式會在系統啟動時啟動工作。
ms.assetid: 9d5a7cf6-2e1d-44ae-bb45-66424770d61b
keywords:
- 啟動觸發程式工作排程器，物件
- BootTrigger 物件工作排程器
- BootTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- BootTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346a4bc7b20606f59c26b131590b92593d40d07e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466992"
---
# <a name="boottrigger-object"></a><span data-ttu-id="6b796-106">BootTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="6b796-106">BootTrigger object</span></span>

<span data-ttu-id="6b796-107">代表觸發程式的腳本物件，此觸發程式會在系統啟動時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="6b796-107">Scripting object that represents a trigger that starts a task when the system is booted.</span></span>

## <a name="members"></a><span data-ttu-id="6b796-108">成員</span><span class="sxs-lookup"><span data-stu-id="6b796-108">Members</span></span>

<span data-ttu-id="6b796-109">**BootTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6b796-109">The **BootTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="6b796-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6b796-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b796-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6b796-111">Properties</span></span>

<span data-ttu-id="6b796-112">**BootTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6b796-112">The **BootTrigger** object has these properties.</span></span>



| <span data-ttu-id="6b796-113">屬性</span><span class="sxs-lookup"><span data-stu-id="6b796-113">Property</span></span>                                                            | <span data-ttu-id="6b796-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="6b796-114">Access type</span></span>           | <span data-ttu-id="6b796-115">Description</span><span class="sxs-lookup"><span data-stu-id="6b796-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b796-116">**延遲**</span><span class="sxs-lookup"><span data-stu-id="6b796-116">**Delay**</span></span>](boottrigger-delay.md)<br/>                       |                       | <span data-ttu-id="6b796-117">取得或設定值，這個值表示系統開機和啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="6b796-117">Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span><br/>                                                           |
| [<span data-ttu-id="6b796-118">**啟用**</span><span class="sxs-lookup"><span data-stu-id="6b796-118">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="6b796-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6b796-119">Read/write</span></span><br/> | <span data-ttu-id="6b796-120">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="6b796-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6b796-121">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6b796-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="6b796-122">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="6b796-122">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="6b796-123">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6b796-123">Read/write</span></span><br/> | <span data-ttu-id="6b796-124">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="6b796-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6b796-125">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6b796-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="6b796-126">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="6b796-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="6b796-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="6b796-127">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="6b796-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6b796-128">Read/write</span></span><br/> | <span data-ttu-id="6b796-129">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="6b796-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6b796-130">取得或設定允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="6b796-130">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="6b796-131">**Id**</span><span class="sxs-lookup"><span data-stu-id="6b796-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="6b796-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6b796-132">Read/write</span></span><br/> | <span data-ttu-id="6b796-133">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="6b796-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6b796-134">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b796-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="6b796-135">**重複**</span><span class="sxs-lookup"><span data-stu-id="6b796-135">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="6b796-136">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6b796-136">Read/write</span></span><br/> | <span data-ttu-id="6b796-137">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="6b796-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6b796-138">取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="6b796-138">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="6b796-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="6b796-139">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="6b796-140">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6b796-140">Read/write</span></span><br/> | <span data-ttu-id="6b796-141">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="6b796-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6b796-142">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6b796-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="6b796-143">**類型**</span><span class="sxs-lookup"><span data-stu-id="6b796-143">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="6b796-144">唯讀</span><span class="sxs-lookup"><span data-stu-id="6b796-144">Read-only</span></span><br/>  | <span data-ttu-id="6b796-145">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="6b796-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="6b796-146">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="6b796-146">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="6b796-147">備註</span><span class="sxs-lookup"><span data-stu-id="6b796-147">Remarks</span></span>

<span data-ttu-id="6b796-148">啟動作業系統時，會啟動工作排程器服務，啟動觸發程式工作則會在工作排程器服務啟動時設定為 [啟動]。</span><span class="sxs-lookup"><span data-stu-id="6b796-148">The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.</span></span>

<span data-ttu-id="6b796-149">只有 Administrators 群組的成員可以建立具有開機觸發程式的工作。</span><span class="sxs-lookup"><span data-stu-id="6b796-149">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="6b796-150">當您為工作建立自己的 XML 時，會使用工作排程器架構的 [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) 元素來指定開機觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6b796-150">When creating your own XML for a task, a boot trigger is specified using the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="6b796-151">範例</span><span class="sxs-lookup"><span data-stu-id="6b796-151">Examples</span></span>

<span data-ttu-id="6b796-152">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [ (腳本) 的開機觸發程式範例 ](boot-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="6b796-152">For more information and example code for this scripting object, see [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b796-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b796-153">Requirements</span></span>



| <span data-ttu-id="6b796-154">需求</span><span class="sxs-lookup"><span data-stu-id="6b796-154">Requirement</span></span> | <span data-ttu-id="6b796-155">值</span><span class="sxs-lookup"><span data-stu-id="6b796-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b796-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b796-156">Minimum supported client</span></span><br/> | <span data-ttu-id="6b796-157">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b796-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6b796-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b796-158">Minimum supported server</span></span><br/> | <span data-ttu-id="6b796-159">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b796-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b796-160">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6b796-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b796-161"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b796-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b796-162">DLL</span><span class="sxs-lookup"><span data-stu-id="6b796-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b796-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b796-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b796-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b796-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b796-165">**觸發**</span><span class="sxs-lookup"><span data-stu-id="6b796-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="6b796-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="6b796-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="6b796-167">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="6b796-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





