---
title: SessionStateChangeTrigger 物件
description: 腳本物件，可觸發主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知的工作。
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- SessionStateChangeTrigger 物件工作排程器
- SessionStateChangeTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995162"
---
# <a name="sessionstatechangetrigger-object"></a><span data-ttu-id="682bd-105">SessionStateChangeTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="682bd-105">SessionStateChangeTrigger object</span></span>

<span data-ttu-id="682bd-106">腳本物件，可觸發主控台連線或中斷連線、遠端連線或中斷連線，或工作站鎖定或解除鎖定通知的工作。</span><span class="sxs-lookup"><span data-stu-id="682bd-106">Scripting object that triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

## <a name="members"></a><span data-ttu-id="682bd-107">成員</span><span class="sxs-lookup"><span data-stu-id="682bd-107">Members</span></span>

<span data-ttu-id="682bd-108">**SessionStateChangeTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="682bd-108">The **SessionStateChangeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="682bd-109">屬性</span><span class="sxs-lookup"><span data-stu-id="682bd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="682bd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="682bd-110">Properties</span></span>

<span data-ttu-id="682bd-111">**SessionStateChangeTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="682bd-111">The **SessionStateChangeTrigger** object has these properties.</span></span>



| <span data-ttu-id="682bd-112">屬性</span><span class="sxs-lookup"><span data-stu-id="682bd-112">Property</span></span>                                                                | <span data-ttu-id="682bd-113">存取類型</span><span class="sxs-lookup"><span data-stu-id="682bd-113">Access type</span></span>           | <span data-ttu-id="682bd-114">Description</span><span class="sxs-lookup"><span data-stu-id="682bd-114">Description</span></span>                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="682bd-115">**延遲**</span><span class="sxs-lookup"><span data-stu-id="682bd-115">**Delay**</span></span>](sessionstatechangetrigger-delay.md)<br/>             | <span data-ttu-id="682bd-116">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="682bd-116">Read/write</span></span><br/> | <span data-ttu-id="682bd-117">取得或設定值，這個值表示偵測到終端機伺服器會話狀態變更之後，啟動工作之前的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="682bd-117">Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span><br/>                                         |
| [<span data-ttu-id="682bd-118">**啟用**</span><span class="sxs-lookup"><span data-stu-id="682bd-118">**Enabled**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | <span data-ttu-id="682bd-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="682bd-119">Read/write</span></span><br/> | <span data-ttu-id="682bd-120">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="682bd-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="682bd-121">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="682bd-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="682bd-122">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="682bd-122">**EndBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | <span data-ttu-id="682bd-123">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="682bd-123">Read/write</span></span><br/> | <span data-ttu-id="682bd-124">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="682bd-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="682bd-125">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="682bd-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="682bd-126">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="682bd-126">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="682bd-127">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="682bd-127">**ExecutionTimeLimit**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | <span data-ttu-id="682bd-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="682bd-128">Read/write</span></span><br/> | <span data-ttu-id="682bd-129">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="682bd-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="682bd-130">取得或設定觸發程式可啟動工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="682bd-130">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="682bd-131">**Id**</span><span class="sxs-lookup"><span data-stu-id="682bd-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | <span data-ttu-id="682bd-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="682bd-132">Read/write</span></span><br/> | <span data-ttu-id="682bd-133">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="682bd-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="682bd-134">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="682bd-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="682bd-135">**重複**</span><span class="sxs-lookup"><span data-stu-id="682bd-135">**Repetition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | <span data-ttu-id="682bd-136">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="682bd-136">Read/write</span></span><br/> | <span data-ttu-id="682bd-137">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="682bd-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="682bd-138">取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="682bd-138">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="682bd-139">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="682bd-139">**StartBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | <span data-ttu-id="682bd-140">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="682bd-140">Read/write</span></span><br/> | <span data-ttu-id="682bd-141">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="682bd-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="682bd-142">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="682bd-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="682bd-143">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="682bd-143">**StateChange**</span></span>](sessionstatechangetrigger-statechange.md)<br/> | <span data-ttu-id="682bd-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="682bd-144">Read/write</span></span><br/> | <span data-ttu-id="682bd-145">取得或設定會觸發工作啟動的終端機伺服器會話變更類型。</span><span class="sxs-lookup"><span data-stu-id="682bd-145">Gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="682bd-146">**類型**</span><span class="sxs-lookup"><span data-stu-id="682bd-146">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | <span data-ttu-id="682bd-147">唯讀</span><span class="sxs-lookup"><span data-stu-id="682bd-147">Read-only</span></span><br/>  | <span data-ttu-id="682bd-148">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="682bd-148">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="682bd-149">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="682bd-149">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="682bd-150">**UserId**</span><span class="sxs-lookup"><span data-stu-id="682bd-150">**UserId**</span></span>](sessionstatechangetrigger-userid.md)<br/>           | <span data-ttu-id="682bd-151">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="682bd-151">Read/write</span></span><br/> | <span data-ttu-id="682bd-152">取得或設定終端機伺服器會話的使用者。</span><span class="sxs-lookup"><span data-stu-id="682bd-152">Gets or sets the user for the Terminal Server session.</span></span> <span data-ttu-id="682bd-153">當偵測到此使用者的會話狀態變更時，就會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="682bd-153">When a session state change is detected for this user, a task is started.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="682bd-154">備註</span><span class="sxs-lookup"><span data-stu-id="682bd-154">Remarks</span></span>

<span data-ttu-id="682bd-155">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) 元素來指定會話狀態變更觸發程式。</span><span class="sxs-lookup"><span data-stu-id="682bd-155">When reading or writing your own XML for a task, a session state change trigger is specified using the [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="682bd-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="682bd-156">Requirements</span></span>



| <span data-ttu-id="682bd-157">需求</span><span class="sxs-lookup"><span data-stu-id="682bd-157">Requirement</span></span> | <span data-ttu-id="682bd-158">值</span><span class="sxs-lookup"><span data-stu-id="682bd-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="682bd-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="682bd-159">Minimum supported client</span></span><br/> | <span data-ttu-id="682bd-160">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="682bd-160">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="682bd-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="682bd-161">Minimum supported server</span></span><br/> | <span data-ttu-id="682bd-162">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="682bd-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="682bd-163">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="682bd-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="682bd-164"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="682bd-164"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="682bd-165">DLL</span><span class="sxs-lookup"><span data-stu-id="682bd-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="682bd-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="682bd-166"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="682bd-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="682bd-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="682bd-168">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="682bd-168">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="682bd-169">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="682bd-169">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





