---
title: RegistrationTrigger 物件
description: 代表觸發程式的腳本物件，此觸發程式會在工作註冊或更新時啟動工作。
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- 註冊觸發程式工作排程器，物件
- RegistrationTrigger 物件工作排程器
- RegistrationTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508776"
---
# <a name="registrationtrigger-object"></a><span data-ttu-id="8de95-106">RegistrationTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="8de95-106">RegistrationTrigger object</span></span>

<span data-ttu-id="8de95-107">代表觸發程式的腳本物件，此觸發程式會在工作註冊或更新時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="8de95-107">Scripting object that represents a trigger that starts a task when the task is registered or updated.</span></span>

## <a name="members"></a><span data-ttu-id="8de95-108">成員</span><span class="sxs-lookup"><span data-stu-id="8de95-108">Members</span></span>

<span data-ttu-id="8de95-109">**RegistrationTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8de95-109">The **RegistrationTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="8de95-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8de95-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8de95-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8de95-111">Properties</span></span>

<span data-ttu-id="8de95-112">**RegistrationTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8de95-112">The **RegistrationTrigger** object has these properties.</span></span>



| <span data-ttu-id="8de95-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8de95-113">Property</span></span>                                                            | <span data-ttu-id="8de95-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="8de95-114">Access type</span></span>           | <span data-ttu-id="8de95-115">Description</span><span class="sxs-lookup"><span data-stu-id="8de95-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8de95-116">**延遲**</span><span class="sxs-lookup"><span data-stu-id="8de95-116">**Delay**</span></span>](registrationtrigger-delay.md)<br/>               | <span data-ttu-id="8de95-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8de95-117">Read/write</span></span><br/> | <span data-ttu-id="8de95-118">取得或設定工作的註冊時間與工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="8de95-118">Gets or sets the amount of time between when the task is registered and when the task is started.</span></span><br/>                                                                                |
| [<span data-ttu-id="8de95-119">**啟用**</span><span class="sxs-lookup"><span data-stu-id="8de95-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="8de95-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8de95-120">Read/write</span></span><br/> | <span data-ttu-id="8de95-121">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="8de95-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="8de95-122">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8de95-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="8de95-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="8de95-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="8de95-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8de95-124">Read/write</span></span><br/> | <span data-ttu-id="8de95-125">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="8de95-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="8de95-126">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8de95-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="8de95-127">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="8de95-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="8de95-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="8de95-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="8de95-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8de95-129">Read/write</span></span><br/> | <span data-ttu-id="8de95-130">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="8de95-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="8de95-131">取得或設定允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="8de95-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="8de95-132">**Id**</span><span class="sxs-lookup"><span data-stu-id="8de95-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="8de95-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8de95-133">Read/write</span></span><br/> | <span data-ttu-id="8de95-134">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="8de95-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="8de95-135">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8de95-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="8de95-136">**重複**</span><span class="sxs-lookup"><span data-stu-id="8de95-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="8de95-137">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8de95-137">Read/write</span></span><br/> | <span data-ttu-id="8de95-138">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="8de95-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="8de95-139">取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="8de95-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="8de95-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="8de95-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="8de95-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8de95-141">Read/write</span></span><br/> | <span data-ttu-id="8de95-142">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="8de95-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="8de95-143">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8de95-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="8de95-144">**類型**</span><span class="sxs-lookup"><span data-stu-id="8de95-144">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="8de95-145">唯讀</span><span class="sxs-lookup"><span data-stu-id="8de95-145">Read-only</span></span><br/>  | <span data-ttu-id="8de95-146">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="8de95-146">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="8de95-147">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="8de95-147">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="8de95-148">備註</span><span class="sxs-lookup"><span data-stu-id="8de95-148">Remarks</span></span>

<span data-ttu-id="8de95-149">當您為工作建立自己的 XML 時，會使用工作排程器架構的 [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) 元素來指定註冊觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8de95-149">When creating your own XML for a task, a registration trigger is specified using the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="8de95-150">如果註冊了具有延遲註冊觸發程式的工作，且在延遲期間關閉或重新開機工作的電腦，在執行工作之前，工作將不會執行，而且會遺失延遲。</span><span class="sxs-lookup"><span data-stu-id="8de95-150">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="examples"></a><span data-ttu-id="8de95-151">範例</span><span class="sxs-lookup"><span data-stu-id="8de95-151">Examples</span></span>

<span data-ttu-id="8de95-152">如需此腳本物件的詳細資訊和程式碼範例，請參閱 [ (腳本) 的註冊觸發程式範例 ](registration-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="8de95-152">For more information and a code example for this scripting object, see [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8de95-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="8de95-153">Requirements</span></span>



| <span data-ttu-id="8de95-154">需求</span><span class="sxs-lookup"><span data-stu-id="8de95-154">Requirement</span></span> | <span data-ttu-id="8de95-155">值</span><span class="sxs-lookup"><span data-stu-id="8de95-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8de95-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8de95-156">Minimum supported client</span></span><br/> | <span data-ttu-id="8de95-157">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8de95-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8de95-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8de95-158">Minimum supported server</span></span><br/> | <span data-ttu-id="8de95-159">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8de95-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8de95-160">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8de95-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="8de95-161"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8de95-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8de95-162">DLL</span><span class="sxs-lookup"><span data-stu-id="8de95-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8de95-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8de95-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8de95-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8de95-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de95-165">**觸發**</span><span class="sxs-lookup"><span data-stu-id="8de95-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="8de95-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="8de95-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="8de95-167">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="8de95-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





