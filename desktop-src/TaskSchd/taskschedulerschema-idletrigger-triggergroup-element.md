---
title: IdleTrigger (triggerGroup) 元素
description: 指定當電腦進入閒置狀態時啟動工作的觸發程式。
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- 閒置觸發程式，XML 元素
- IdleTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 221d272145670b9514cde5ffbe8b02e5ddcd6e0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024770"
---
# <a name="idletrigger-triggergroup-element"></a><span data-ttu-id="f9d65-105">IdleTrigger (triggerGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="f9d65-105">IdleTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="f9d65-106">指定當電腦進入閒置狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="f9d65-106">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span> <span data-ttu-id="f9d65-107">如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d65-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

<span data-ttu-id="f9d65-108">**IdleTrigger** 元素是由 [**triggerGroup**](taskschedulerschema-triggergroup-group.md)定義。</span><span class="sxs-lookup"><span data-stu-id="f9d65-108">The **IdleTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f9d65-109">父元素</span><span class="sxs-lookup"><span data-stu-id="f9d65-109">Parent element</span></span>



| <span data-ttu-id="f9d65-110">元素</span><span class="sxs-lookup"><span data-stu-id="f9d65-110">Element</span></span>                                                           | <span data-ttu-id="f9d65-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="f9d65-111">Derived from</span></span>                                                         | <span data-ttu-id="f9d65-112">Description</span><span class="sxs-lookup"><span data-stu-id="f9d65-112">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f9d65-113">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="f9d65-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="f9d65-114">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="f9d65-114">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="f9d65-115">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="f9d65-115">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f9d65-116">子元素</span><span class="sxs-lookup"><span data-stu-id="f9d65-116">Child elements</span></span>



| <span data-ttu-id="f9d65-117">元素</span><span class="sxs-lookup"><span data-stu-id="f9d65-117">Element</span></span>                                                                                                        | <span data-ttu-id="f9d65-118">類型</span><span class="sxs-lookup"><span data-stu-id="f9d65-118">Type</span></span>                                                                     | <span data-ttu-id="f9d65-119">Description</span><span class="sxs-lookup"><span data-stu-id="f9d65-119">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9d65-120">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-120">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="f9d65-121">boolean</span><span class="sxs-lookup"><span data-stu-id="f9d65-121">boolean</span></span>                                                                  | <span data-ttu-id="f9d65-122">指定啟用觸發程序。</span><span class="sxs-lookup"><span data-stu-id="f9d65-122">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f9d65-123">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-123">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="f9d65-124">dateTime</span><span class="sxs-lookup"><span data-stu-id="f9d65-124">dateTime</span></span>                                                                 | <span data-ttu-id="f9d65-125">指定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f9d65-125">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="f9d65-126">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="f9d65-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="f9d65-127">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-127">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="f9d65-128">duration</span><span class="sxs-lookup"><span data-stu-id="f9d65-128">duration</span></span>                                                                 | <span data-ttu-id="f9d65-129">指定觸發程式可啟動工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="f9d65-129">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="f9d65-130">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-130">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="f9d65-131">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="f9d65-131">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="f9d65-132">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="f9d65-132">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="f9d65-133">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-133">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="f9d65-134">dateTime</span><span class="sxs-lookup"><span data-stu-id="f9d65-134">dateTime</span></span>                                                                 | <span data-ttu-id="f9d65-135">指定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f9d65-135">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="f9d65-136">屬性</span><span class="sxs-lookup"><span data-stu-id="f9d65-136">Attributes</span></span>



| <span data-ttu-id="f9d65-137">名稱</span><span class="sxs-lookup"><span data-stu-id="f9d65-137">Name</span></span> | <span data-ttu-id="f9d65-138">類型</span><span class="sxs-lookup"><span data-stu-id="f9d65-138">Type</span></span>   | <span data-ttu-id="f9d65-139">Description</span><span class="sxs-lookup"><span data-stu-id="f9d65-139">Description</span></span>                               |
|------|--------|-------------------------------------------|
| <span data-ttu-id="f9d65-140">識別碼</span><span class="sxs-lookup"><span data-stu-id="f9d65-140">Id</span></span>   | <span data-ttu-id="f9d65-141">字串</span><span class="sxs-lookup"><span data-stu-id="f9d65-141">string</span></span> | <span data-ttu-id="f9d65-142">觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9d65-142">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f9d65-143">備註</span><span class="sxs-lookup"><span data-stu-id="f9d65-143">Remarks</span></span>

<span data-ttu-id="f9d65-144">針對開發腳本，會使用 [**IdleTrigger**](idletrigger.md) 物件來指定閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="f9d65-144">For scripting development, an idle trigger is specified using the [**IdleTrigger**](idletrigger.md) object.</span></span>

<span data-ttu-id="f9d65-145">針對 c + + 開發，會使用 [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) 介面指定閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="f9d65-145">For C++ development, an idle trigger is specified using the [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) interface.</span></span>

<span data-ttu-id="f9d65-146">上方所列的子專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="f9d65-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="f9d65-147">這些專案必須加入如下所示的順序中。</span><span class="sxs-lookup"><span data-stu-id="f9d65-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="f9d65-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="f9d65-149">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="f9d65-150">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="f9d65-151">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="f9d65-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="f9d65-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="f9d65-153">範例</span><span class="sxs-lookup"><span data-stu-id="f9d65-153">Examples</span></span>

<span data-ttu-id="f9d65-154">下列 XML 定義閒置觸發程式。</span><span class="sxs-lookup"><span data-stu-id="f9d65-154">The following XML defines an idle trigger.</span></span>


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



## <a name="requirements"></a><span data-ttu-id="f9d65-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9d65-155">Requirements</span></span>



| <span data-ttu-id="f9d65-156">需求</span><span class="sxs-lookup"><span data-stu-id="f9d65-156">Requirement</span></span> | <span data-ttu-id="f9d65-157">值</span><span class="sxs-lookup"><span data-stu-id="f9d65-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9d65-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9d65-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f9d65-159">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9d65-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9d65-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9d65-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f9d65-161">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9d65-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9d65-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9d65-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9d65-163">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="f9d65-163">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f9d65-164">工作排程器</span><span class="sxs-lookup"><span data-stu-id="f9d65-164">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

