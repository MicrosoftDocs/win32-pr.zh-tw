---
title: triggersType 複雜類型
description: 定義所有觸發程式元素的群組 (triggerGroup) 。
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- triggersType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968800"
---
# <a name="triggerstype-complex-type"></a><span data-ttu-id="0d439-104">triggersType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="0d439-104">triggersType Complex Type</span></span>

<span data-ttu-id="0d439-105">定義所有觸發程式元素的群組 ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) 。</span><span class="sxs-lookup"><span data-stu-id="0d439-105">Defines the group ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) for all trigger elements.</span></span> <span data-ttu-id="0d439-106">[**TriggerGroup**](taskschedulerschema-triggergroup-group.md)群組包含可在工作中使用的觸發程式清單。</span><span class="sxs-lookup"><span data-stu-id="0d439-106">The [**triggerGroup**](taskschedulerschema-triggergroup-group.md) group contains the list of triggers that can be used in a task.</span></span>

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="0d439-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d439-107">Requirements</span></span>



| <span data-ttu-id="0d439-108">需求</span><span class="sxs-lookup"><span data-stu-id="0d439-108">Requirement</span></span> | <span data-ttu-id="0d439-109">值</span><span class="sxs-lookup"><span data-stu-id="0d439-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d439-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d439-110">Minimum supported client</span></span><br/> | <span data-ttu-id="0d439-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d439-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0d439-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d439-112">Minimum supported server</span></span><br/> | <span data-ttu-id="0d439-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d439-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d439-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d439-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d439-115">工作排程器</span><span class="sxs-lookup"><span data-stu-id="0d439-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





