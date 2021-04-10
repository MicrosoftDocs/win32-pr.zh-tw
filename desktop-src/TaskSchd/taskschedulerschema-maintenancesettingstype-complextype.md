---
title: maintenanceSettingsType 複雜類型
description: 定義 MaintenanceSettings 元素的子項目和排序資訊。
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- maintenanceSettingsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686223"
---
# <a name="maintenancesettingstype-complex-type"></a><span data-ttu-id="19ab0-104">maintenanceSettingsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="19ab0-104">maintenanceSettingsType Complex Type</span></span>

<span data-ttu-id="19ab0-105">定義 [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="19ab0-105">Defines the child elements and sequencing information for the [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="19ab0-106">子元素</span><span class="sxs-lookup"><span data-stu-id="19ab0-106">Child elements</span></span>



| <span data-ttu-id="19ab0-107">元素</span><span class="sxs-lookup"><span data-stu-id="19ab0-107">Element</span></span>                                                                        | <span data-ttu-id="19ab0-108">類型</span><span class="sxs-lookup"><span data-stu-id="19ab0-108">Type</span></span>    | <span data-ttu-id="19ab0-109">Description</span><span class="sxs-lookup"><span data-stu-id="19ab0-109">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19ab0-110">**期限**</span><span class="sxs-lookup"><span data-stu-id="19ab0-110">**Deadline**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | <span data-ttu-id="19ab0-111">指定當工作排程器在正常維護期間無法完成時，在緊急自動維護期間，工作排程器將嘗試啟動工作的時間量。</span><span class="sxs-lookup"><span data-stu-id="19ab0-111">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span><br/> |
| <span data-ttu-id="19ab0-112">**排除**</span><span class="sxs-lookup"><span data-stu-id="19ab0-112">**Exclusive**</span></span>                                                                  | <span data-ttu-id="19ab0-113">boolean</span><span class="sxs-lookup"><span data-stu-id="19ab0-113">boolean</span></span> | <span data-ttu-id="19ab0-114">如果設定為 true，則工作將會在其他維護工作中以獨佔方式啟動。</span><span class="sxs-lookup"><span data-stu-id="19ab0-114">If set to true, the task will be started exclusively among other maintenance tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="19ab0-115">**期間**</span><span class="sxs-lookup"><span data-stu-id="19ab0-115">**Period**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | <span data-ttu-id="19ab0-116">指定在自動維護期間必須啟動工作的頻率。</span><span class="sxs-lookup"><span data-stu-id="19ab0-116">Specifies how often the task needs to be started during Automatic maintenance.</span></span><br/>                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="19ab0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="19ab0-117">Requirements</span></span>



| <span data-ttu-id="19ab0-118">需求</span><span class="sxs-lookup"><span data-stu-id="19ab0-118">Requirement</span></span> | <span data-ttu-id="19ab0-119">值</span><span class="sxs-lookup"><span data-stu-id="19ab0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19ab0-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19ab0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="19ab0-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19ab0-121">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="19ab0-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19ab0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="19ab0-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19ab0-123">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19ab0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19ab0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ab0-125">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="19ab0-125">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="19ab0-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="19ab0-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





