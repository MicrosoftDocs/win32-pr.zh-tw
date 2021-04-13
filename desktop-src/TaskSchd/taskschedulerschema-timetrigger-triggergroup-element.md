---
title: TimeTrigger (triggerGroup) 元素
description: 指定啟動觸發程式時啟動工作的觸發程式。
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- TimeTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466272"
---
# <a name="timetrigger-triggergroup-element"></a><span data-ttu-id="57103-104">TimeTrigger (triggerGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="57103-104">TimeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="57103-105">指定啟動觸發程式時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="57103-105">Specifies a trigger that starts a task when the trigger is activated.</span></span>

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

<span data-ttu-id="57103-106">**TimeTrigger** 元素是由 [**triggerGroup**](taskschedulerschema-triggergroup-group.md)定義。</span><span class="sxs-lookup"><span data-stu-id="57103-106">The **TimeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="57103-107">父元素</span><span class="sxs-lookup"><span data-stu-id="57103-107">Parent element</span></span>



| <span data-ttu-id="57103-108">元素</span><span class="sxs-lookup"><span data-stu-id="57103-108">Element</span></span>                                                           | <span data-ttu-id="57103-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="57103-109">Derived from</span></span>                                                         | <span data-ttu-id="57103-110">Description</span><span class="sxs-lookup"><span data-stu-id="57103-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="57103-111">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="57103-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="57103-112">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="57103-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="57103-113">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="57103-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="57103-114">子元素</span><span class="sxs-lookup"><span data-stu-id="57103-114">Child elements</span></span>



| <span data-ttu-id="57103-115">元素</span><span class="sxs-lookup"><span data-stu-id="57103-115">Element</span></span>                                                                                                        | <span data-ttu-id="57103-116">類型</span><span class="sxs-lookup"><span data-stu-id="57103-116">Type</span></span>                                                                     | <span data-ttu-id="57103-117">Description</span><span class="sxs-lookup"><span data-stu-id="57103-117">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57103-118">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-118">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="57103-119">boolean</span><span class="sxs-lookup"><span data-stu-id="57103-119">boolean</span></span>                                                                  | <span data-ttu-id="57103-120">指定啟用觸發程序。</span><span class="sxs-lookup"><span data-stu-id="57103-120">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="57103-121">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-121">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="57103-122">dateTime</span><span class="sxs-lookup"><span data-stu-id="57103-122">dateTime</span></span>                                                                 | <span data-ttu-id="57103-123">指定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="57103-123">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="57103-124">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="57103-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="57103-125">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-125">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="57103-126">duration</span><span class="sxs-lookup"><span data-stu-id="57103-126">duration</span></span>                                                                 | <span data-ttu-id="57103-127">指定觸發程式可啟動工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="57103-127">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="57103-128">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-128">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="57103-129">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="57103-129">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="57103-130">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="57103-130">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="57103-131">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-131">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="57103-132">dateTime</span><span class="sxs-lookup"><span data-stu-id="57103-132">dateTime</span></span>                                                                 | <span data-ttu-id="57103-133">指定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="57103-133">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="57103-134">這個元素是必要的。</span><span class="sxs-lookup"><span data-stu-id="57103-134">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="57103-135">屬性</span><span class="sxs-lookup"><span data-stu-id="57103-135">Attributes</span></span>



| <span data-ttu-id="57103-136">名稱</span><span class="sxs-lookup"><span data-stu-id="57103-136">Name</span></span> | <span data-ttu-id="57103-137">類型</span><span class="sxs-lookup"><span data-stu-id="57103-137">Type</span></span>       | <span data-ttu-id="57103-138">Description</span><span class="sxs-lookup"><span data-stu-id="57103-138">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="57103-139">識別碼</span><span class="sxs-lookup"><span data-stu-id="57103-139">Id</span></span>   | <span data-ttu-id="57103-140">**string**</span><span class="sxs-lookup"><span data-stu-id="57103-140">**string**</span></span> | <span data-ttu-id="57103-141">觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="57103-141">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="57103-142">備註</span><span class="sxs-lookup"><span data-stu-id="57103-142">Remarks</span></span>

<span data-ttu-id="57103-143">[**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是時間和行事曆觸發程式的必要元素， (**TimeTrigger** 和 [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)) 。</span><span class="sxs-lookup"><span data-stu-id="57103-143">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers (**TimeTrigger** and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="57103-144">針對開發腳本，會使用 [**TimeTrigger**](timetrigger.md) 物件來指定時間觸發程式。</span><span class="sxs-lookup"><span data-stu-id="57103-144">For scripting development, a time trigger is specified using the [**TimeTrigger**](timetrigger.md) object.</span></span>

<span data-ttu-id="57103-145">針對 c + + 開發，會使用 [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) 介面來指定時間觸發程式。</span><span class="sxs-lookup"><span data-stu-id="57103-145">For C++ development, a time trigger is specified using the [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) interface.</span></span>

<span data-ttu-id="57103-146">上方所列的子專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="57103-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="57103-147">這些專案必須加入如下所示的順序中。</span><span class="sxs-lookup"><span data-stu-id="57103-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="57103-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="57103-149">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="57103-150">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="57103-151">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="57103-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="57103-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="57103-153">範例</span><span class="sxs-lookup"><span data-stu-id="57103-153">Examples</span></span>

<span data-ttu-id="57103-154">如需指定時間觸發程式之 XML 的完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="57103-154">For a complete example of the XML for a task that specifies a time trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57103-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="57103-155">Requirements</span></span>



| <span data-ttu-id="57103-156">需求</span><span class="sxs-lookup"><span data-stu-id="57103-156">Requirement</span></span> | <span data-ttu-id="57103-157">值</span><span class="sxs-lookup"><span data-stu-id="57103-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="57103-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57103-158">Minimum supported client</span></span><br/> | <span data-ttu-id="57103-159">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57103-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="57103-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57103-160">Minimum supported server</span></span><br/> | <span data-ttu-id="57103-161">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57103-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57103-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57103-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57103-163">工作排程器</span><span class="sxs-lookup"><span data-stu-id="57103-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





