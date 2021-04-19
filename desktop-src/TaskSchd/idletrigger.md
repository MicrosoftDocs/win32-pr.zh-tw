---
title: IdleTrigger 物件
description: 代表觸發程式的腳本物件，此觸發程式會在發生閒置條件時啟動工作。
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- 閒置觸發程式工作排程器，物件
- IdleTrigger 物件工作排程器
- IdleTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106988038"
---
# <a name="idletrigger-object"></a><span data-ttu-id="bec9c-106">IdleTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="bec9c-106">IdleTrigger object</span></span>

<span data-ttu-id="bec9c-107">代表觸發程式的腳本物件，此觸發程式會在發生閒置條件時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="bec9c-107">Scripting object that represents a trigger that starts a task when an idle condition occurs.</span></span> <span data-ttu-id="bec9c-108">如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。</span><span class="sxs-lookup"><span data-stu-id="bec9c-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="bec9c-109">成員</span><span class="sxs-lookup"><span data-stu-id="bec9c-109">Members</span></span>

<span data-ttu-id="bec9c-110">**IdleTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bec9c-110">The **IdleTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="bec9c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bec9c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bec9c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="bec9c-112">Properties</span></span>

<span data-ttu-id="bec9c-113">**IdleTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bec9c-113">The **IdleTrigger** object has these properties.</span></span>



| <span data-ttu-id="bec9c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="bec9c-114">Property</span></span>                                                            | <span data-ttu-id="bec9c-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="bec9c-115">Access type</span></span>           | <span data-ttu-id="bec9c-116">Description</span><span class="sxs-lookup"><span data-stu-id="bec9c-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bec9c-117">**已啟用**</span><span class="sxs-lookup"><span data-stu-id="bec9c-117">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="bec9c-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bec9c-118">Read/write</span></span><br/> | <span data-ttu-id="bec9c-119">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="bec9c-119">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="bec9c-120">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="bec9c-120">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="bec9c-121">EndBoundary</span><span class="sxs-lookup"><span data-stu-id="bec9c-121">EndBoundary</span></span>](trigger-endboundary.md)<br/>                   | <span data-ttu-id="bec9c-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bec9c-122">Read/write</span></span><br/> | <span data-ttu-id="bec9c-123">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="bec9c-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="bec9c-124">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="bec9c-124">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="bec9c-125">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="bec9c-125">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="bec9c-126">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="bec9c-126">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="bec9c-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bec9c-127">Read/write</span></span><br/> | <span data-ttu-id="bec9c-128">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="bec9c-128">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="bec9c-129">取得或設定觸發程式可啟動工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="bec9c-129">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="bec9c-130">**Id**</span><span class="sxs-lookup"><span data-stu-id="bec9c-130">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="bec9c-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bec9c-131">Read/write</span></span><br/> | <span data-ttu-id="bec9c-132">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="bec9c-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="bec9c-133">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bec9c-133">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="bec9c-134">**重複**</span><span class="sxs-lookup"><span data-stu-id="bec9c-134">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="bec9c-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bec9c-135">Read/write</span></span><br/> | <span data-ttu-id="bec9c-136">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="bec9c-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="bec9c-137">取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="bec9c-137">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="bec9c-138">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="bec9c-138">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="bec9c-139">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bec9c-139">Read/write</span></span><br/> | <span data-ttu-id="bec9c-140">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="bec9c-140">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="bec9c-141">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="bec9c-141">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="bec9c-142">**類型**</span><span class="sxs-lookup"><span data-stu-id="bec9c-142">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="bec9c-143">唯讀</span><span class="sxs-lookup"><span data-stu-id="bec9c-143">Read-only</span></span><br/>  | <span data-ttu-id="bec9c-144">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="bec9c-144">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="bec9c-145">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="bec9c-145">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="bec9c-146">備註</span><span class="sxs-lookup"><span data-stu-id="bec9c-146">Remarks</span></span>

<span data-ttu-id="bec9c-147">閒置觸發程式只會在觸發程式啟動界限後進入閒置狀態時，才會觸發工作動作。</span><span class="sxs-lookup"><span data-stu-id="bec9c-147">An idle trigger will only trigger a task action if the computer goes into an idle state after the start boundary of the trigger.</span></span>

<span data-ttu-id="bec9c-148">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) 元素來指定閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="bec9c-148">When reading or writing XML for a task, an idle trigger is specified using the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="bec9c-149">如果工作是由閒置觸發程式觸發，則會忽略 [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="bec9c-149">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

<span data-ttu-id="bec9c-150">如果具有閒置觸發程式之工作的初始實例仍在執行中，則工作只會在沒有重複的情況下啟動一次，即使在 [ [**重複**](trigger-repetition.md) ] 屬性中定義了多個重複。</span><span class="sxs-lookup"><span data-stu-id="bec9c-150">If the initial instance of a task with an idle trigger is still running, then the task is only launched once with no repetitions, even if multiple repetition is defined in the [**Repetition**](trigger-repetition.md) property.</span></span> <span data-ttu-id="bec9c-151">如果工作本身停止，則不會發生此行為。</span><span class="sxs-lookup"><span data-stu-id="bec9c-151">This behavior does not occur if the task stops by itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="bec9c-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="bec9c-152">Requirements</span></span>



| <span data-ttu-id="bec9c-153">需求</span><span class="sxs-lookup"><span data-stu-id="bec9c-153">Requirement</span></span> | <span data-ttu-id="bec9c-154">值</span><span class="sxs-lookup"><span data-stu-id="bec9c-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bec9c-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bec9c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="bec9c-156">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bec9c-156">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bec9c-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bec9c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="bec9c-158">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bec9c-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bec9c-159">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bec9c-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="bec9c-160"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bec9c-160"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bec9c-161">DLL</span><span class="sxs-lookup"><span data-stu-id="bec9c-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bec9c-162"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bec9c-162"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bec9c-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bec9c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec9c-164">**觸發**</span><span class="sxs-lookup"><span data-stu-id="bec9c-164">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="bec9c-165">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="bec9c-165">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="bec9c-166">工作排程器</span><span class="sxs-lookup"><span data-stu-id="bec9c-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





