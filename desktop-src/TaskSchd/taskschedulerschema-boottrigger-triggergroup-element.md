---
title: BootTrigger (triggerGroup) 元素
description: 指定啟動系統時啟動工作的觸發程式。
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- 開機觸發程式工作排程器、XML 元素
- BootTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317356"
---
# <a name="boottrigger-triggergroup-element"></a><span data-ttu-id="0cf58-105">BootTrigger (triggerGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="0cf58-105">BootTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="0cf58-106">指定啟動系統時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="0cf58-106">Specifies a trigger that starts a task when the system is booted.</span></span>

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

<span data-ttu-id="0cf58-107">**BootTrigger** 元素是由 [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="0cf58-107">The **BootTrigger** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0cf58-108">父元素</span><span class="sxs-lookup"><span data-stu-id="0cf58-108">Parent element</span></span>



| <span data-ttu-id="0cf58-109">元素</span><span class="sxs-lookup"><span data-stu-id="0cf58-109">Element</span></span>                                                           | <span data-ttu-id="0cf58-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="0cf58-110">Derived from</span></span>                                                         | <span data-ttu-id="0cf58-111">Description</span><span class="sxs-lookup"><span data-stu-id="0cf58-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="0cf58-112">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="0cf58-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="0cf58-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="0cf58-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="0cf58-114">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="0cf58-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="0cf58-115">子元素</span><span class="sxs-lookup"><span data-stu-id="0cf58-115">Child elements</span></span>



| <span data-ttu-id="0cf58-116">元素</span><span class="sxs-lookup"><span data-stu-id="0cf58-116">Element</span></span>                                                                                                        | <span data-ttu-id="0cf58-117">類型</span><span class="sxs-lookup"><span data-stu-id="0cf58-117">Type</span></span>                                                                     | <span data-ttu-id="0cf58-118">Description</span><span class="sxs-lookup"><span data-stu-id="0cf58-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cf58-119">**延遲 (bootTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="0cf58-119">**Delay (bootTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                           | <span data-ttu-id="0cf58-120">duration</span><span class="sxs-lookup"><span data-stu-id="0cf58-120">duration</span></span>                                                                 | <span data-ttu-id="0cf58-121">指定啟動系統與啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="0cf58-121">Specifies the amount of time between when the system is booted and when the task is started.</span></span><br/>                            |
| [<span data-ttu-id="0cf58-122">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0cf58-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="0cf58-123">boolean</span><span class="sxs-lookup"><span data-stu-id="0cf58-123">boolean</span></span>                                                                  | <span data-ttu-id="0cf58-124">指定啟用觸發程序。</span><span class="sxs-lookup"><span data-stu-id="0cf58-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="0cf58-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0cf58-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="0cf58-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="0cf58-126">dateTime</span></span>                                                                 | <span data-ttu-id="0cf58-127">指定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0cf58-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="0cf58-128">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="0cf58-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="0cf58-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0cf58-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="0cf58-130">duration</span><span class="sxs-lookup"><span data-stu-id="0cf58-130">duration</span></span>                                                                 | <span data-ttu-id="0cf58-131">指定觸發程式可啟動工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="0cf58-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="0cf58-132">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0cf58-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="0cf58-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="0cf58-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="0cf58-134">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="0cf58-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="0cf58-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="0cf58-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="0cf58-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="0cf58-136">dateTime</span></span>                                                                 | <span data-ttu-id="0cf58-137">指定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0cf58-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="0cf58-138">屬性</span><span class="sxs-lookup"><span data-stu-id="0cf58-138">Attributes</span></span>



| <span data-ttu-id="0cf58-139">名稱</span><span class="sxs-lookup"><span data-stu-id="0cf58-139">Name</span></span> | <span data-ttu-id="0cf58-140">類型</span><span class="sxs-lookup"><span data-stu-id="0cf58-140">Type</span></span>       | <span data-ttu-id="0cf58-141">Description</span><span class="sxs-lookup"><span data-stu-id="0cf58-141">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="0cf58-142">識別碼</span><span class="sxs-lookup"><span data-stu-id="0cf58-142">Id</span></span>   | <span data-ttu-id="0cf58-143">**string**</span><span class="sxs-lookup"><span data-stu-id="0cf58-143">**string**</span></span> | <span data-ttu-id="0cf58-144">觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cf58-144">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0cf58-145">備註</span><span class="sxs-lookup"><span data-stu-id="0cf58-145">Remarks</span></span>

<span data-ttu-id="0cf58-146">針對開發腳本， [**BootTrigger**](boottrigger.md) 物件會定義開機觸發程式。</span><span class="sxs-lookup"><span data-stu-id="0cf58-146">For script development, a boot trigger is defined by the [**BootTrigger**](boottrigger.md) object.</span></span>

<span data-ttu-id="0cf58-147">針對 c + + 開發，開機觸發程式是由 [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) 物件所定義。</span><span class="sxs-lookup"><span data-stu-id="0cf58-147">For C++ development, a boot trigger is defined by the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) object.</span></span>

## <a name="examples"></a><span data-ttu-id="0cf58-148">範例</span><span class="sxs-lookup"><span data-stu-id="0cf58-148">Examples</span></span>

<span data-ttu-id="0cf58-149">如需指定開機觸發程式之工作的完整 XML 範例，請參閱 [ (xml) 的開機觸發程式範例 ](boot-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="0cf58-149">For a complete example of the XML for a task that specifies a boot trigger, see [Boot Trigger Example (XML)](boot-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf58-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cf58-150">Requirements</span></span>



| <span data-ttu-id="0cf58-151">需求</span><span class="sxs-lookup"><span data-stu-id="0cf58-151">Requirement</span></span> | <span data-ttu-id="0cf58-152">值</span><span class="sxs-lookup"><span data-stu-id="0cf58-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0cf58-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0cf58-153">Minimum supported client</span></span><br/> | <span data-ttu-id="0cf58-154">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cf58-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0cf58-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0cf58-155">Minimum supported server</span></span><br/> | <span data-ttu-id="0cf58-156">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cf58-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0cf58-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cf58-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf58-158">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="0cf58-158">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0cf58-159">工作排程器</span><span class="sxs-lookup"><span data-stu-id="0cf58-159">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





