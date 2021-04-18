---
title: restartType 複雜類型
description: 定義 RestartOnFailure 元素的子項目和順序資訊。
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- restartType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509444"
---
# <a name="restarttype-complex-type"></a><span data-ttu-id="5fcd8-104">restartType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="5fcd8-104">restartType Complex Type</span></span>

<span data-ttu-id="5fcd8-105">定義 [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) 元素的子項目和順序資訊。</span><span class="sxs-lookup"><span data-stu-id="5fcd8-105">Defines the child elements and sequence information for the [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="restartType">
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
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5fcd8-106">子元素</span><span class="sxs-lookup"><span data-stu-id="5fcd8-106">Child elements</span></span>



| <span data-ttu-id="5fcd8-107">元素</span><span class="sxs-lookup"><span data-stu-id="5fcd8-107">Element</span></span>                                                              | <span data-ttu-id="5fcd8-108">類型</span><span class="sxs-lookup"><span data-stu-id="5fcd8-108">Type</span></span> | <span data-ttu-id="5fcd8-109">Description</span><span class="sxs-lookup"><span data-stu-id="5fcd8-109">Description</span></span>                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [<span data-ttu-id="5fcd8-110">**計數**</span><span class="sxs-lookup"><span data-stu-id="5fcd8-110">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       |      | <span data-ttu-id="5fcd8-111">重新開機工作的嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="5fcd8-111">Number of attempts to restart the task.</span></span><br/> |
| [<span data-ttu-id="5fcd8-112">**間隔**</span><span class="sxs-lookup"><span data-stu-id="5fcd8-112">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) |      | <span data-ttu-id="5fcd8-113">嘗試啟動工作的時間長度。</span><span class="sxs-lookup"><span data-stu-id="5fcd8-113">How long to try to start the task.</span></span><br/>      |



## <a name="requirements"></a><span data-ttu-id="5fcd8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fcd8-114">Requirements</span></span>



| <span data-ttu-id="5fcd8-115">需求</span><span class="sxs-lookup"><span data-stu-id="5fcd8-115">Requirement</span></span> | <span data-ttu-id="5fcd8-116">值</span><span class="sxs-lookup"><span data-stu-id="5fcd8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5fcd8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5fcd8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5fcd8-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fcd8-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5fcd8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5fcd8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5fcd8-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fcd8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fcd8-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fcd8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fcd8-122">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="5fcd8-122">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="5fcd8-123">工作排程器</span><span class="sxs-lookup"><span data-stu-id="5fcd8-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





