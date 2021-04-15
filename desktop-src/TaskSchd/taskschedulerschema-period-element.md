---
title: Period 元素
description: 指定在自動維護期間必須啟動工作的頻率。
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Period 元素工作排程器
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466984"
---
# <a name="period-element"></a><span data-ttu-id="dc4af-104">Period 元素</span><span class="sxs-lookup"><span data-stu-id="dc4af-104">Period Element</span></span>

<span data-ttu-id="dc4af-105">指定在自動維護期間必須啟動工作的頻率。</span><span class="sxs-lookup"><span data-stu-id="dc4af-105">Specifies how often the task needs to be started during Automatic maintenance.</span></span>

<span data-ttu-id="dc4af-106">此字串的格式為 *PnYnMnDTnHnMnS*，其中 *nY* 是年數，nm 是月數、 *nD* 是天、 *T* 是日期/時間分隔符號、 *nH* 是時數、 *nM* 為分鐘數，而 *nS* 是秒數 (例如，"PT5M" 指定5分鐘，而 "P1M4DT2H5M" 則指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="dc4af-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="dc4af-107">最小值是一分鐘。</span><span class="sxs-lookup"><span data-stu-id="dc4af-107">The minimum value is one minute.</span></span> <span data-ttu-id="dc4af-108">如需持續時間類型的詳細資訊，請參閱 [XML 架構第2部分：資料類型第二版](https://www.w3.org/TR/xmlschema-2/#duration)。</span><span class="sxs-lookup"><span data-stu-id="dc4af-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span>

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="dc4af-109">**Period** 元素是由 [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="dc4af-109">The **Period** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dc4af-110">父元素</span><span class="sxs-lookup"><span data-stu-id="dc4af-110">Parent element</span></span>



| <span data-ttu-id="dc4af-111">元素</span><span class="sxs-lookup"><span data-stu-id="dc4af-111">Element</span></span>                                                                                                                          | <span data-ttu-id="dc4af-112">衍生自</span><span class="sxs-lookup"><span data-stu-id="dc4af-112">Derived from</span></span>                                                                               | <span data-ttu-id="dc4af-113">Description</span><span class="sxs-lookup"><span data-stu-id="dc4af-113">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc4af-114">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="dc4af-114">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="dc4af-115">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="dc4af-115">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="dc4af-116">指定工作排程器將在自動維護期間用來啟動工作的工作設定。</span><span class="sxs-lookup"><span data-stu-id="dc4af-116">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dc4af-117">備註</span><span class="sxs-lookup"><span data-stu-id="dc4af-117">Remarks</span></span>

<span data-ttu-id="dc4af-118">若是 c + + 程式設計，則會使用 [**IMaintenanceSettings：:P eriod**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) 屬性來指定此閒置設定。</span><span class="sxs-lookup"><span data-stu-id="dc4af-118">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Period**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) property.</span></span>

## <a name="examples"></a><span data-ttu-id="dc4af-119">範例</span><span class="sxs-lookup"><span data-stu-id="dc4af-119">Examples</span></span>

<span data-ttu-id="dc4af-120">下列 XML 定義了週期性需求設為5天的維護工作。</span><span class="sxs-lookup"><span data-stu-id="dc4af-120">The following XML defines maintenance task with periodicity requirement set to 5 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="dc4af-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc4af-121">Requirements</span></span>



| <span data-ttu-id="dc4af-122">需求</span><span class="sxs-lookup"><span data-stu-id="dc4af-122">Requirement</span></span> | <span data-ttu-id="dc4af-123">值</span><span class="sxs-lookup"><span data-stu-id="dc4af-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc4af-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc4af-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dc4af-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc4af-125">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="dc4af-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc4af-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dc4af-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc4af-127">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc4af-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc4af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4af-129">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="dc4af-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dc4af-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="dc4af-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





