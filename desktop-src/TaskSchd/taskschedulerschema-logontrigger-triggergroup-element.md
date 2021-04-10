---
title: LogonTrigger (triggerGroup) 元素
description: 指定當使用者登入時啟動工作的觸發程式。
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- 登入觸發程式，XML 元素
- LogonTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317195"
---
# <a name="logontrigger-triggergroup-element"></a><span data-ttu-id="da40e-105">LogonTrigger (triggerGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="da40e-105">LogonTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="da40e-106">指定當使用者登入時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="da40e-106">Specifies a trigger that starts a task when a user logs on.</span></span>

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

<span data-ttu-id="da40e-107">**LogonTrigger** 元素是由 [**triggerGroup**](taskschedulerschema-triggergroup-group.md)定義。</span><span class="sxs-lookup"><span data-stu-id="da40e-107">The **LogonTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="da40e-108">父元素</span><span class="sxs-lookup"><span data-stu-id="da40e-108">Parent element</span></span>



| <span data-ttu-id="da40e-109">元素</span><span class="sxs-lookup"><span data-stu-id="da40e-109">Element</span></span>                                                           | <span data-ttu-id="da40e-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="da40e-110">Derived from</span></span>                                                         | <span data-ttu-id="da40e-111">Description</span><span class="sxs-lookup"><span data-stu-id="da40e-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="da40e-112">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="da40e-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="da40e-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="da40e-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="da40e-114">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="da40e-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="da40e-115">子元素</span><span class="sxs-lookup"><span data-stu-id="da40e-115">Child elements</span></span>



| <span data-ttu-id="da40e-116">元素</span><span class="sxs-lookup"><span data-stu-id="da40e-116">Element</span></span>                                                                                                        | <span data-ttu-id="da40e-117">類型</span><span class="sxs-lookup"><span data-stu-id="da40e-117">Type</span></span>                                                                     | <span data-ttu-id="da40e-118">Description</span><span class="sxs-lookup"><span data-stu-id="da40e-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da40e-119">**延遲 (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-119">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)                         | <span data-ttu-id="da40e-120">duration</span><span class="sxs-lookup"><span data-stu-id="da40e-120">duration</span></span>                                                                 | <span data-ttu-id="da40e-121">使用者登入和工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="da40e-121">Amount of time between when the user logs on and when the task is started.</span></span><br/>                                              |
| [<span data-ttu-id="da40e-122">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="da40e-123">boolean</span><span class="sxs-lookup"><span data-stu-id="da40e-123">boolean</span></span>                                                                  | <span data-ttu-id="da40e-124">指定啟用觸發程序。</span><span class="sxs-lookup"><span data-stu-id="da40e-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="da40e-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="da40e-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="da40e-126">dateTime</span></span>                                                                 | <span data-ttu-id="da40e-127">指定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="da40e-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="da40e-128">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="da40e-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="da40e-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="da40e-130">duration</span><span class="sxs-lookup"><span data-stu-id="da40e-130">duration</span></span>                                                                 | <span data-ttu-id="da40e-131">指定觸發程式可啟動工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="da40e-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="da40e-132">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="da40e-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="da40e-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="da40e-134">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="da40e-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="da40e-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="da40e-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="da40e-136">dateTime</span></span>                                                                 | <span data-ttu-id="da40e-137">指定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="da40e-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="da40e-138">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-138">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)                       | <span data-ttu-id="da40e-139">字串</span><span class="sxs-lookup"><span data-stu-id="da40e-139">string</span></span>                                                                   | <span data-ttu-id="da40e-140">使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="da40e-140">Identifier of the user.</span></span> <span data-ttu-id="da40e-141">此工作會在此使用者登入電腦時啟動。</span><span class="sxs-lookup"><span data-stu-id="da40e-141">The task is started when this user logs onto the computer.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="da40e-142">備註</span><span class="sxs-lookup"><span data-stu-id="da40e-142">Remarks</span></span>

<span data-ttu-id="da40e-143">針對開發腳本，會使用 [**LogonTrigger**](logontrigger.md) 物件來指定登入觸發程式。</span><span class="sxs-lookup"><span data-stu-id="da40e-143">For scripting development, a logon trigger is specified using the [**LogonTrigger**](logontrigger.md) object.</span></span>

<span data-ttu-id="da40e-144">針對 c + + 開發，會使用 [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) 介面來指定登入觸發程式。</span><span class="sxs-lookup"><span data-stu-id="da40e-144">For C++ development, a logon trigger is specified using the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface.</span></span>

<span data-ttu-id="da40e-145">上方所列的子專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 和 [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="da40e-145">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="da40e-146">這些專案必須加入如下所示的順序中。</span><span class="sxs-lookup"><span data-stu-id="da40e-146">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="da40e-147">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-147">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="da40e-148">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-148">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="da40e-149">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-149">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="da40e-150">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-150">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="da40e-151">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-151">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="da40e-152">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-152">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)
-   [<span data-ttu-id="da40e-153">**延遲 (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="da40e-153">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a><span data-ttu-id="da40e-154">屬性</span><span class="sxs-lookup"><span data-stu-id="da40e-154">Attributes</span></span>

<span data-ttu-id="da40e-155">下列屬性是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="da40e-155">The attribute listed below is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span>

-   <span data-ttu-id="da40e-156">識別碼：觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="da40e-156">Id: Identifier of the trigger.</span></span>

## <a name="examples"></a><span data-ttu-id="da40e-157">範例</span><span class="sxs-lookup"><span data-stu-id="da40e-157">Examples</span></span>

<span data-ttu-id="da40e-158">如需使用登入觸發程式之 XML 的完整範例，請參閱登入 [觸發程式範例 (xml) ](logon-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="da40e-158">For a complete example of the XML for a task that uses a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da40e-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="da40e-159">Requirements</span></span>



| <span data-ttu-id="da40e-160">需求</span><span class="sxs-lookup"><span data-stu-id="da40e-160">Requirement</span></span> | <span data-ttu-id="da40e-161">值</span><span class="sxs-lookup"><span data-stu-id="da40e-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da40e-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da40e-162">Minimum supported client</span></span><br/> | <span data-ttu-id="da40e-163">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da40e-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da40e-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da40e-164">Minimum supported server</span></span><br/> | <span data-ttu-id="da40e-165">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da40e-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da40e-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da40e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da40e-167">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="da40e-167">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





