---
title: 字串 (StringTableType) 元素
description: 定義當地語系化的字串。
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- string 元素 EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934563"
---
# <a name="string-stringtabletype-element"></a><span data-ttu-id="223b9-104">字串 (StringTableType) 元素</span><span class="sxs-lookup"><span data-stu-id="223b9-104">string (StringTableType) Element</span></span>

<span data-ttu-id="223b9-105">定義當地語系化的字串。</span><span class="sxs-lookup"><span data-stu-id="223b9-105">Defines a localized string.</span></span>

``` syntax
<xs:element name="string">
    <xs:complexType>
        <xs:attribute name="id"
            type="string"
            use="required"
         />
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="stringType"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="223b9-106">**String** 元素是由 [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="223b9-106">The **string** element is defined by the [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="223b9-107">屬性</span><span class="sxs-lookup"><span data-stu-id="223b9-107">Attributes</span></span>



| <span data-ttu-id="223b9-108">名稱</span><span class="sxs-lookup"><span data-stu-id="223b9-108">Name</span></span>       | <span data-ttu-id="223b9-109">類型</span><span class="sxs-lookup"><span data-stu-id="223b9-109">Type</span></span>   | <span data-ttu-id="223b9-110">描述</span><span class="sxs-lookup"><span data-stu-id="223b9-110">Description</span></span>                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="223b9-111">id</span><span class="sxs-lookup"><span data-stu-id="223b9-111">id</span></span>         | <span data-ttu-id="223b9-112">字串</span><span class="sxs-lookup"><span data-stu-id="223b9-112">string</span></span> | <span data-ttu-id="223b9-113">唯一識別字串資料表內之字串的識別碼。</span><span class="sxs-lookup"><span data-stu-id="223b9-113">An identifier that uniquely identifies the string within the string table.</span></span><br/> |
| <span data-ttu-id="223b9-114">stringType</span><span class="sxs-lookup"><span data-stu-id="223b9-114">stringType</span></span> | <span data-ttu-id="223b9-115">字串</span><span class="sxs-lookup"><span data-stu-id="223b9-115">string</span></span> | <span data-ttu-id="223b9-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="223b9-116">Not used.</span></span><br/>                                                                  |
| <span data-ttu-id="223b9-117">value</span><span class="sxs-lookup"><span data-stu-id="223b9-117">value</span></span>      | <span data-ttu-id="223b9-118">字串</span><span class="sxs-lookup"><span data-stu-id="223b9-118">string</span></span> | <span data-ttu-id="223b9-119">當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="223b9-119">The localized string.</span></span><br/>                                                      |



## <a name="requirements"></a><span data-ttu-id="223b9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="223b9-120">Requirements</span></span>



| <span data-ttu-id="223b9-121">需求</span><span class="sxs-lookup"><span data-stu-id="223b9-121">Requirement</span></span> | <span data-ttu-id="223b9-122">值</span><span class="sxs-lookup"><span data-stu-id="223b9-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="223b9-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="223b9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="223b9-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="223b9-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="223b9-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="223b9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="223b9-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="223b9-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="223b9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="223b9-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="223b9-128">**父元素**</span><span class="sxs-lookup"><span data-stu-id="223b9-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="223b9-129">**stringTable (LocalizationType)**</span><span class="sxs-lookup"><span data-stu-id="223b9-129">**stringTable (LocalizationType)**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





