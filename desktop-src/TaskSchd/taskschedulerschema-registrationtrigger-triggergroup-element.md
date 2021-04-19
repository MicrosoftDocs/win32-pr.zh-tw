---
title: RegistrationTrigger (triggerGroup) 元素
description: 指定在註冊工作時啟動工作的觸發程式。
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- 註冊觸發程式工作排程器、XML 元素
- RegistrationTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979686"
---
# <a name="registrationtrigger-triggergroup-element"></a><span data-ttu-id="3c835-105">RegistrationTrigger (triggerGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="3c835-105">RegistrationTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="3c835-106">指定在註冊工作時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3c835-106">Specifies a trigger that starts a task when the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

<span data-ttu-id="3c835-107">**RegistrationTrigger** 元素是由 [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="3c835-107">The **RegistrationTrigger** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3c835-108">父元素</span><span class="sxs-lookup"><span data-stu-id="3c835-108">Parent element</span></span>



| <span data-ttu-id="3c835-109">元素</span><span class="sxs-lookup"><span data-stu-id="3c835-109">Element</span></span>                                                           | <span data-ttu-id="3c835-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="3c835-110">Derived from</span></span>                                                         | <span data-ttu-id="3c835-111">Description</span><span class="sxs-lookup"><span data-stu-id="3c835-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="3c835-112">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="3c835-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="3c835-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="3c835-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="3c835-114">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3c835-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="3c835-115">子元素</span><span class="sxs-lookup"><span data-stu-id="3c835-115">Child elements</span></span>



| <span data-ttu-id="3c835-116">元素</span><span class="sxs-lookup"><span data-stu-id="3c835-116">Element</span></span>                                                                                                        | <span data-ttu-id="3c835-117">類型</span><span class="sxs-lookup"><span data-stu-id="3c835-117">Type</span></span>                                                                     | <span data-ttu-id="3c835-118">Description</span><span class="sxs-lookup"><span data-stu-id="3c835-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c835-119">**延遲 (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-119">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                   | <span data-ttu-id="3c835-120">duration</span><span class="sxs-lookup"><span data-stu-id="3c835-120">duration</span></span>                                                                 | <span data-ttu-id="3c835-121">指定在註冊工作與啟動工作之間的時間長度。</span><span class="sxs-lookup"><span data-stu-id="3c835-121">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/>                          |
| [<span data-ttu-id="3c835-122">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="3c835-123">boolean</span><span class="sxs-lookup"><span data-stu-id="3c835-123">boolean</span></span>                                                                  | <span data-ttu-id="3c835-124">指定啟用觸發程序。</span><span class="sxs-lookup"><span data-stu-id="3c835-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="3c835-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="3c835-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="3c835-126">dateTime</span></span>                                                                 | <span data-ttu-id="3c835-127">指定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3c835-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="3c835-128">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="3c835-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="3c835-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="3c835-130">duration</span><span class="sxs-lookup"><span data-stu-id="3c835-130">duration</span></span>                                                                 | <span data-ttu-id="3c835-131">指定觸發程式可啟動工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="3c835-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="3c835-132">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="3c835-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="3c835-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="3c835-134">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="3c835-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="3c835-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="3c835-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="3c835-136">dateTime</span></span>                                                                 | <span data-ttu-id="3c835-137">指定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3c835-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="3c835-138">屬性</span><span class="sxs-lookup"><span data-stu-id="3c835-138">Attributes</span></span>



| <span data-ttu-id="3c835-139">名稱</span><span class="sxs-lookup"><span data-stu-id="3c835-139">Name</span></span> | <span data-ttu-id="3c835-140">類型</span><span class="sxs-lookup"><span data-stu-id="3c835-140">Type</span></span> | <span data-ttu-id="3c835-141">Description</span><span class="sxs-lookup"><span data-stu-id="3c835-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="3c835-142">識別碼</span><span class="sxs-lookup"><span data-stu-id="3c835-142">Id</span></span>   | <span data-ttu-id="3c835-143">識別碼</span><span class="sxs-lookup"><span data-stu-id="3c835-143">ID</span></span>   | <span data-ttu-id="3c835-144">觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c835-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3c835-145">備註</span><span class="sxs-lookup"><span data-stu-id="3c835-145">Remarks</span></span>

<span data-ttu-id="3c835-146">針對開發腳本，會使用 [**RegistrationTrigger**](registrationtrigger.md) 物件來指定註冊觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3c835-146">For scripting development, a registration trigger is specified using the [**RegistrationTrigger**](registrationtrigger.md) object.</span></span>

<span data-ttu-id="3c835-147">針對 c + + 開發，會使用 [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) 介面指定註冊觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3c835-147">For C++ development, a registration trigger is specified using the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface.</span></span>

<span data-ttu-id="3c835-148">上方所列的子專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 和 [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="3c835-148">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="3c835-149">這些專案必須加入如下所示的順序中。</span><span class="sxs-lookup"><span data-stu-id="3c835-149">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="3c835-150">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-150">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="3c835-151">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-151">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="3c835-152">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-152">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="3c835-153">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-153">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="3c835-154">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-154">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="3c835-155">**延遲 (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="3c835-155">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a><span data-ttu-id="3c835-156">範例</span><span class="sxs-lookup"><span data-stu-id="3c835-156">Examples</span></span>

<span data-ttu-id="3c835-157">如需指定開機觸發程式之工作的完整 XML 範例，請參閱 [ (xml) 的註冊觸發程式範例 ](registration-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="3c835-157">For a complete example of the XML for a task that specifies a boot trigger, see [Registration Trigger Example (XML)](registration-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c835-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c835-158">Requirements</span></span>



| <span data-ttu-id="3c835-159">需求</span><span class="sxs-lookup"><span data-stu-id="3c835-159">Requirement</span></span> | <span data-ttu-id="3c835-160">值</span><span class="sxs-lookup"><span data-stu-id="3c835-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c835-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c835-161">Minimum supported client</span></span><br/> | <span data-ttu-id="3c835-162">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c835-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3c835-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c835-163">Minimum supported server</span></span><br/> | <span data-ttu-id="3c835-164">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c835-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c835-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c835-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c835-166">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="3c835-166">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3c835-167">工作排程器</span><span class="sxs-lookup"><span data-stu-id="3c835-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





