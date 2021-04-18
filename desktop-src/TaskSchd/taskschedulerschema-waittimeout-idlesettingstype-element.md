---
title: WaitTimeout (idleSettingsType) 元素
description: 指定工作排程器將等候閒置條件發生的時間量。
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- WaitTimeout 元素工作排程器
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16f71a014358a8e0520274d1ff853cf6146aa05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509043"
---
# <a name="waittimeout-idlesettingstype-element"></a><span data-ttu-id="0c6fd-104">WaitTimeout (idleSettingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="0c6fd-104">WaitTimeout (idleSettingsType) Element</span></span>

<span data-ttu-id="0c6fd-105">指定工作排程器將等候閒置條件發生的時間量。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-105">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="0c6fd-106">如果未指定這個專案的值，工作排程器服務將會無限期地等候閒置的情況發生。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-106">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span> <span data-ttu-id="0c6fd-107">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="0c6fd-108">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="0c6fd-109">允許的最小時間是1分鐘。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-109">The minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="WaitTimeout"
    default="PT1H"
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

<span data-ttu-id="0c6fd-110">元素是由 [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-110">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0c6fd-111">父元素</span><span class="sxs-lookup"><span data-stu-id="0c6fd-111">Parent element</span></span>



| <span data-ttu-id="0c6fd-112">元素</span><span class="sxs-lookup"><span data-stu-id="0c6fd-112">Element</span></span>                                                                       | <span data-ttu-id="0c6fd-113">衍生自</span><span class="sxs-lookup"><span data-stu-id="0c6fd-113">Derived from</span></span>                                                                 | <span data-ttu-id="0c6fd-114">Description</span><span class="sxs-lookup"><span data-stu-id="0c6fd-114">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c6fd-115">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="0c6fd-115">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="0c6fd-116">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="0c6fd-116">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="0c6fd-117">指定當電腦處於閒置狀態時，工作排程器如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-117">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0c6fd-118">備註</span><span class="sxs-lookup"><span data-stu-id="0c6fd-118">Remarks</span></span>

<span data-ttu-id="0c6fd-119">針對腳本開發，此閒置設定是使用 [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-119">For script development, this idle setting is specified using the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property.</span></span>

<span data-ttu-id="0c6fd-120">針對 c + + 開發，此閒置設定是使用 [**IIdleSettings：： WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-120">For C++ development, this idle setting is specified using the [**IIdleSettings::WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) property.</span></span>

## <a name="examples"></a><span data-ttu-id="0c6fd-121">範例</span><span class="sxs-lookup"><span data-stu-id="0c6fd-121">Examples</span></span>

<span data-ttu-id="0c6fd-122">下列 XML 會定義閒置設定，以等候24小時進行閒置的條件。</span><span class="sxs-lookup"><span data-stu-id="0c6fd-122">The following XML defines an idle setting that waits 24 hours for an idle condition to occur.</span></span>


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="0c6fd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c6fd-123">Requirements</span></span>



| <span data-ttu-id="0c6fd-124">需求</span><span class="sxs-lookup"><span data-stu-id="0c6fd-124">Requirement</span></span> | <span data-ttu-id="0c6fd-125">值</span><span class="sxs-lookup"><span data-stu-id="0c6fd-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c6fd-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c6fd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0c6fd-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c6fd-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c6fd-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c6fd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0c6fd-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c6fd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c6fd-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c6fd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c6fd-131">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="0c6fd-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0c6fd-132">工作排程器</span><span class="sxs-lookup"><span data-stu-id="0c6fd-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





