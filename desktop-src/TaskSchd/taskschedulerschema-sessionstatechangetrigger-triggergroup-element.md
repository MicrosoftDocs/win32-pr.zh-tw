---
title: SessionStateChangeTrigger (triggerGroup) 元素
description: 指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- SessionStateChangeTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686221"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a><span data-ttu-id="1b8c5-104">SessionStateChangeTrigger (triggerGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="1b8c5-104">SessionStateChangeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="1b8c5-105">指定在終端機伺服器會話變更狀態時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="1b8c5-105">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span>

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

<span data-ttu-id="1b8c5-106">**SessionStateChangeTrigger** 元素是由 [**triggerGroup**](taskschedulerschema-triggergroup-group.md)定義。</span><span class="sxs-lookup"><span data-stu-id="1b8c5-106">The **SessionStateChangeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="1b8c5-107">父元素</span><span class="sxs-lookup"><span data-stu-id="1b8c5-107">Parent element</span></span>



| <span data-ttu-id="1b8c5-108">元素</span><span class="sxs-lookup"><span data-stu-id="1b8c5-108">Element</span></span>                                                           | <span data-ttu-id="1b8c5-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="1b8c5-109">Derived from</span></span>                                                         | <span data-ttu-id="1b8c5-110">Description</span><span class="sxs-lookup"><span data-stu-id="1b8c5-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="1b8c5-111">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="1b8c5-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="1b8c5-112">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="1b8c5-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="1b8c5-113">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="1b8c5-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="1b8c5-114">子元素</span><span class="sxs-lookup"><span data-stu-id="1b8c5-114">Child elements</span></span>



| <span data-ttu-id="1b8c5-115">元素</span><span class="sxs-lookup"><span data-stu-id="1b8c5-115">Element</span></span>                                                                                      | <span data-ttu-id="1b8c5-116">類型</span><span class="sxs-lookup"><span data-stu-id="1b8c5-116">Type</span></span>                                                                                    | <span data-ttu-id="1b8c5-117">Description</span><span class="sxs-lookup"><span data-stu-id="1b8c5-117">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b8c5-118">**延遲**</span><span class="sxs-lookup"><span data-stu-id="1b8c5-118">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="1b8c5-119">duration</span><span class="sxs-lookup"><span data-stu-id="1b8c5-119">duration</span></span>                                                                                | <span data-ttu-id="1b8c5-120">指定值，這個值表示在偵測到終端機伺服器會話狀態變更時，工作開始之前的延遲時間長度。</span><span class="sxs-lookup"><span data-stu-id="1b8c5-120">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="1b8c5-121">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="1b8c5-121">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="1b8c5-122">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="1b8c5-122">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="1b8c5-123">指定會觸發工作啟動的終端機伺服器會話變更類型。</span><span class="sxs-lookup"><span data-stu-id="1b8c5-123">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="1b8c5-124">**UserId**</span><span class="sxs-lookup"><span data-stu-id="1b8c5-124">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="1b8c5-125">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="1b8c5-125">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="1b8c5-126">指定終端機伺服器會話的使用者。</span><span class="sxs-lookup"><span data-stu-id="1b8c5-126">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="1b8c5-127">當偵測到此使用者的會話狀態變更時，就會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="1b8c5-127">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="1b8c5-128">備註</span><span class="sxs-lookup"><span data-stu-id="1b8c5-128">Remarks</span></span>

<span data-ttu-id="1b8c5-129">針對開發腳本，會使用 [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) 物件來指定會話狀態變更觸發程式。</span><span class="sxs-lookup"><span data-stu-id="1b8c5-129">For scripting development, a session state change trigger is specified using the [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) object.</span></span>

<span data-ttu-id="1b8c5-130">針對 c + + 開發，會話狀態變更觸發程式是使用 [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) 介面指定的。</span><span class="sxs-lookup"><span data-stu-id="1b8c5-130">For C++ development, a session state change trigger is specified using the [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8c5-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b8c5-131">Requirements</span></span>



| <span data-ttu-id="1b8c5-132">需求</span><span class="sxs-lookup"><span data-stu-id="1b8c5-132">Requirement</span></span> | <span data-ttu-id="1b8c5-133">值</span><span class="sxs-lookup"><span data-stu-id="1b8c5-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b8c5-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b8c5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8c5-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b8c5-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b8c5-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b8c5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8c5-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b8c5-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





