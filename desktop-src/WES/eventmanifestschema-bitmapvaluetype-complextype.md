---
title: BitMapValueType 複雜類型
description: 定義位值與字串值之間的對應。 |BitMapValueType 複雜類型
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- BitMapValueType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945894"
---
# <a name="bitmapvaluetype-complex-type"></a><span data-ttu-id="fff3c-105">BitMapValueType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="fff3c-105">BitMapValueType Complex Type</span></span>

<span data-ttu-id="fff3c-106">定義位值與字串值之間的對應。</span><span class="sxs-lookup"><span data-stu-id="fff3c-106">Defines the mapping between a bit value and a string value.</span></span>

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
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

## <a name="attributes"></a><span data-ttu-id="fff3c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="fff3c-107">Attributes</span></span>



| <span data-ttu-id="fff3c-108">名稱</span><span class="sxs-lookup"><span data-stu-id="fff3c-108">Name</span></span>    | <span data-ttu-id="fff3c-109">類型</span><span class="sxs-lookup"><span data-stu-id="fff3c-109">Type</span></span>                                                              | <span data-ttu-id="fff3c-110">Description</span><span class="sxs-lookup"><span data-stu-id="fff3c-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fff3c-111">message</span><span class="sxs-lookup"><span data-stu-id="fff3c-111">message</span></span> | [<span data-ttu-id="fff3c-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="fff3c-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="fff3c-113">位值所對應的當地語系化字串值。</span><span class="sxs-lookup"><span data-stu-id="fff3c-113">The localized string value to which the bit value maps.</span></span> <span data-ttu-id="fff3c-114">訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="fff3c-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                  |
| <span data-ttu-id="fff3c-115">符號</span><span class="sxs-lookup"><span data-stu-id="fff3c-115">symbol</span></span>  | [<span data-ttu-id="fff3c-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="fff3c-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="fff3c-117">用來在應用程式中參考地圖的符號。</span><span class="sxs-lookup"><span data-stu-id="fff3c-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="fff3c-118">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立對應的常數。</span><span class="sxs-lookup"><span data-stu-id="fff3c-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="fff3c-119">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="fff3c-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="fff3c-120">value</span><span class="sxs-lookup"><span data-stu-id="fff3c-120">value</span></span>   | [<span data-ttu-id="fff3c-121">**HexInt32Type**</span><span class="sxs-lookup"><span data-stu-id="fff3c-121">**HexInt32Type**</span></span>](eventmanifestschema-hex32type-simpletype.md)  | <span data-ttu-id="fff3c-122">要對應至字串值的位值。</span><span class="sxs-lookup"><span data-stu-id="fff3c-122">The bit value to map to the string value.</span></span> <span data-ttu-id="fff3c-123">您必須指定已設定單一位的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="fff3c-123">You must specify a hexadecimal number that has a single bit set.</span></span><br/>                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="fff3c-124">備註</span><span class="sxs-lookup"><span data-stu-id="fff3c-124">Remarks</span></span>

<span data-ttu-id="fff3c-125">對應十六進位值 (數位前面必須加上 0x) ，並將單一位設定為名稱。</span><span class="sxs-lookup"><span data-stu-id="fff3c-125">Maps a hexadecimal value (the number must be preceded by 0x) with a single bit set to a name.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff3c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="fff3c-126">Requirements</span></span>



| <span data-ttu-id="fff3c-127">需求</span><span class="sxs-lookup"><span data-stu-id="fff3c-127">Requirement</span></span> | <span data-ttu-id="fff3c-128">值</span><span class="sxs-lookup"><span data-stu-id="fff3c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fff3c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fff3c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fff3c-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fff3c-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fff3c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fff3c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fff3c-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fff3c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





