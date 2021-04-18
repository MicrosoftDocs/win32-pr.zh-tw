---
title: Exclusive 元素
description: 指出工作排程器是否必須在獨佔模式的自動維護期間啟動工作。
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- 專有元素工作排程器
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965282"
---
# <a name="exclusive-element"></a><span data-ttu-id="a7a86-104">Exclusive 元素</span><span class="sxs-lookup"><span data-stu-id="a7a86-104">Exclusive Element</span></span>

<span data-ttu-id="a7a86-105">指出工作排程器是否必須在獨佔模式的自動維護期間啟動工作。</span><span class="sxs-lookup"><span data-stu-id="a7a86-105">Indicates whether the Task scheduler must start the task during the Automatic maintenance in exclusive mode.</span></span>

<span data-ttu-id="a7a86-106">獨佔性只會在其他維護工作之間獲得保證，且不會授與工作的任何順序優先權。</span><span class="sxs-lookup"><span data-stu-id="a7a86-106">The exclusivity is guaranteed only between other maintenance tasks and doesn't grant any ordering priority of the task.</span></span> <span data-ttu-id="a7a86-107">如果未指定獨佔性，工作就會與其他維護工作平行啟動。</span><span class="sxs-lookup"><span data-stu-id="a7a86-107">If exclusivity is not specified, the task is started in parallel with other maintenance tasks.</span></span>

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="a7a86-108">**Exclusive** 元素是由 [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="a7a86-108">The **Exclusive** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a7a86-109">父元素</span><span class="sxs-lookup"><span data-stu-id="a7a86-109">Parent element</span></span>



| <span data-ttu-id="a7a86-110">元素</span><span class="sxs-lookup"><span data-stu-id="a7a86-110">Element</span></span>                                                                                                                          | <span data-ttu-id="a7a86-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="a7a86-111">Derived from</span></span>                                                                               | <span data-ttu-id="a7a86-112">Description</span><span class="sxs-lookup"><span data-stu-id="a7a86-112">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7a86-113">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="a7a86-113">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="a7a86-114">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="a7a86-114">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="a7a86-115">指定工作排程器將在自動維護期間用來啟動工作的工作設定。</span><span class="sxs-lookup"><span data-stu-id="a7a86-115">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a7a86-116">備註</span><span class="sxs-lookup"><span data-stu-id="a7a86-116">Remarks</span></span>

<span data-ttu-id="a7a86-117">若是 c + + 程式設計，則會使用 [**IMaintenanceSettings：： Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) 屬性來指定此閒置設定。</span><span class="sxs-lookup"><span data-stu-id="a7a86-117">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a7a86-118">範例</span><span class="sxs-lookup"><span data-stu-id="a7a86-118">Examples</span></span>

<span data-ttu-id="a7a86-119">下列 XML 會定義期限需求設為15天的維護工作。</span><span class="sxs-lookup"><span data-stu-id="a7a86-119">The following XML defines maintenance task with deadline requirement set to 15 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="a7a86-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7a86-120">Requirements</span></span>



| <span data-ttu-id="a7a86-121">需求</span><span class="sxs-lookup"><span data-stu-id="a7a86-121">Requirement</span></span> | <span data-ttu-id="a7a86-122">值</span><span class="sxs-lookup"><span data-stu-id="a7a86-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7a86-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7a86-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a86-124">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7a86-124">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="a7a86-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7a86-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a86-126">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7a86-126">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7a86-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7a86-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a86-128">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="a7a86-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a7a86-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="a7a86-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





