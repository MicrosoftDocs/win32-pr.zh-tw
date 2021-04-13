---
title: ValueMapValueType 複雜類型
description: 定義整數值與字串值之間的對應。 |ValueMapValueType 複雜類型
ms.assetid: 8fd3b3ed-5b62-4e2e-b6f9-8e1bf6d83a35
keywords:
- ValueMapValueType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ValueMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 197eb7e402068f541dc5a385eca14a631de2488c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386352"
---
# <a name="valuemapvaluetype-complex-type"></a><span data-ttu-id="09285-105">ValueMapValueType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="09285-105">ValueMapValueType Complex Type</span></span>

<span data-ttu-id="09285-106">定義整數值與字串值之間的對應。</span><span class="sxs-lookup"><span data-stu-id="09285-106">Defines the mapping between an integer value and a string value.</span></span>

``` syntax
<xs:complexType name="ValueMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="09285-107">屬性</span><span class="sxs-lookup"><span data-stu-id="09285-107">Attributes</span></span>



| <span data-ttu-id="09285-108">名稱</span><span class="sxs-lookup"><span data-stu-id="09285-108">Name</span></span>    | <span data-ttu-id="09285-109">類型</span><span class="sxs-lookup"><span data-stu-id="09285-109">Type</span></span>                                                              | <span data-ttu-id="09285-110">Description</span><span class="sxs-lookup"><span data-stu-id="09285-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09285-111">message</span><span class="sxs-lookup"><span data-stu-id="09285-111">message</span></span> | [<span data-ttu-id="09285-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="09285-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="09285-113">整數值所對應的當地語系化字串值。</span><span class="sxs-lookup"><span data-stu-id="09285-113">The localized string value to which the integer value maps.</span></span> <span data-ttu-id="09285-114">訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="09285-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                              |
| <span data-ttu-id="09285-115">符號</span><span class="sxs-lookup"><span data-stu-id="09285-115">symbol</span></span>  | [<span data-ttu-id="09285-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="09285-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="09285-117">用來在應用程式中參考地圖的符號。</span><span class="sxs-lookup"><span data-stu-id="09285-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="09285-118">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立對應的常數。</span><span class="sxs-lookup"><span data-stu-id="09285-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="09285-119">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="09285-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="09285-120">value</span><span class="sxs-lookup"><span data-stu-id="09285-120">value</span></span>   | [<span data-ttu-id="09285-121">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="09285-121">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="09285-122">要對應至字串值的整數值。</span><span class="sxs-lookup"><span data-stu-id="09285-122">The integer value to map to the string value.</span></span><br/>                                                                                                                                                                                                                                                       |



## <a name="requirements"></a><span data-ttu-id="09285-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="09285-123">Requirements</span></span>



| <span data-ttu-id="09285-124">需求</span><span class="sxs-lookup"><span data-stu-id="09285-124">Requirement</span></span> | <span data-ttu-id="09285-125">值</span><span class="sxs-lookup"><span data-stu-id="09285-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09285-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09285-126">Minimum supported client</span></span><br/> | <span data-ttu-id="09285-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09285-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="09285-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09285-128">Minimum supported server</span></span><br/> | <span data-ttu-id="09285-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09285-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





