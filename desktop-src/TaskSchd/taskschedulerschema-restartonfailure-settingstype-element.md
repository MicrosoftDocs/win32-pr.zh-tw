---
title: RestartOnFailure (settingsType) 元素
description: 指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- RestartOnFailure 元素工作排程器
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187317"
---
# <a name="restartonfailure-settingstype-element"></a><span data-ttu-id="b81f5-104">RestartOnFailure (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="b81f5-104">RestartOnFailure (settingsType) Element</span></span>

<span data-ttu-id="b81f5-105">指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="b81f5-105">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span>

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

<span data-ttu-id="b81f5-106">**RestartOnFailure** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="b81f5-106">The **RestartOnFailure** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b81f5-107">父元素</span><span class="sxs-lookup"><span data-stu-id="b81f5-107">Parent element</span></span>



| <span data-ttu-id="b81f5-108">元素</span><span class="sxs-lookup"><span data-stu-id="b81f5-108">Element</span></span>                                                           | <span data-ttu-id="b81f5-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="b81f5-109">Derived from</span></span>                                                         | <span data-ttu-id="b81f5-110">Description</span><span class="sxs-lookup"><span data-stu-id="b81f5-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="b81f5-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="b81f5-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="b81f5-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="b81f5-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="b81f5-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="b81f5-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="b81f5-114">子元素</span><span class="sxs-lookup"><span data-stu-id="b81f5-114">Child elements</span></span>



| <span data-ttu-id="b81f5-115">元素</span><span class="sxs-lookup"><span data-stu-id="b81f5-115">Element</span></span>                                                              | <span data-ttu-id="b81f5-116">類型</span><span class="sxs-lookup"><span data-stu-id="b81f5-116">Type</span></span>         | <span data-ttu-id="b81f5-117">Description</span><span class="sxs-lookup"><span data-stu-id="b81f5-117">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b81f5-118">**計數**</span><span class="sxs-lookup"><span data-stu-id="b81f5-118">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       | <span data-ttu-id="b81f5-119">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="b81f5-119">unsignedByte</span></span> | <span data-ttu-id="b81f5-120">指定工作排程器將嘗試重新開機工作的次數。</span><span class="sxs-lookup"><span data-stu-id="b81f5-120">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span><br/> |
| [<span data-ttu-id="b81f5-121">**間隔**</span><span class="sxs-lookup"><span data-stu-id="b81f5-121">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) | <span data-ttu-id="b81f5-122">duration</span><span class="sxs-lookup"><span data-stu-id="b81f5-122">duration</span></span>     | <span data-ttu-id="b81f5-123">指定工作排程器將嘗試重新開機工作的時間長度。</span><span class="sxs-lookup"><span data-stu-id="b81f5-123">Specifies how long the Task Scheduler will attempt to restart the task.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="b81f5-124">備註</span><span class="sxs-lookup"><span data-stu-id="b81f5-124">Remarks</span></span>

<span data-ttu-id="b81f5-125">當應用程式指定工作設定時，這項資訊會透過 [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings)介面的 [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount)和 [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="b81f5-125">When an application specifies task settings, this information is accessed through the [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) and [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) properties of the [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) interface.</span></span> <span data-ttu-id="b81f5-126">針對腳本，這項資訊是透過 [**TaskSettings. RestartCount**](tasksettings-restartcount.md) 和 [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) 屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="b81f5-126">For scripting, this information is accessed through the [**TaskSettings.RestartCount**](tasksettings-restartcount.md) and [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md) properties.</span></span>

<span data-ttu-id="b81f5-127">這兩個子專案都必須設定為指定工作排程器重新開機工作的方式。</span><span class="sxs-lookup"><span data-stu-id="b81f5-127">Both child elements must be set to specify how the Task Scheduler restarts the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="b81f5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b81f5-128">Requirements</span></span>



| <span data-ttu-id="b81f5-129">需求</span><span class="sxs-lookup"><span data-stu-id="b81f5-129">Requirement</span></span> | <span data-ttu-id="b81f5-130">值</span><span class="sxs-lookup"><span data-stu-id="b81f5-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b81f5-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b81f5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b81f5-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b81f5-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b81f5-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b81f5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b81f5-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b81f5-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b81f5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b81f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b81f5-136">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="b81f5-136">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





