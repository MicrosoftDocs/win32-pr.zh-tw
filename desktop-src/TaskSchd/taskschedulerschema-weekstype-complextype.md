---
title: weeksType 複雜類型
description: 定義 Week 元素的子專案和排序資訊。
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- weeksType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 597cc72c043a478a414187f63a9aa89516dee658
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105348"
---
# <a name="weekstype-complex-type"></a><span data-ttu-id="105a7-104">weeksType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="105a7-104">weeksType Complex Type</span></span>

<span data-ttu-id="105a7-105">定義 [**Week**](taskschedulerschema-week-weekstype-element.md) 元素的子專案和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="105a7-105">Defines the child element and sequencing information for the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="105a7-106">子元素</span><span class="sxs-lookup"><span data-stu-id="105a7-106">Child elements</span></span>



| <span data-ttu-id="105a7-107">元素</span><span class="sxs-lookup"><span data-stu-id="105a7-107">Element</span></span>                                                    | <span data-ttu-id="105a7-108">類型</span><span class="sxs-lookup"><span data-stu-id="105a7-108">Type</span></span>                                                        | <span data-ttu-id="105a7-109">Description</span><span class="sxs-lookup"><span data-stu-id="105a7-109">Description</span></span>                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="105a7-110">**週**</span><span class="sxs-lookup"><span data-stu-id="105a7-110">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="105a7-111">**weekType**</span><span class="sxs-lookup"><span data-stu-id="105a7-111">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="105a7-112">指定執行工作的周。</span><span class="sxs-lookup"><span data-stu-id="105a7-112">Specifies the week in which the task is run.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="105a7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="105a7-113">Requirements</span></span>



| <span data-ttu-id="105a7-114">需求</span><span class="sxs-lookup"><span data-stu-id="105a7-114">Requirement</span></span> | <span data-ttu-id="105a7-115">值</span><span class="sxs-lookup"><span data-stu-id="105a7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="105a7-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="105a7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="105a7-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="105a7-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="105a7-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="105a7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="105a7-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="105a7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="105a7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="105a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="105a7-121">工作排程器</span><span class="sxs-lookup"><span data-stu-id="105a7-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





