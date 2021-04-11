---
title: 相互關聯 (SystemPropertiesType) 元素
description: 取用者可用來將相關事件群組在一起的活動識別碼。
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- 相互關聯元素 EventLog
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934825"
---
# <a name="correlation-systempropertiestype-element"></a><span data-ttu-id="2eb30-104">相互關聯 (SystemPropertiesType) 元素</span><span class="sxs-lookup"><span data-stu-id="2eb30-104">Correlation (SystemPropertiesType) Element</span></span>

<span data-ttu-id="2eb30-105">取用者可用來將相關事件群組在一起的活動識別碼。</span><span class="sxs-lookup"><span data-stu-id="2eb30-105">The activity identifiers that consumers can use to group related events together.</span></span>

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2eb30-106">相互 **關聯** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="2eb30-106">The **Correlation** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="2eb30-107">屬性</span><span class="sxs-lookup"><span data-stu-id="2eb30-107">Attributes</span></span>



| <span data-ttu-id="2eb30-108">名稱</span><span class="sxs-lookup"><span data-stu-id="2eb30-108">Name</span></span>              | <span data-ttu-id="2eb30-109">類型</span><span class="sxs-lookup"><span data-stu-id="2eb30-109">Type</span></span>                                                | <span data-ttu-id="2eb30-110">Description</span><span class="sxs-lookup"><span data-stu-id="2eb30-110">Description</span></span>                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb30-111">ActivityID</span><span class="sxs-lookup"><span data-stu-id="2eb30-111">ActivityID</span></span>        | [<span data-ttu-id="2eb30-112">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="2eb30-112">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="2eb30-113">識別目前活動的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2eb30-113">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="2eb30-114">以此識別碼發佈的事件是相同活動的一部分。</span><span class="sxs-lookup"><span data-stu-id="2eb30-114">The events that are published with this identifier are part of the same activity.</span></span><br/>                              |
| <span data-ttu-id="2eb30-115">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="2eb30-115">RelatedActivityID</span></span> | [<span data-ttu-id="2eb30-116">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="2eb30-116">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="2eb30-117">全域唯一識別碼，用來識別要將控制項傳送至其中的活動。</span><span class="sxs-lookup"><span data-stu-id="2eb30-117">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="2eb30-118">相關事件接著會有此識別碼作為其 ActivityID 識別碼。</span><span class="sxs-lookup"><span data-stu-id="2eb30-118">The related events would then have this identifier as their ActivityID identifier.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2eb30-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eb30-119">Requirements</span></span>



| <span data-ttu-id="2eb30-120">需求</span><span class="sxs-lookup"><span data-stu-id="2eb30-120">Requirement</span></span> | <span data-ttu-id="2eb30-121">值</span><span class="sxs-lookup"><span data-stu-id="2eb30-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2eb30-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2eb30-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb30-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eb30-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2eb30-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2eb30-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb30-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eb30-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2eb30-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2eb30-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="2eb30-127">**父元素**</span><span class="sxs-lookup"><span data-stu-id="2eb30-127">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="2eb30-128">**系統 (的系統事件)**</span><span class="sxs-lookup"><span data-stu-id="2eb30-128">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





