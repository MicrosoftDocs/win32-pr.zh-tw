---
title: TypeListType 複雜類型
description: 定義在資訊清單中使用的類型。
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- TypeListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965315"
---
# <a name="typelisttype-complex-type"></a><span data-ttu-id="fca02-104">TypeListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="fca02-104">TypeListType Complex Type</span></span>

<span data-ttu-id="fca02-105">定義在資訊清單中使用的類型。</span><span class="sxs-lookup"><span data-stu-id="fca02-105">Defines the types that are used in the manifest.</span></span>

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="fca02-106">子元素</span><span class="sxs-lookup"><span data-stu-id="fca02-106">Child elements</span></span>



| <span data-ttu-id="fca02-107">元素</span><span class="sxs-lookup"><span data-stu-id="fca02-107">Element</span></span>                                                               | <span data-ttu-id="fca02-108">類型</span><span class="sxs-lookup"><span data-stu-id="fca02-108">Type</span></span>                                                                           | <span data-ttu-id="fca02-109">Description</span><span class="sxs-lookup"><span data-stu-id="fca02-109">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fca02-110">**inTypes**</span><span class="sxs-lookup"><span data-stu-id="fca02-110">**inTypes**</span></span>](eventmanifestschema-intypes-typelisttype-element.md)   | [<span data-ttu-id="fca02-111">**InputTypeListType**</span><span class="sxs-lookup"><span data-stu-id="fca02-111">**InputTypeListType**</span></span>](eventmanifestschema-inputtypelisttype-complextype.md) | <span data-ttu-id="fca02-112">定義輸入資料類型的清單。</span><span class="sxs-lookup"><span data-stu-id="fca02-112">Defines a list of input data types.</span></span><br/>                                                              |
| [<span data-ttu-id="fca02-113">**xmlTypes**</span><span class="sxs-lookup"><span data-stu-id="fca02-113">**xmlTypes**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md) | [<span data-ttu-id="fca02-114">**XmlTypeListType**</span><span class="sxs-lookup"><span data-stu-id="fca02-114">**XmlTypeListType**</span></span>](eventmanifestschema-xmltypelisttype-complextype.md)     | <span data-ttu-id="fca02-115">定義清單輸出類型，服務會使用此類型來判斷如何轉譯輸入資料類型。</span><span class="sxs-lookup"><span data-stu-id="fca02-115">Defines a list output types that the service uses to determine how to render an input data type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fca02-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fca02-116">Requirements</span></span>



| <span data-ttu-id="fca02-117">需求</span><span class="sxs-lookup"><span data-stu-id="fca02-117">Requirement</span></span> | <span data-ttu-id="fca02-118">值</span><span class="sxs-lookup"><span data-stu-id="fca02-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fca02-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fca02-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fca02-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fca02-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fca02-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fca02-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fca02-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fca02-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





