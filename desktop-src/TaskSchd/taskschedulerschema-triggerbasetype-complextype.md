---
title: triggerBaseType 複雜類型
description: 定義屬性、基底子項目，以及所有觸發程式複雜類型的排序資訊。
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- triggerBaseType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56602e4a7e6599b7b756ff6bc109376dddc63ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317495"
---
# <a name="triggerbasetype-complex-type"></a><span data-ttu-id="03e36-104">triggerBaseType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="03e36-104">triggerBaseType Complex Type</span></span>

<span data-ttu-id="03e36-105">定義屬性、基底子項目，以及所有觸發程式複雜類型的排序資訊。</span><span class="sxs-lookup"><span data-stu-id="03e36-105">Defines the attribute, base child elements, and sequencing information for all trigger complex types.</span></span>

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="03e36-106">子元素</span><span class="sxs-lookup"><span data-stu-id="03e36-106">Child elements</span></span>



| <span data-ttu-id="03e36-107">元素</span><span class="sxs-lookup"><span data-stu-id="03e36-107">Element</span></span>                                                                                      | <span data-ttu-id="03e36-108">類型</span><span class="sxs-lookup"><span data-stu-id="03e36-108">Type</span></span>                                                                     | <span data-ttu-id="03e36-109">Description</span><span class="sxs-lookup"><span data-stu-id="03e36-109">Description</span></span>                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03e36-110">**已啟用**</span><span class="sxs-lookup"><span data-stu-id="03e36-110">**Enabled**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="03e36-111">boolean</span><span class="sxs-lookup"><span data-stu-id="03e36-111">boolean</span></span>                                                                  | <span data-ttu-id="03e36-112">指定啟用觸發程序。</span><span class="sxs-lookup"><span data-stu-id="03e36-112">Specifies that the trigger is enabled.</span></span><br/>                                                                      |
| [<span data-ttu-id="03e36-113">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="03e36-113">**EndBoundary**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="03e36-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="03e36-114">dateTime</span></span>                                                                 | <span data-ttu-id="03e36-115">停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="03e36-115">The date and time when the trigger is deactivated.</span></span><br/>                                                          |
| [<span data-ttu-id="03e36-116">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="03e36-116">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="03e36-117">duration</span><span class="sxs-lookup"><span data-stu-id="03e36-117">duration</span></span>                                                                 | <span data-ttu-id="03e36-118">指定觸發程式可啟動工作的間隔。</span><span class="sxs-lookup"><span data-stu-id="03e36-118">Specifies the interval when the trigger can start the task.</span></span><br/>                                                 |
| [<span data-ttu-id="03e36-119">**重複**</span><span class="sxs-lookup"><span data-stu-id="03e36-119">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="03e36-120">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="03e36-120">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="03e36-121">指定執行工作的頻率，以及引發觸發程式之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="03e36-121">Specifies how often the task is run and how long the repetition pattern is repeated once the trigger fires.</span></span><br/> |
| [<span data-ttu-id="03e36-122">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="03e36-122">**StartBoundary**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="03e36-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="03e36-123">dateTime</span></span>                                                                 | <span data-ttu-id="03e36-124">啟用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="03e36-124">The date and time when the trigger is activated.</span></span><br/>                                                            |



## <a name="attributes"></a><span data-ttu-id="03e36-125">屬性</span><span class="sxs-lookup"><span data-stu-id="03e36-125">Attributes</span></span>



| <span data-ttu-id="03e36-126">名稱</span><span class="sxs-lookup"><span data-stu-id="03e36-126">Name</span></span> | <span data-ttu-id="03e36-127">類型</span><span class="sxs-lookup"><span data-stu-id="03e36-127">Type</span></span> | <span data-ttu-id="03e36-128">描述</span><span class="sxs-lookup"><span data-stu-id="03e36-128">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="03e36-129">id</span><span class="sxs-lookup"><span data-stu-id="03e36-129">id</span></span>   | <span data-ttu-id="03e36-130">識別碼</span><span class="sxs-lookup"><span data-stu-id="03e36-130">ID</span></span>   | <span data-ttu-id="03e36-131">觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03e36-131">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="03e36-132">備註</span><span class="sxs-lookup"><span data-stu-id="03e36-132">Remarks</span></span>

<span data-ttu-id="03e36-133">觸發複雜類型包含下列各項。</span><span class="sxs-lookup"><span data-stu-id="03e36-133">Trigger complex types include the following.</span></span>

-   [<span data-ttu-id="03e36-134">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="03e36-134">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)
-   [<span data-ttu-id="03e36-135">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="03e36-135">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)
-   [<span data-ttu-id="03e36-136">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="03e36-136">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)
-   [<span data-ttu-id="03e36-137">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="03e36-137">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)
-   [<span data-ttu-id="03e36-138">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="03e36-138">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)
-   [<span data-ttu-id="03e36-139">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="03e36-139">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)
-   [<span data-ttu-id="03e36-140">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="03e36-140">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a><span data-ttu-id="03e36-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="03e36-141">Requirements</span></span>



| <span data-ttu-id="03e36-142">需求</span><span class="sxs-lookup"><span data-stu-id="03e36-142">Requirement</span></span> | <span data-ttu-id="03e36-143">值</span><span class="sxs-lookup"><span data-stu-id="03e36-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="03e36-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03e36-144">Minimum supported client</span></span><br/> | <span data-ttu-id="03e36-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03e36-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="03e36-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03e36-146">Minimum supported server</span></span><br/> | <span data-ttu-id="03e36-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03e36-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03e36-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03e36-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e36-149">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="03e36-149">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="03e36-150">工作排程器</span><span class="sxs-lookup"><span data-stu-id="03e36-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





