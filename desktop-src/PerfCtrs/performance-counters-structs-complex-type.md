---
description: 定義包含計數器值的結構清單。
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: 結構複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976897"
---
# <a name="structs-complex-type"></a><span data-ttu-id="e8f63-103">結構複雜類型</span><span class="sxs-lookup"><span data-stu-id="e8f63-103">structs Complex Type</span></span>

<span data-ttu-id="e8f63-104">定義包含計數器值的結構清單。</span><span class="sxs-lookup"><span data-stu-id="e8f63-104">Defines a list of structures that contain counter values.</span></span>

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e8f63-105">子元素</span><span class="sxs-lookup"><span data-stu-id="e8f63-105">Child elements</span></span>



| <span data-ttu-id="e8f63-106">元素</span><span class="sxs-lookup"><span data-stu-id="e8f63-106">Element</span></span>    | <span data-ttu-id="e8f63-107">類型</span><span class="sxs-lookup"><span data-stu-id="e8f63-107">Type</span></span>                                                           | <span data-ttu-id="e8f63-108">Description</span><span class="sxs-lookup"><span data-stu-id="e8f63-108">Description</span></span>                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e8f63-109">**結構**</span><span class="sxs-lookup"><span data-stu-id="e8f63-109">**struct**</span></span> | [<span data-ttu-id="e8f63-110">**man： struct**</span><span class="sxs-lookup"><span data-stu-id="e8f63-110">**man:struct**</span></span>](performance-counters-struct-complex-type.md) | <span data-ttu-id="e8f63-111">包含計數器值之結構的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f63-111">The name of a structure that contains counter values.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e8f63-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8f63-112">Requirements</span></span>



| <span data-ttu-id="e8f63-113">需求</span><span class="sxs-lookup"><span data-stu-id="e8f63-113">Requirement</span></span> | <span data-ttu-id="e8f63-114">值</span><span class="sxs-lookup"><span data-stu-id="e8f63-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e8f63-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8f63-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e8f63-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8f63-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e8f63-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8f63-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e8f63-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8f63-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




