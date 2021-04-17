---
title: 持續時間 (idleSettingsType) 元素
description: 指定在執行工作之前，電腦必須處於閒置狀態的時間長度。
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
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
ms.openlocfilehash: 31ad092693c72dcc33357f4b7e21436e2cba8af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508432"
---
# <a name="duration-idlesettingstype-element"></a><span data-ttu-id="38dbb-104">持續時間 (idleSettingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="38dbb-104">Duration (idleSettingsType) Element</span></span>

<span data-ttu-id="38dbb-105">指定在執行工作之前，電腦必須處於閒置狀態的時間長度。</span><span class="sxs-lookup"><span data-stu-id="38dbb-105">Specifies how long the computer must be in an idle state before the task is run.</span></span> <span data-ttu-id="38dbb-106">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="38dbb-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="38dbb-107">最小值是一分鐘。</span><span class="sxs-lookup"><span data-stu-id="38dbb-107">The minimum value is one minute.</span></span> <span data-ttu-id="38dbb-108">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="38dbb-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Duration"
    default="PT10M"
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

<span data-ttu-id="38dbb-109">元素是由 [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="38dbb-109">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="38dbb-110">父元素</span><span class="sxs-lookup"><span data-stu-id="38dbb-110">Parent element</span></span>



| <span data-ttu-id="38dbb-111">元素</span><span class="sxs-lookup"><span data-stu-id="38dbb-111">Element</span></span>                                                                       | <span data-ttu-id="38dbb-112">衍生自</span><span class="sxs-lookup"><span data-stu-id="38dbb-112">Derived from</span></span>                                                                 | <span data-ttu-id="38dbb-113">Description</span><span class="sxs-lookup"><span data-stu-id="38dbb-113">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38dbb-114">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="38dbb-114">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="38dbb-115">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="38dbb-115">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="38dbb-116">指定當電腦處於閒置狀態時，工作排程器如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="38dbb-116">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="38dbb-117">備註</span><span class="sxs-lookup"><span data-stu-id="38dbb-117">Remarks</span></span>

<span data-ttu-id="38dbb-118">若為腳本程式設計，則會使用 [**IdleSettings. IdleDuration**](idlesettings-idleduration.md) 屬性來指定此閒置設定。</span><span class="sxs-lookup"><span data-stu-id="38dbb-118">For script programming, this idle setting is specified using the [**IdleSettings.IdleDuration**](idlesettings-idleduration.md) property.</span></span>

<span data-ttu-id="38dbb-119">針對 c + + 程式設計，此閒置設定是使用 [**IIdleSettings：： IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="38dbb-119">For C++ programming, this idle setting is specified using the [**IIdleSettings::IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="38dbb-120">範例</span><span class="sxs-lookup"><span data-stu-id="38dbb-120">Examples</span></span>

<span data-ttu-id="38dbb-121">下列 XML 會定義閒置設定，讓工作可以使用5分鐘來啟動。</span><span class="sxs-lookup"><span data-stu-id="38dbb-121">The following XML defines an idle setting that allows 5 minutes for the task to start.</span></span>


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="38dbb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="38dbb-122">Requirements</span></span>



| <span data-ttu-id="38dbb-123">需求</span><span class="sxs-lookup"><span data-stu-id="38dbb-123">Requirement</span></span> | <span data-ttu-id="38dbb-124">值</span><span class="sxs-lookup"><span data-stu-id="38dbb-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38dbb-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38dbb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="38dbb-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38dbb-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38dbb-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38dbb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="38dbb-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38dbb-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38dbb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38dbb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38dbb-130">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="38dbb-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="38dbb-131">工作排程器</span><span class="sxs-lookup"><span data-stu-id="38dbb-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





