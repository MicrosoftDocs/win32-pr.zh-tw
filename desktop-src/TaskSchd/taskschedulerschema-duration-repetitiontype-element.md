---
title: 持續時間 (repetitionType) 元素
description: 指定重複模式的時間長度。
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Duration 元素工作排程器
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317507"
---
# <a name="duration-repetitiontype-element"></a><span data-ttu-id="9dac5-104">持續時間 (repetitionType) 元素</span><span class="sxs-lookup"><span data-stu-id="9dac5-104">Duration (repetitionType) Element</span></span>

<span data-ttu-id="9dac5-105">指定重複模式的時間長度。</span><span class="sxs-lookup"><span data-stu-id="9dac5-105">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="9dac5-106">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="9dac5-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="9dac5-107">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="9dac5-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="9dac5-108">如果未在持續時間內指定任何值，則會無限期地重複模式。</span><span class="sxs-lookup"><span data-stu-id="9dac5-108">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span> <span data-ttu-id="9dac5-109">最小值是一分鐘。</span><span class="sxs-lookup"><span data-stu-id="9dac5-109">The minimum value is one minute.</span></span>

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="9dac5-110">元素是由 [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="9dac5-110">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9dac5-111">父元素</span><span class="sxs-lookup"><span data-stu-id="9dac5-111">Parent element</span></span>



| <span data-ttu-id="9dac5-112">元素</span><span class="sxs-lookup"><span data-stu-id="9dac5-112">Element</span></span>                                                                      | <span data-ttu-id="9dac5-113">衍生自</span><span class="sxs-lookup"><span data-stu-id="9dac5-113">Derived from</span></span>                                                             | <span data-ttu-id="9dac5-114">Description</span><span class="sxs-lookup"><span data-stu-id="9dac5-114">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dac5-115">**重複**</span><span class="sxs-lookup"><span data-stu-id="9dac5-115">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="9dac5-116">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="9dac5-116">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="9dac5-117">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="9dac5-117">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9dac5-118">備註</span><span class="sxs-lookup"><span data-stu-id="9dac5-118">Remarks</span></span>

<span data-ttu-id="9dac5-119">若為腳本應用程式，則會使用 [**RepetitionPattern duration**](repetitionpattern-duration.md) 屬性指定模式的持續時間。</span><span class="sxs-lookup"><span data-stu-id="9dac5-119">For scripting applications, the duration of the pattern is specified using the [**RepetitionPattern.Duration**](repetitionpattern-duration.md) property.</span></span>

<span data-ttu-id="9dac5-120">若是 c + + 應用程式，則會使用 [**IRepetitionPattern：:D uration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) 屬性指定模式的持續時間。</span><span class="sxs-lookup"><span data-stu-id="9dac5-120">For C++ applications, the duration of the pattern is specified using the [**IRepetitionPattern::Duration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9dac5-121">範例</span><span class="sxs-lookup"><span data-stu-id="9dac5-121">Examples</span></span>

<span data-ttu-id="9dac5-122">下列 XML 會定義觸發程式的重複模式。</span><span class="sxs-lookup"><span data-stu-id="9dac5-122">The following XML defines a repetition pattern for a trigger.</span></span>


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
```



## <a name="requirements"></a><span data-ttu-id="9dac5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9dac5-123">Requirements</span></span>



| <span data-ttu-id="9dac5-124">需求</span><span class="sxs-lookup"><span data-stu-id="9dac5-124">Requirement</span></span> | <span data-ttu-id="9dac5-125">值</span><span class="sxs-lookup"><span data-stu-id="9dac5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9dac5-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9dac5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9dac5-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9dac5-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9dac5-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9dac5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9dac5-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9dac5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dac5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dac5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dac5-131">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="9dac5-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9dac5-132">工作排程器</span><span class="sxs-lookup"><span data-stu-id="9dac5-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





