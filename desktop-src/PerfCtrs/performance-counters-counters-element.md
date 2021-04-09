---
description: 識別檢測資訊清單之計數器區段的根節點。
ms.assetid: f16f432b-466f-4a3c-bc1b-e80b876a2511
title: 計數器元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11ced77890dba6d47f713642adf9b41d4b30f6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849285"
---
# <a name="counters-element"></a><span data-ttu-id="17930-103">計數器元素</span><span class="sxs-lookup"><span data-stu-id="17930-103">counters Element</span></span>

<span data-ttu-id="17930-104">識別檢測資訊清單之計數器區段的根節點。</span><span class="sxs-lookup"><span data-stu-id="17930-104">Identifies the root node of the counters section of an instrumentation manifest.</span></span>

``` syntax
<xs:element name="counters"
    type="man:counters"
>
    <xs:key name="uniqueprovGUID">
        <xs:selector
            xpath="./man:provider"
         />
        <xs:field
            xpath="@providerGuid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetGUID">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@guid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetURI">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetName">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@name"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:key>
    <xs:unique name="uniqueCounterSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:unique>
    <xs:key name="uniqueCounterURI">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
</xs:element>
```

## <a name="remarks"></a><span data-ttu-id="17930-105">備註</span><span class="sxs-lookup"><span data-stu-id="17930-105">Remarks</span></span>

<span data-ttu-id="17930-106">這個元素的父節點是資訊清單的 [**檢測**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype) 元素。</span><span class="sxs-lookup"><span data-stu-id="17930-106">This element's parent node is the [**instrumentation**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype) element of the manifest.</span></span>

## <a name="requirements"></a><span data-ttu-id="17930-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="17930-107">Requirements</span></span>



| <span data-ttu-id="17930-108">需求</span><span class="sxs-lookup"><span data-stu-id="17930-108">Requirement</span></span> | <span data-ttu-id="17930-109">值</span><span class="sxs-lookup"><span data-stu-id="17930-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="17930-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17930-110">Minimum supported client</span></span><br/> | <span data-ttu-id="17930-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17930-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="17930-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17930-112">Minimum supported server</span></span><br/> | <span data-ttu-id="17930-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17930-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

