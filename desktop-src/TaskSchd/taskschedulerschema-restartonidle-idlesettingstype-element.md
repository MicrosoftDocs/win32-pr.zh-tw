---
title: RestartOnIdle (idleSettingsType) 元素
description: 指定當電腦迴圈進入閒置條件超過一次時，是否重新開機工作。
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- RestartOnIdle 元素工作排程器
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965533"
---
# <a name="restartonidle-idlesettingstype-element"></a><span data-ttu-id="73b58-104">RestartOnIdle (idleSettingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="73b58-104">RestartOnIdle (idleSettingsType) Element</span></span>

<span data-ttu-id="73b58-105">指定當電腦迴圈進入閒置條件超過一次時，是否重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="73b58-105">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="73b58-106">**RestartOnIdle** 元素是由 [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="73b58-106">The **RestartOnIdle** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="73b58-107">父元素</span><span class="sxs-lookup"><span data-stu-id="73b58-107">Parent element</span></span>



| <span data-ttu-id="73b58-108">元素</span><span class="sxs-lookup"><span data-stu-id="73b58-108">Element</span></span>                                                                       | <span data-ttu-id="73b58-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="73b58-109">Derived from</span></span>                                                                 | <span data-ttu-id="73b58-110">Description</span><span class="sxs-lookup"><span data-stu-id="73b58-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73b58-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="73b58-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="73b58-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="73b58-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="73b58-113">指定當電腦處於閒置狀態時，工作排程器如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="73b58-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="73b58-114">備註</span><span class="sxs-lookup"><span data-stu-id="73b58-114">Remarks</span></span>

<span data-ttu-id="73b58-115">只有當 [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) 元素設定為 True 時，才會使用這個元素。</span><span class="sxs-lookup"><span data-stu-id="73b58-115">This element is used only if the [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element is set to True.</span></span>

<span data-ttu-id="73b58-116">針對腳本開發，此工作設定會使用 [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="73b58-116">For script development, this task settings is specified using the [**IdleSettings.RestartOnIdle**](idlesettings-restartonidle.md) property.</span></span>

<span data-ttu-id="73b58-117">針對 c + + 開發，此工作設定會使用 [**IIdleSettings：： RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="73b58-117">For C++ development, this task settings is specified using the [**IIdleSettings::RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) property.</span></span>

## <a name="examples"></a><span data-ttu-id="73b58-118">範例</span><span class="sxs-lookup"><span data-stu-id="73b58-118">Examples</span></span>

<span data-ttu-id="73b58-119">下列 XML 定義閒置設定，指出當閒置條件迴圈時，不應重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="73b58-119">The following XML defines an idle setting that indicates that the task should not be restarted when the idle condition cycles.</span></span>


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="73b58-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="73b58-120">Requirements</span></span>



| <span data-ttu-id="73b58-121">需求</span><span class="sxs-lookup"><span data-stu-id="73b58-121">Requirement</span></span> | <span data-ttu-id="73b58-122">值</span><span class="sxs-lookup"><span data-stu-id="73b58-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="73b58-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73b58-123">Minimum supported client</span></span><br/> | <span data-ttu-id="73b58-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73b58-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="73b58-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73b58-125">Minimum supported server</span></span><br/> | <span data-ttu-id="73b58-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73b58-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73b58-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73b58-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b58-128">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="73b58-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="73b58-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="73b58-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





