---
title: 期限元素
description: 指定工作排程器在緊急自動維護期間必須啟動工作的時間（如果在定期自動維護期間無法完成）。
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- 期限元素工作排程器
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685740"
---
# <a name="deadline-element"></a><span data-ttu-id="ab43d-104">期限元素</span><span class="sxs-lookup"><span data-stu-id="ab43d-104">Deadline Element</span></span>

<span data-ttu-id="ab43d-105">指定工作排程器在緊急自動維護期間必須啟動工作的時間（如果在定期自動維護期間無法完成）。</span><span class="sxs-lookup"><span data-stu-id="ab43d-105">Specifies when the Task scheduler must to start the task during emergency Automatic maintenance, if it failed to complete during regular Automatic maintenance.</span></span>

<span data-ttu-id="ab43d-106">此字串的格式為 *PnYnMnDTnHnMnS*，其中 *nY* 是年數，nm 是月數、 *nD* 是天、 *T* 是日期/時間分隔符號、 *nH* 是時數、 *nM* 為分鐘數，而 *nS* 是秒數 (例如，"PT5M" 指定5分鐘，而 "P1M4DT2H5M" 則指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="ab43d-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="ab43d-107">最小值是一分鐘。</span><span class="sxs-lookup"><span data-stu-id="ab43d-107">The minimum value is one minute.</span></span> <span data-ttu-id="ab43d-108">如需持續時間類型的詳細資訊，請參閱 [XML 架構第2部分：資料類型第二版](https://www.w3.org/TR/xmlschema-2/#duration)。</span><span class="sxs-lookup"><span data-stu-id="ab43d-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span> <span data-ttu-id="ab43d-109">工作可以使用的最短期限為1天。</span><span class="sxs-lookup"><span data-stu-id="ab43d-109">Minimum Deadline a task can use is 1 day.</span></span> <span data-ttu-id="ab43d-110">**期限** 元素的值應大於 [**Period**](taskschedulerschema-period-element.md)元素的值。</span><span class="sxs-lookup"><span data-stu-id="ab43d-110">The value of the **Deadline** element should be greater than the value of the [**Period**](taskschedulerschema-period-element.md) element.</span></span> <span data-ttu-id="ab43d-111">如果未指定期限，則不會在緊急自動維護期間啟動工作。</span><span class="sxs-lookup"><span data-stu-id="ab43d-111">If the deadline is not specified the task will not be started during emergency Automatic maintenance.</span></span>

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
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

<span data-ttu-id="ab43d-112">**期限** 元素是由 [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="ab43d-112">The **Deadline** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ab43d-113">父元素</span><span class="sxs-lookup"><span data-stu-id="ab43d-113">Parent element</span></span>



| <span data-ttu-id="ab43d-114">元素</span><span class="sxs-lookup"><span data-stu-id="ab43d-114">Element</span></span>                                                                                                                          | <span data-ttu-id="ab43d-115">衍生自</span><span class="sxs-lookup"><span data-stu-id="ab43d-115">Derived from</span></span>                                                                               | <span data-ttu-id="ab43d-116">Description</span><span class="sxs-lookup"><span data-stu-id="ab43d-116">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab43d-117">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="ab43d-117">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="ab43d-118">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="ab43d-118">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="ab43d-119">指定工作排程器將在自動維護期間用來啟動工作的工作設定。</span><span class="sxs-lookup"><span data-stu-id="ab43d-119">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ab43d-120">備註</span><span class="sxs-lookup"><span data-stu-id="ab43d-120">Remarks</span></span>

<span data-ttu-id="ab43d-121">若是 c + + 程式設計，則會使用 [**IMaintenanceSettings：:D eadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) 屬性來指定此閒置設定。</span><span class="sxs-lookup"><span data-stu-id="ab43d-121">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Deadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) property.</span></span>

## <a name="examples"></a><span data-ttu-id="ab43d-122">範例</span><span class="sxs-lookup"><span data-stu-id="ab43d-122">Examples</span></span>

<span data-ttu-id="ab43d-123">下列 XML 定義在三月執行工作的月份行事曆。</span><span class="sxs-lookup"><span data-stu-id="ab43d-123">The following XML defines a months calendar that runs the task in March.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="ab43d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab43d-124">Requirements</span></span>



| <span data-ttu-id="ab43d-125">需求</span><span class="sxs-lookup"><span data-stu-id="ab43d-125">Requirement</span></span> | <span data-ttu-id="ab43d-126">值</span><span class="sxs-lookup"><span data-stu-id="ab43d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab43d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab43d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ab43d-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab43d-128">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="ab43d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab43d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ab43d-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab43d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab43d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab43d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab43d-132">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="ab43d-132">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ab43d-133">工作排程器</span><span class="sxs-lookup"><span data-stu-id="ab43d-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





