---
title: MaintenanceSettings (maintenanceSettingsType) 元素
description: 指定工作排程器在自動維護期間如何執行工作。
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- MaintenanceSettings 元素工作排程器
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105216"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a><span data-ttu-id="c315e-104">MaintenanceSettings (maintenanceSettingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="c315e-104">MaintenanceSettings (maintenanceSettingsType) Element</span></span>

<span data-ttu-id="c315e-105">指定工作排程器在自動維護期間如何執行工作。</span><span class="sxs-lookup"><span data-stu-id="c315e-105">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span>

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="c315e-106">**MaintenanceSettings** 元素是由 [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c315e-106">The **MaintenanceSettings** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c315e-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c315e-107">Parent element</span></span>



| <span data-ttu-id="c315e-108">元素</span><span class="sxs-lookup"><span data-stu-id="c315e-108">Element</span></span>                                                           | <span data-ttu-id="c315e-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c315e-109">Derived from</span></span>                                                         | <span data-ttu-id="c315e-110">Description</span><span class="sxs-lookup"><span data-stu-id="c315e-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c315e-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="c315e-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c315e-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c315e-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c315e-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="c315e-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c315e-114">子元素</span><span class="sxs-lookup"><span data-stu-id="c315e-114">Child elements</span></span>



| <span data-ttu-id="c315e-115">元素</span><span class="sxs-lookup"><span data-stu-id="c315e-115">Element</span></span>                                                    | <span data-ttu-id="c315e-116">類型</span><span class="sxs-lookup"><span data-stu-id="c315e-116">Type</span></span>    | <span data-ttu-id="c315e-117">Description</span><span class="sxs-lookup"><span data-stu-id="c315e-117">Description</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c315e-118">**期限**</span><span class="sxs-lookup"><span data-stu-id="c315e-118">**Deadline**</span></span>](taskschedulerschema-deadline-element.md)   |         | <span data-ttu-id="c315e-119">指定當工作排程器在正常維護期間無法完成時，在緊急自動維護期間，工作排程器將嘗試啟動工作的時間量。</span><span class="sxs-lookup"><span data-stu-id="c315e-119">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span> <br/> |
| [<span data-ttu-id="c315e-120">**獨佔**</span><span class="sxs-lookup"><span data-stu-id="c315e-120">**Exclusive**</span></span>](taskschedulerschema-exclusive-element.md) | <span data-ttu-id="c315e-121">boolean</span><span class="sxs-lookup"><span data-stu-id="c315e-121">boolean</span></span> | <span data-ttu-id="c315e-122">如果設定為 true，則工作將會在其他維護工作中以獨佔方式啟動。</span><span class="sxs-lookup"><span data-stu-id="c315e-122">If set to true, the task will be started exclusively among other maintenance tasks.</span></span> <br/>                                                                                                 |
| [<span data-ttu-id="c315e-123">**期間**</span><span class="sxs-lookup"><span data-stu-id="c315e-123">**Period**</span></span>](taskschedulerschema-period-element.md)       |         | <span data-ttu-id="c315e-124">指定在自動維護期間必須啟動工作的頻率。</span><span class="sxs-lookup"><span data-stu-id="c315e-124">Specifies how often the task needs to be started during Automatic maintenance.</span></span> <br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="c315e-125">備註</span><span class="sxs-lookup"><span data-stu-id="c315e-125">Remarks</span></span>

<span data-ttu-id="c315e-126">針對 c + + 程式設計，此閒置設定是使用 [**ITaskSettings3：： MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="c315e-126">For C++ programming, this idle setting is specified using the [**ITaskSettings3::MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c315e-127">範例</span><span class="sxs-lookup"><span data-stu-id="c315e-127">Examples</span></span>

<span data-ttu-id="c315e-128">下列 XML 定義的設定元素，會指示工作排程器在定期自動維護期間的5天內執行工作一次，如果在15天內失敗，則在緊急自動維護期間開始嘗試工作。</span><span class="sxs-lookup"><span data-stu-id="c315e-128">The following XML defines a settings element that instructs Task Scheduler to execute task once in 5 days during regular Automatic maintenance and if failed for 15 days, start attempting the task during the emergency Automatic maintenance.</span></span>


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="c315e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c315e-129">Requirements</span></span>



| <span data-ttu-id="c315e-130">需求</span><span class="sxs-lookup"><span data-stu-id="c315e-130">Requirement</span></span> | <span data-ttu-id="c315e-131">值</span><span class="sxs-lookup"><span data-stu-id="c315e-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c315e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c315e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c315e-133">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c315e-133">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="c315e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c315e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c315e-135">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c315e-135">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c315e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c315e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c315e-137">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="c315e-137">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c315e-138">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c315e-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





