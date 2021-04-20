---
title: 間隔 (repetitionType) 元素
description: 指定工作每次重新開機之間的時間量。
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
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
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734193"
---
# <a name="interval-repetitiontype-element"></a><span data-ttu-id="b1a67-104">間隔 (repetitionType) 元素</span><span class="sxs-lookup"><span data-stu-id="b1a67-104">Interval (repetitionType) Element</span></span>

<span data-ttu-id="b1a67-105">指定工作每次重新開機之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="b1a67-105">Specifies the amount of time between each restart of the task.</span></span> <span data-ttu-id="b1a67-106">此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，"PT5M" 為5分鐘、"PT1H" 為1小時，而 "PT20M" 為20分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="b1a67-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="b1a67-107">允許的時間上限為31天，而允許的最短時間為1分鐘。</span><span class="sxs-lookup"><span data-stu-id="b1a67-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

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

<span data-ttu-id="b1a67-108">元素是由 [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="b1a67-108">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b1a67-109">父元素</span><span class="sxs-lookup"><span data-stu-id="b1a67-109">Parent element</span></span>



| <span data-ttu-id="b1a67-110">元素</span><span class="sxs-lookup"><span data-stu-id="b1a67-110">Element</span></span>                                                                      | <span data-ttu-id="b1a67-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="b1a67-111">Derived from</span></span>                                                             | <span data-ttu-id="b1a67-112">Description</span><span class="sxs-lookup"><span data-stu-id="b1a67-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1a67-113">**重複**</span><span class="sxs-lookup"><span data-stu-id="b1a67-113">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="b1a67-114">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="b1a67-114">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="b1a67-115">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="b1a67-115">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b1a67-116">備註</span><span class="sxs-lookup"><span data-stu-id="b1a67-116">Remarks</span></span>

<span data-ttu-id="b1a67-117">針對腳本開發，重複模式的間隔是使用 [**RepetitionPattern. interval**](repetitionpattern-interval.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="b1a67-117">For scripting development, the interval of the repetition pattern is specified using the [**RepetitionPattern.Interval**](repetitionpattern-interval.md) property.</span></span>

<span data-ttu-id="b1a67-118">針對 c + + 開發，會使用 [**IRepetitionPattern：： interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) 屬性指定重複模式的間隔。</span><span class="sxs-lookup"><span data-stu-id="b1a67-118">For C++ development, the interval of the repetition pattern is specified using the [**IRepetitionPattern::Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b1a67-119">範例</span><span class="sxs-lookup"><span data-stu-id="b1a67-119">Examples</span></span>

<span data-ttu-id="b1a67-120">如需使用重複間隔之工作的 XML 完整範例，請參閱 [ (xml) 的每日觸發程式範例 ](daily-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a67-120">For a complete example of the XML for a task that uses a repetition interval, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a67-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1a67-121">Requirements</span></span>



| <span data-ttu-id="b1a67-122">需求</span><span class="sxs-lookup"><span data-stu-id="b1a67-122">Requirement</span></span> | <span data-ttu-id="b1a67-123">值</span><span class="sxs-lookup"><span data-stu-id="b1a67-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1a67-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1a67-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a67-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1a67-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b1a67-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1a67-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a67-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1a67-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1a67-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1a67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a67-129">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="b1a67-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b1a67-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="b1a67-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





