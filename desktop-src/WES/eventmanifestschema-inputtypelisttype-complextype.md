---
title: InputTypeListType 複雜類型
description: 定義輸入類型的清單。
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- InputTypeListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106037"
---
# <a name="inputtypelisttype-complex-type"></a><span data-ttu-id="ce2b9-104">InputTypeListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="ce2b9-104">InputTypeListType Complex Type</span></span>

<span data-ttu-id="ce2b9-105">定義輸入類型的清單。</span><span class="sxs-lookup"><span data-stu-id="ce2b9-105">Defines a list of input types.</span></span>

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ce2b9-106">子元素</span><span class="sxs-lookup"><span data-stu-id="ce2b9-106">Child elements</span></span>



| <span data-ttu-id="ce2b9-107">元素</span><span class="sxs-lookup"><span data-stu-id="ce2b9-107">Element</span></span>                                                                | <span data-ttu-id="ce2b9-108">類型</span><span class="sxs-lookup"><span data-stu-id="ce2b9-108">Type</span></span>                                                           | <span data-ttu-id="ce2b9-109">Description</span><span class="sxs-lookup"><span data-stu-id="ce2b9-109">Description</span></span>                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="ce2b9-110">**inType**</span><span class="sxs-lookup"><span data-stu-id="ce2b9-110">**inType**</span></span>](eventmanifestschema-intype-inputtypelisttype-element.md) | [<span data-ttu-id="ce2b9-111">**InputType**</span><span class="sxs-lookup"><span data-stu-id="ce2b9-111">**InputType**</span></span>](eventmanifestschema-inputtype-complextype.md) | <span data-ttu-id="ce2b9-112">定義輸入類型。</span><span class="sxs-lookup"><span data-stu-id="ce2b9-112">Defines an input type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ce2b9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce2b9-113">Requirements</span></span>



| <span data-ttu-id="ce2b9-114">需求</span><span class="sxs-lookup"><span data-stu-id="ce2b9-114">Requirement</span></span> | <span data-ttu-id="ce2b9-115">值</span><span class="sxs-lookup"><span data-stu-id="ce2b9-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce2b9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce2b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2b9-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce2b9-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce2b9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce2b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2b9-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce2b9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





