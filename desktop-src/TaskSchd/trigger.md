---
title: 觸發程式物件
description: 提供所有觸發程式物件所繼承之通用屬性的腳本物件。
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- 觸發程式工作排程器，觸發程式物件
- 觸發程式物件工作排程器
- 觸發物件工作排程器，說明
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843316"
---
# <a name="trigger-object"></a><span data-ttu-id="352a4-106">觸發程式物件</span><span class="sxs-lookup"><span data-stu-id="352a4-106">Trigger object</span></span>

<span data-ttu-id="352a4-107">提供所有觸發程式物件所繼承之通用屬性的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="352a4-107">Scripting object that provides the common properties that are inherited by all trigger objects.</span></span>

## <a name="members"></a><span data-ttu-id="352a4-108">成員</span><span class="sxs-lookup"><span data-stu-id="352a4-108">Members</span></span>

<span data-ttu-id="352a4-109">**觸發** 程式物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="352a4-109">The **Trigger** object has these types of members:</span></span>

-   [<span data-ttu-id="352a4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="352a4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="352a4-111">屬性</span><span class="sxs-lookup"><span data-stu-id="352a4-111">Properties</span></span>

<span data-ttu-id="352a4-112">**觸發** 程式物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="352a4-112">The **Trigger** object has these properties.</span></span>



| <span data-ttu-id="352a4-113">屬性</span><span class="sxs-lookup"><span data-stu-id="352a4-113">Property</span></span>                                                            | <span data-ttu-id="352a4-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="352a4-114">Access type</span></span>           | <span data-ttu-id="352a4-115">Description</span><span class="sxs-lookup"><span data-stu-id="352a4-115">Description</span></span>                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="352a4-116">**已啟用**</span><span class="sxs-lookup"><span data-stu-id="352a4-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="352a4-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="352a4-117">Read/write</span></span><br/> | <span data-ttu-id="352a4-118">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="352a4-118">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="352a4-119">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="352a4-119">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="352a4-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="352a4-120">Read/write</span></span><br/> | <span data-ttu-id="352a4-121">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="352a4-121">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="352a4-122">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="352a4-122">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="352a4-123">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="352a4-123">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="352a4-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="352a4-124">Read/write</span></span><br/> | <span data-ttu-id="352a4-125">取得或設定允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="352a4-125">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="352a4-126">**Id**</span><span class="sxs-lookup"><span data-stu-id="352a4-126">**Id**</span></span>](trigger-id.md)<br/>                                 | <span data-ttu-id="352a4-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="352a4-127">Read/write</span></span><br/> | <span data-ttu-id="352a4-128">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="352a4-128">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="352a4-129">**重複**</span><span class="sxs-lookup"><span data-stu-id="352a4-129">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="352a4-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="352a4-130">Read/write</span></span><br/> | <span data-ttu-id="352a4-131">取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="352a4-131">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="352a4-132">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="352a4-132">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="352a4-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="352a4-133">Read/write</span></span><br/> | <span data-ttu-id="352a4-134">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="352a4-134">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="352a4-135">觸發程式可以在啟動觸發程式之後啟動工作。</span><span class="sxs-lookup"><span data-stu-id="352a4-135">The trigger can start the task after the trigger is activated.</span></span><br/>             |
| [<span data-ttu-id="352a4-136">**類型**</span><span class="sxs-lookup"><span data-stu-id="352a4-136">**Type**</span></span>](trigger-type.md)<br/>                             |                       | <span data-ttu-id="352a4-137">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="352a4-137">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="352a4-138">備註</span><span class="sxs-lookup"><span data-stu-id="352a4-138">Remarks</span></span>

<span data-ttu-id="352a4-139">工作排程器針對工作可使用的不同觸發程式提供下列個別物件：</span><span class="sxs-lookup"><span data-stu-id="352a4-139">The Task Scheduler provides the following individual objects for the different triggers that a task can use:</span></span>

-   [<span data-ttu-id="352a4-140">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-140">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="352a4-141">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-141">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="352a4-142">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-142">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="352a4-143">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-143">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="352a4-144">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-144">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="352a4-145">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-145">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="352a4-146">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-146">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="352a4-147">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-147">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="352a4-148">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-148">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="352a4-149">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-149">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="352a4-150">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="352a4-150">**SessionStateChangeTrigger**</span></span>](sessionstatechangetrigger.md)

<span data-ttu-id="352a4-151">讀取或寫入 XML 時，工作的觸發程式會在工作排程器架構的 [**trigger**](taskschedulerschema-triggers-tasktype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="352a4-151">When reading or writing XML, the triggers of a task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="352a4-152">範例</span><span class="sxs-lookup"><span data-stu-id="352a4-152">Examples</span></span>

<span data-ttu-id="352a4-153">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="352a4-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="352a4-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="352a4-154">Requirements</span></span>



| <span data-ttu-id="352a4-155">需求</span><span class="sxs-lookup"><span data-stu-id="352a4-155">Requirement</span></span> | <span data-ttu-id="352a4-156">值</span><span class="sxs-lookup"><span data-stu-id="352a4-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="352a4-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="352a4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="352a4-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="352a4-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="352a4-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="352a4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="352a4-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="352a4-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="352a4-161">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="352a4-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="352a4-162"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="352a4-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="352a4-163">DLL</span><span class="sxs-lookup"><span data-stu-id="352a4-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="352a4-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="352a4-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="352a4-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="352a4-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352a4-166">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="352a4-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> </dl>

 

 





