---
title: repetitionType 複雜類型
description: 定義重複 (triggerBaseType) 元素的子項目和順序資訊。
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- repetitionType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa9ee8c08a79f5db053b772c86929f98a72f011c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384997"
---
# <a name="repetitiontype-complex-type"></a><span data-ttu-id="3ec92-104">repetitionType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="3ec92-104">repetitionType Complex Type</span></span>

<span data-ttu-id="3ec92-105">定義 [**重複 (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) 元素的子項目和順序資訊。</span><span class="sxs-lookup"><span data-stu-id="3ec92-105">Defines the child elements and sequence information for the [**Repetition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
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
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3ec92-106">子元素</span><span class="sxs-lookup"><span data-stu-id="3ec92-106">Child elements</span></span>



| <span data-ttu-id="3ec92-107">元素</span><span class="sxs-lookup"><span data-stu-id="3ec92-107">Element</span></span>                                                                                   | <span data-ttu-id="3ec92-108">類型</span><span class="sxs-lookup"><span data-stu-id="3ec92-108">Type</span></span>    | <span data-ttu-id="3ec92-109">Description</span><span class="sxs-lookup"><span data-stu-id="3ec92-109">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ec92-110">**持續時間**</span><span class="sxs-lookup"><span data-stu-id="3ec92-110">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   |         | <span data-ttu-id="3ec92-111">指定重複模式的時間長度。</span><span class="sxs-lookup"><span data-stu-id="3ec92-111">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="3ec92-112">如果未指定任何值，則會無限期地重複模式。</span><span class="sxs-lookup"><span data-stu-id="3ec92-112">If no value is specified, the pattern is repeated indefinitely.</span></span><br/> |
| [<span data-ttu-id="3ec92-113">**間隔**</span><span class="sxs-lookup"><span data-stu-id="3ec92-113">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   |         | <span data-ttu-id="3ec92-114">指定工作每次重新開機之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="3ec92-114">Specifies the amount of time between each restart of the task.</span></span><br/>                                              |
| [<span data-ttu-id="3ec92-115">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="3ec92-115">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="3ec92-116">boolean</span><span class="sxs-lookup"><span data-stu-id="3ec92-116">boolean</span></span> | <span data-ttu-id="3ec92-117">指定在重複模式期間結束時停止執行中的工作實例。</span><span class="sxs-lookup"><span data-stu-id="3ec92-117">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="3ec92-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ec92-118">Requirements</span></span>



| <span data-ttu-id="3ec92-119">需求</span><span class="sxs-lookup"><span data-stu-id="3ec92-119">Requirement</span></span> | <span data-ttu-id="3ec92-120">值</span><span class="sxs-lookup"><span data-stu-id="3ec92-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ec92-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ec92-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec92-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec92-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ec92-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ec92-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec92-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ec92-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ec92-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ec92-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec92-126">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="3ec92-126">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3ec92-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="3ec92-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





