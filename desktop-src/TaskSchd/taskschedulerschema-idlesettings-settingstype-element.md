---
title: IdleSettings (settingsType) 元素
description: 指定當電腦處於閒置狀態時，工作排程器如何執行工作。
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- IdleSettings 元素工作排程器
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105221"
---
# <a name="idlesettings-settingstype-element"></a><span data-ttu-id="f5c76-104">IdleSettings (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="f5c76-104">IdleSettings (settingsType) Element</span></span>

<span data-ttu-id="f5c76-105">指定當電腦處於閒置狀態時，工作排程器如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="f5c76-105">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span> <span data-ttu-id="f5c76-106">如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。</span><span class="sxs-lookup"><span data-stu-id="f5c76-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="f5c76-107">**IdleSettings** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="f5c76-107">The **IdleSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f5c76-108">父元素</span><span class="sxs-lookup"><span data-stu-id="f5c76-108">Parent element</span></span>

| <span data-ttu-id="f5c76-109">元素</span><span class="sxs-lookup"><span data-stu-id="f5c76-109">Element</span></span>                                                           | <span data-ttu-id="f5c76-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="f5c76-110">Derived from</span></span>                                                         | <span data-ttu-id="f5c76-111">Description</span><span class="sxs-lookup"><span data-stu-id="f5c76-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5c76-112">**設定**</span><span class="sxs-lookup"><span data-stu-id="f5c76-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f5c76-113">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="f5c76-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f5c76-114">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="f5c76-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |

## <a name="child-elements"></a><span data-ttu-id="f5c76-115">子元素</span><span class="sxs-lookup"><span data-stu-id="f5c76-115">Child elements</span></span>

> [!NOTE]
> <span data-ttu-id="f5c76-116">*持續時間* 和 *WaitTimeout* 設定已淘汰。</span><span class="sxs-lookup"><span data-stu-id="f5c76-116">The *Duration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="f5c76-117">它們仍然存在於工作排程器的使用者介面中，而且其介面方法可能仍會傳回有效值，但不再使用這些值。</span><span class="sxs-lookup"><span data-stu-id="f5c76-117">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="f5c76-118">元素</span><span class="sxs-lookup"><span data-stu-id="f5c76-118">Element</span></span>                                                                                  | <span data-ttu-id="f5c76-119">類型</span><span class="sxs-lookup"><span data-stu-id="f5c76-119">Type</span></span>     | <span data-ttu-id="f5c76-120">Description</span><span class="sxs-lookup"><span data-stu-id="f5c76-120">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5c76-121">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="f5c76-121">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="f5c76-122">boolean</span><span class="sxs-lookup"><span data-stu-id="f5c76-122">boolean</span></span>  | <span data-ttu-id="f5c76-123">指定當電腦迴圈進入閒置條件超過一次時，是否重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="f5c76-123">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>       |
| [<span data-ttu-id="f5c76-124">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="f5c76-124">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="f5c76-125">boolean</span><span class="sxs-lookup"><span data-stu-id="f5c76-125">boolean</span></span>  | <span data-ttu-id="f5c76-126">指定如果閒置條件在工作完成之前結束，工作排程器將停止工作。</span><span class="sxs-lookup"><span data-stu-id="f5c76-126">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="f5c76-127">已 **淘汰**： [**持續時間**](taskschedulerschema-duration-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="f5c76-127">**Deprecated**: [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)</span></span>                | <span data-ttu-id="f5c76-128">duration</span><span class="sxs-lookup"><span data-stu-id="f5c76-128">duration</span></span> | <span data-ttu-id="f5c76-129">指定在執行工作之前，電腦必須處於閒置狀態的時間長度。</span><span class="sxs-lookup"><span data-stu-id="f5c76-129">Specifies how long the computer must be in an idle state before the task is run.</span></span><br/>                              |
| <span data-ttu-id="f5c76-130">已 **淘汰**： [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="f5c76-130">**Deprecated**: [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span></span>          | <span data-ttu-id="f5c76-131">duration</span><span class="sxs-lookup"><span data-stu-id="f5c76-131">duration</span></span> | <span data-ttu-id="f5c76-132">指定工作排程器將等候閒置條件發生的時間量。</span><span class="sxs-lookup"><span data-stu-id="f5c76-132">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                |

## <a name="remarks"></a><span data-ttu-id="f5c76-133">備註</span><span class="sxs-lookup"><span data-stu-id="f5c76-133">Remarks</span></span>

<span data-ttu-id="f5c76-134">針對腳本開發，閒置設定會使用 [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="f5c76-134">For script development, idle settings are specified using the [**TaskSettings.IdleSettings**](tasksettings-idlesettings.md) property.</span></span>

<span data-ttu-id="f5c76-135">針對 c + + 開發，閒置設定是使用 [**ITaskSettings：： IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="f5c76-135">For C++ development, idle settings are specified using the [**ITaskSettings::IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f5c76-136">範例</span><span class="sxs-lookup"><span data-stu-id="f5c76-136">Examples</span></span>

<span data-ttu-id="f5c76-137">下列 XML 定義了設定元素，可讓工作排程器等候24小時的閒置條件，然後只允許10分鐘的 {IdleDuration) 起始工作。</span><span class="sxs-lookup"><span data-stu-id="f5c76-137">The following XML defines a settings element that allows Task Scheduler to wait 24 hours for an idle condition and then allows only 10 minutes {IdleDuration) to initiate the task.</span></span>

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a><span data-ttu-id="f5c76-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5c76-138">Requirements</span></span>

| <span data-ttu-id="f5c76-139">需求</span><span class="sxs-lookup"><span data-stu-id="f5c76-139">Requirement</span></span> | <span data-ttu-id="f5c76-140">值</span><span class="sxs-lookup"><span data-stu-id="f5c76-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5c76-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5c76-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c76-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5c76-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f5c76-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5c76-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c76-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5c76-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="f5c76-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5c76-145">See also</span></span>

[<span data-ttu-id="f5c76-146">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="f5c76-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="f5c76-147">工作排程器</span><span class="sxs-lookup"><span data-stu-id="f5c76-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
