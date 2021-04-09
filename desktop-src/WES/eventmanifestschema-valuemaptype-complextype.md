---
title: ValueMapType 複雜類型
description: 定義整數值與字串值之間的名稱/值對應清單。
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- ValueMapType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685461"
---
# <a name="valuemaptype-complex-type"></a><span data-ttu-id="85c84-104">ValueMapType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="85c84-104">ValueMapType Complex Type</span></span>

<span data-ttu-id="85c84-105">定義整數值與字串值之間的名稱/值對應清單。</span><span class="sxs-lookup"><span data-stu-id="85c84-105">Defines a list of name/value mappings between integer values and string values.</span></span>

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="85c84-106">子元素</span><span class="sxs-lookup"><span data-stu-id="85c84-106">Child elements</span></span>



| <span data-ttu-id="85c84-107">元素</span><span class="sxs-lookup"><span data-stu-id="85c84-107">Element</span></span>                                                     | <span data-ttu-id="85c84-108">類型</span><span class="sxs-lookup"><span data-stu-id="85c84-108">Type</span></span>                                                                           | <span data-ttu-id="85c84-109">Description</span><span class="sxs-lookup"><span data-stu-id="85c84-109">Description</span></span>                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="85c84-110">**地圖**</span><span class="sxs-lookup"><span data-stu-id="85c84-110">**map**</span></span>](eventmanifestschema-map-valuemaptype-element.md) | [<span data-ttu-id="85c84-111">**ValueMapValueType**</span><span class="sxs-lookup"><span data-stu-id="85c84-111">**ValueMapValueType**</span></span>](eventmanifestschema-valuemapvaluetype-complextype.md) | <span data-ttu-id="85c84-112">定義整數值與字串值之間的對應。</span><span class="sxs-lookup"><span data-stu-id="85c84-112">Defines the mapping between an integer value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="85c84-113">屬性</span><span class="sxs-lookup"><span data-stu-id="85c84-113">Attributes</span></span>



| <span data-ttu-id="85c84-114">名稱</span><span class="sxs-lookup"><span data-stu-id="85c84-114">Name</span></span>   | <span data-ttu-id="85c84-115">類型</span><span class="sxs-lookup"><span data-stu-id="85c84-115">Type</span></span>                                                              | <span data-ttu-id="85c84-116">描述</span><span class="sxs-lookup"><span data-stu-id="85c84-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c84-117">NAME</span><span class="sxs-lookup"><span data-stu-id="85c84-117">name</span></span>   | <span data-ttu-id="85c84-118">字串</span><span class="sxs-lookup"><span data-stu-id="85c84-118">string</span></span>                                                            | <span data-ttu-id="85c84-119">值對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="85c84-119">The name of the value map.</span></span> <span data-ttu-id="85c84-120">使用資料元素中的名稱來參考對應。</span><span class="sxs-lookup"><span data-stu-id="85c84-120">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                     |
| <span data-ttu-id="85c84-121">符號</span><span class="sxs-lookup"><span data-stu-id="85c84-121">symbol</span></span> | [<span data-ttu-id="85c84-122">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="85c84-122">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="85c84-123">用來參考應用程式中對應的符號。</span><span class="sxs-lookup"><span data-stu-id="85c84-123">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="85c84-124">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立對應的常數。</span><span class="sxs-lookup"><span data-stu-id="85c84-124">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="85c84-125">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="85c84-125">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="85c84-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="85c84-126">Requirements</span></span>



| <span data-ttu-id="85c84-127">需求</span><span class="sxs-lookup"><span data-stu-id="85c84-127">Requirement</span></span> | <span data-ttu-id="85c84-128">值</span><span class="sxs-lookup"><span data-stu-id="85c84-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85c84-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85c84-129">Minimum supported client</span></span><br/> | <span data-ttu-id="85c84-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85c84-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85c84-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85c84-131">Minimum supported server</span></span><br/> | <span data-ttu-id="85c84-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85c84-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





