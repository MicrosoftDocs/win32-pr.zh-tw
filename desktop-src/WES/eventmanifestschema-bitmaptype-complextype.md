---
title: BitMapType 複雜類型
description: 定義位值與字串值之間的名稱/值對應清單。
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- BitMapType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466973"
---
# <a name="bitmaptype-complex-type"></a><span data-ttu-id="6d487-104">BitMapType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="6d487-104">BitMapType Complex Type</span></span>

<span data-ttu-id="6d487-105">定義位值與字串值之間的名稱/值對應清單。</span><span class="sxs-lookup"><span data-stu-id="6d487-105">Defines a list of name/value mappings between bit values and string values.</span></span>

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6d487-106">子元素</span><span class="sxs-lookup"><span data-stu-id="6d487-106">Child elements</span></span>



| <span data-ttu-id="6d487-107">元素</span><span class="sxs-lookup"><span data-stu-id="6d487-107">Element</span></span>                                                   | <span data-ttu-id="6d487-108">類型</span><span class="sxs-lookup"><span data-stu-id="6d487-108">Type</span></span>                                                                       | <span data-ttu-id="6d487-109">Description</span><span class="sxs-lookup"><span data-stu-id="6d487-109">Description</span></span>                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="6d487-110">**地圖**</span><span class="sxs-lookup"><span data-stu-id="6d487-110">**map**</span></span>](eventmanifestschema-map-bitmaptype-element.md) | [<span data-ttu-id="6d487-111">**BitMapValueType**</span><span class="sxs-lookup"><span data-stu-id="6d487-111">**BitMapValueType**</span></span>](eventmanifestschema-bitmapvaluetype-complextype.md) | <span data-ttu-id="6d487-112">定義位值與字串值之間的對應。</span><span class="sxs-lookup"><span data-stu-id="6d487-112">Defines the mapping between a bit value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="6d487-113">屬性</span><span class="sxs-lookup"><span data-stu-id="6d487-113">Attributes</span></span>



| <span data-ttu-id="6d487-114">名稱</span><span class="sxs-lookup"><span data-stu-id="6d487-114">Name</span></span>   | <span data-ttu-id="6d487-115">類型</span><span class="sxs-lookup"><span data-stu-id="6d487-115">Type</span></span>                                                              | <span data-ttu-id="6d487-116">描述</span><span class="sxs-lookup"><span data-stu-id="6d487-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d487-117">NAME</span><span class="sxs-lookup"><span data-stu-id="6d487-117">name</span></span>   | <span data-ttu-id="6d487-118">字串</span><span class="sxs-lookup"><span data-stu-id="6d487-118">string</span></span>                                                            | <span data-ttu-id="6d487-119">點陣圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d487-119">The name of the bitmap.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6d487-120">符號</span><span class="sxs-lookup"><span data-stu-id="6d487-120">symbol</span></span> | [<span data-ttu-id="6d487-121">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="6d487-121">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="6d487-122">用來參考應用程式中對應的符號。</span><span class="sxs-lookup"><span data-stu-id="6d487-122">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="6d487-123">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立對應的常數。</span><span class="sxs-lookup"><span data-stu-id="6d487-123">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="6d487-124">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="6d487-124">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6d487-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d487-125">Requirements</span></span>



| <span data-ttu-id="6d487-126">需求</span><span class="sxs-lookup"><span data-stu-id="6d487-126">Requirement</span></span> | <span data-ttu-id="6d487-127">值</span><span class="sxs-lookup"><span data-stu-id="6d487-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6d487-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d487-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6d487-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d487-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6d487-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d487-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6d487-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d487-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





