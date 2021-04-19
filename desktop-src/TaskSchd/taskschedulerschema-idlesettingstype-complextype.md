---
title: idleSettingsType 複雜類型
description: 定義 IdleSettings (settingsType) 元素的子項目和排序資訊。
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- idleSettingsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967326"
---
# <a name="idlesettingstype-complex-type"></a><span data-ttu-id="af621-104">idleSettingsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="af621-104">idleSettingsType Complex Type</span></span>

<span data-ttu-id="af621-105">定義 [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) 元素的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="af621-105">Defines the child elements and sequencing information for the [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
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
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="af621-106">子元素</span><span class="sxs-lookup"><span data-stu-id="af621-106">Child elements</span></span>



| <span data-ttu-id="af621-107">元素</span><span class="sxs-lookup"><span data-stu-id="af621-107">Element</span></span>                                                                                  | <span data-ttu-id="af621-108">類型</span><span class="sxs-lookup"><span data-stu-id="af621-108">Type</span></span>    | <span data-ttu-id="af621-109">Description</span><span class="sxs-lookup"><span data-stu-id="af621-109">Description</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af621-110">**持續時間**</span><span class="sxs-lookup"><span data-stu-id="af621-110">**Duration**</span></span>](taskschedulerschema-duration-idlesettingstype-element.md)                |         | <span data-ttu-id="af621-111">指定在閒置條件下，允許啟動工作的時間量。</span><span class="sxs-lookup"><span data-stu-id="af621-111">Specifies the amount of time allowed to start the task while in an idle condition.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="af621-112">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="af621-112">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="af621-113">boolean</span><span class="sxs-lookup"><span data-stu-id="af621-113">boolean</span></span> | <span data-ttu-id="af621-114">當閒置條件啟動時，就會立即重新開機工作。</span><span class="sxs-lookup"><span data-stu-id="af621-114">The task is restarted as soon as an idle condition starts.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="af621-115">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="af621-115">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="af621-116">boolean</span><span class="sxs-lookup"><span data-stu-id="af621-116">boolean</span></span> | <span data-ttu-id="af621-117">指定如果閒置條件在超過閒置持續時間之前結束，則工作會終止。</span><span class="sxs-lookup"><span data-stu-id="af621-117">Specifies that the task is terminated if the idle condition ends before the idle duration is exceeded.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="af621-118">**WaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="af621-118">**WaitTimeout**</span></span>](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | <span data-ttu-id="af621-119">指定等待閒置條件啟動的時間量。</span><span class="sxs-lookup"><span data-stu-id="af621-119">Specifies the amount of time to wait for an idle condition to start.</span></span> <span data-ttu-id="af621-120">如果未指定這個專案的值，工作排程器服務將會無限期地等候閒置的情況發生。</span><span class="sxs-lookup"><span data-stu-id="af621-120">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="af621-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="af621-121">Requirements</span></span>



| <span data-ttu-id="af621-122">需求</span><span class="sxs-lookup"><span data-stu-id="af621-122">Requirement</span></span> | <span data-ttu-id="af621-123">值</span><span class="sxs-lookup"><span data-stu-id="af621-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af621-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af621-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af621-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af621-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af621-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af621-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af621-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af621-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af621-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af621-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af621-129">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="af621-129">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="af621-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="af621-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





