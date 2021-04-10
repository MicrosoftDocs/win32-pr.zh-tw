---
title: 間隔 (restartType) 元素
description: 指定工作排程器將嘗試重新開機工作的時間長度。
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Interval 元素工作排程器
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c97e754e0b29a43d6ba419bd806404fe1b85b2b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934015"
---
# <a name="interval-restarttype-element"></a><span data-ttu-id="4cc17-104">間隔 (restartType) 元素</span><span class="sxs-lookup"><span data-stu-id="4cc17-104">Interval (restartType) Element</span></span>

<span data-ttu-id="4cc17-105">指定工作排程器將嘗試重新開機工作的時間長度。</span><span class="sxs-lookup"><span data-stu-id="4cc17-105">Specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="4cc17-106">此字串的格式為 P <days> DT <hours> H <minutes> M <seconds> S (例如，"PT5M" 為5分鐘、"PT1H" 為1小時，而 "PT20M" 為20分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="4cc17-106">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="4cc17-107">允許的時間上限為31天，而允許的最短時間為1分鐘。</span><span class="sxs-lookup"><span data-stu-id="4cc17-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="4cc17-108">元素是由 [**restartType**](taskschedulerschema-restarttype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="4cc17-108">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4cc17-109">父元素</span><span class="sxs-lookup"><span data-stu-id="4cc17-109">Parent element</span></span>



| <span data-ttu-id="4cc17-110">元素</span><span class="sxs-lookup"><span data-stu-id="4cc17-110">Element</span></span>                                                                               | <span data-ttu-id="4cc17-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="4cc17-111">Derived from</span></span>                                                       | <span data-ttu-id="4cc17-112">Description</span><span class="sxs-lookup"><span data-stu-id="4cc17-112">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cc17-113">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="4cc17-113">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="4cc17-114">**restartType**</span><span class="sxs-lookup"><span data-stu-id="4cc17-114">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="4cc17-115">指定當工作因為任何原因而失敗時，工作排程器將嘗試重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="4cc17-115">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4cc17-116">備註</span><span class="sxs-lookup"><span data-stu-id="4cc17-116">Remarks</span></span>

<span data-ttu-id="4cc17-117">如果指定這個元素，則也必須指定 [**Count**](taskschedulerschema-count-restarttype-element.md) 元素，以告知工作排程器應該嘗試重新開機工作的次數。</span><span class="sxs-lookup"><span data-stu-id="4cc17-117">If this element is specified, the [**Count**](taskschedulerschema-count-restarttype-element.md) element must also be specified to tell the Task Scheduler how many times it should try to restart the task.</span></span>

<span data-ttu-id="4cc17-118">針對 c + + 開發，請參閱 [**ITaskSettings 的 RestartInterval 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)。</span><span class="sxs-lookup"><span data-stu-id="4cc17-118">For C++ development, see [**RestartInterval Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span></span>

<span data-ttu-id="4cc17-119">如需腳本開發，請參閱 [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md)。</span><span class="sxs-lookup"><span data-stu-id="4cc17-119">For script development, see [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc17-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cc17-120">Requirements</span></span>



| <span data-ttu-id="4cc17-121">需求</span><span class="sxs-lookup"><span data-stu-id="4cc17-121">Requirement</span></span> | <span data-ttu-id="4cc17-122">值</span><span class="sxs-lookup"><span data-stu-id="4cc17-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4cc17-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cc17-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4cc17-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cc17-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4cc17-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cc17-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4cc17-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cc17-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4cc17-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cc17-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc17-128">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="4cc17-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





