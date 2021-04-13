---
title: 'EventTrigger 物件 (]) '
description: 代表觸發程式的腳本物件，此觸發程式會在系統事件發生時啟動工作。
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- 事件觸發程式工作排程器，物件
- EventTrigger 物件工作排程器
- EventTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509127"
---
# <a name="eventtrigger-object"></a><span data-ttu-id="37f01-106">EventTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="37f01-106">EventTrigger object</span></span>

<span data-ttu-id="37f01-107">代表觸發程式的腳本物件，此觸發程式會在系統事件發生時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="37f01-107">Scripting object that represents a trigger that starts a task when a system event occurs.</span></span>

## <a name="members"></a><span data-ttu-id="37f01-108">成員</span><span class="sxs-lookup"><span data-stu-id="37f01-108">Members</span></span>

<span data-ttu-id="37f01-109">**EventTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="37f01-109">The **EventTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="37f01-110">屬性</span><span class="sxs-lookup"><span data-stu-id="37f01-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37f01-111">屬性</span><span class="sxs-lookup"><span data-stu-id="37f01-111">Properties</span></span>

<span data-ttu-id="37f01-112">**EventTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="37f01-112">The **EventTrigger** object has these properties.</span></span>



| <span data-ttu-id="37f01-113">屬性</span><span class="sxs-lookup"><span data-stu-id="37f01-113">Property</span></span>                                                            | <span data-ttu-id="37f01-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="37f01-114">Access type</span></span>           | <span data-ttu-id="37f01-115">Description</span><span class="sxs-lookup"><span data-stu-id="37f01-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37f01-116">**延遲**</span><span class="sxs-lookup"><span data-stu-id="37f01-116">**Delay**</span></span>](eventtrigger-delay.md)<br/>                      | <span data-ttu-id="37f01-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37f01-117">Read/write</span></span><br/> | <span data-ttu-id="37f01-118">取得或設定值，這個值表示發生事件的時間與啟動工作的時間之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="37f01-118">Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="37f01-119">**啟用**</span><span class="sxs-lookup"><span data-stu-id="37f01-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="37f01-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37f01-120">Read/write</span></span><br/> | <span data-ttu-id="37f01-121">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="37f01-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="37f01-122">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="37f01-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="37f01-123">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="37f01-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="37f01-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37f01-124">Read/write</span></span><br/> | <span data-ttu-id="37f01-125">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="37f01-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="37f01-126">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="37f01-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="37f01-127">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="37f01-127">The trigger cannot start the task after it is deactivated.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="37f01-128">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="37f01-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="37f01-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37f01-129">Read/write</span></span><br/> | <span data-ttu-id="37f01-130">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="37f01-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="37f01-131">取得或設定允許執行此觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="37f01-131">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                                                                                                                                                                                                                       |
| [<span data-ttu-id="37f01-132">**Id**</span><span class="sxs-lookup"><span data-stu-id="37f01-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="37f01-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37f01-133">Read/write</span></span><br/> | <span data-ttu-id="37f01-134">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="37f01-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="37f01-135">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37f01-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="37f01-136">**重複**</span><span class="sxs-lookup"><span data-stu-id="37f01-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="37f01-137">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37f01-137">Read/write</span></span><br/> | <span data-ttu-id="37f01-138">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="37f01-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="37f01-139">取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="37f01-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="37f01-140">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="37f01-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="37f01-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37f01-141">Read/write</span></span><br/> | <span data-ttu-id="37f01-142">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="37f01-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="37f01-143">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="37f01-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="37f01-144">**訂用帳戶**</span><span class="sxs-lookup"><span data-stu-id="37f01-144">**Subscription**</span></span>](eventtrigger-subscription.md)<br/>        | <span data-ttu-id="37f01-145">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37f01-145">Read/write</span></span><br/> | <span data-ttu-id="37f01-146">取得或設定 XPath 查詢字串，這個字串會識別引發觸發程式的事件。</span><span class="sxs-lookup"><span data-stu-id="37f01-146">Gets or sets the XPath query string that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="37f01-147">**類型**</span><span class="sxs-lookup"><span data-stu-id="37f01-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="37f01-148">唯讀</span><span class="sxs-lookup"><span data-stu-id="37f01-148">Read-only</span></span><br/>  | <span data-ttu-id="37f01-149">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="37f01-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="37f01-150">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="37f01-150">Gets the type of the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="37f01-151">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="37f01-151">**ValueQueries**</span></span>](eventtrigger-valuequeries.md)<br/>        | <span data-ttu-id="37f01-152">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37f01-152">Read/write</span></span><br/> | <span data-ttu-id="37f01-153">取得或設定已命名 XPath 查詢的集合。</span><span class="sxs-lookup"><span data-stu-id="37f01-153">Gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="37f01-154">集合中的每個查詢都會套用至 [**訂閱**](eventtrigger-subscription.md) 屬性中指定之訂閱查詢所傳回的最後一個相符事件 XML。</span><span class="sxs-lookup"><span data-stu-id="37f01-154">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span> <span data-ttu-id="37f01-155">查詢的名稱可以當做 [**ShowMessageAction**](showmessageaction.md) 動作訊息中的變數使用。</span><span class="sxs-lookup"><span data-stu-id="37f01-155">The name of the query can be used as a variable in the message of a [**ShowMessageAction**](showmessageaction.md) action.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37f01-156">備註</span><span class="sxs-lookup"><span data-stu-id="37f01-156">Remarks</span></span>

<span data-ttu-id="37f01-157">您可以建立最多500個具有事件訂閱的工作。</span><span class="sxs-lookup"><span data-stu-id="37f01-157">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="37f01-158">針對各種事件進行查詢的事件訂閱，可以用來觸發使用相同動作來回應所記錄事件的工作。</span><span class="sxs-lookup"><span data-stu-id="37f01-158">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="37f01-159">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) 元素來指定事件觸發程式。</span><span class="sxs-lookup"><span data-stu-id="37f01-159">When reading or writing your own XML for a task, an event trigger is specified using the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="37f01-160">範例</span><span class="sxs-lookup"><span data-stu-id="37f01-160">Examples</span></span>

<span data-ttu-id="37f01-161">如需此腳本物件的詳細資訊和程式碼範例，請參閱 [事件觸發程式範例 (腳本) ](/previous-versions//aa446887(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="37f01-161">For more information and a code example for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="37f01-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="37f01-162">Requirements</span></span>



| <span data-ttu-id="37f01-163">需求</span><span class="sxs-lookup"><span data-stu-id="37f01-163">Requirement</span></span> | <span data-ttu-id="37f01-164">值</span><span class="sxs-lookup"><span data-stu-id="37f01-164">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37f01-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37f01-165">Minimum supported client</span></span><br/> | <span data-ttu-id="37f01-166">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37f01-166">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37f01-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37f01-167">Minimum supported server</span></span><br/> | <span data-ttu-id="37f01-168">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37f01-168">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="37f01-169">標頭</span><span class="sxs-lookup"><span data-stu-id="37f01-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f01-170"><dt>App.xaml.。h</dt></span><span class="sxs-lookup"><span data-stu-id="37f01-170"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="37f01-171">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="37f01-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="37f01-172"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="37f01-172"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="37f01-173">DLL</span><span class="sxs-lookup"><span data-stu-id="37f01-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37f01-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37f01-174"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="37f01-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37f01-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f01-176">**觸發**</span><span class="sxs-lookup"><span data-stu-id="37f01-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="37f01-177">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="37f01-177">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="37f01-178">**TriggerCollection 建立**</span><span class="sxs-lookup"><span data-stu-id="37f01-178">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

