---
title: PatternMapType 複雜類型
description: 未使用。 定義兩個正則運算式之間的對應。 其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則是用來在服務將字串放回訊息字串之前變更字串。
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- PatternMapType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465757"
---
# <a name="patternmaptype-complex-type"></a><span data-ttu-id="04794-106">PatternMapType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="04794-106">PatternMapType Complex Type</span></span>

<span data-ttu-id="04794-107">未使用。</span><span class="sxs-lookup"><span data-stu-id="04794-107">Not used.</span></span> <span data-ttu-id="04794-108">定義兩個正則運算式之間的對應。</span><span class="sxs-lookup"><span data-stu-id="04794-108">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="04794-109">其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則是用來在服務將字串放回訊息字串之前變更字串。</span><span class="sxs-lookup"><span data-stu-id="04794-109">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="04794-110">子元素</span><span class="sxs-lookup"><span data-stu-id="04794-110">Child elements</span></span>



| <span data-ttu-id="04794-111">元素</span><span class="sxs-lookup"><span data-stu-id="04794-111">Element</span></span>                                                       | <span data-ttu-id="04794-112">類型</span><span class="sxs-lookup"><span data-stu-id="04794-112">Type</span></span>                                                                               | <span data-ttu-id="04794-113">Description</span><span class="sxs-lookup"><span data-stu-id="04794-113">Description</span></span>                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04794-114">**地圖**</span><span class="sxs-lookup"><span data-stu-id="04794-114">**map**</span></span>](eventmanifestschema-map-patternmaptype-element.md) | [<span data-ttu-id="04794-115">**PatternMapValueType**</span><span class="sxs-lookup"><span data-stu-id="04794-115">**PatternMapValueType**</span></span>](eventmanifestschema-patternmapvaluetype-complextype.md) | <span data-ttu-id="04794-116">定義用來在訊息字串中尋找相符字串的正則運算式，並加以修改。</span><span class="sxs-lookup"><span data-stu-id="04794-116">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="04794-117">屬性</span><span class="sxs-lookup"><span data-stu-id="04794-117">Attributes</span></span>



| <span data-ttu-id="04794-118">名稱</span><span class="sxs-lookup"><span data-stu-id="04794-118">Name</span></span>   | <span data-ttu-id="04794-119">類型</span><span class="sxs-lookup"><span data-stu-id="04794-119">Type</span></span>                                                              | <span data-ttu-id="04794-120">Description</span><span class="sxs-lookup"><span data-stu-id="04794-120">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04794-121">format</span><span class="sxs-lookup"><span data-stu-id="04794-121">format</span></span> | <span data-ttu-id="04794-122">anyURI</span><span class="sxs-lookup"><span data-stu-id="04794-122">anyURI</span></span>                                                            | <span data-ttu-id="04794-123">要使用的正則運算式引擎。</span><span class="sxs-lookup"><span data-stu-id="04794-123">The regular expression engine to use.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="04794-124">NAME</span><span class="sxs-lookup"><span data-stu-id="04794-124">name</span></span>   | <span data-ttu-id="04794-125">**QName**</span><span class="sxs-lookup"><span data-stu-id="04794-125">**QName**</span></span>                                                         | <span data-ttu-id="04794-126">模式對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="04794-126">The name of the pattern map.</span></span> <span data-ttu-id="04794-127">使用資料元素中的名稱來參考對應。</span><span class="sxs-lookup"><span data-stu-id="04794-127">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="04794-128">符號</span><span class="sxs-lookup"><span data-stu-id="04794-128">symbol</span></span> | [<span data-ttu-id="04794-129">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="04794-129">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="04794-130">用來參考應用程式中對應的符號。</span><span class="sxs-lookup"><span data-stu-id="04794-130">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="04794-131">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立對應的常數。</span><span class="sxs-lookup"><span data-stu-id="04794-131">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="04794-132">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="04794-132">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="04794-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="04794-133">Requirements</span></span>



| <span data-ttu-id="04794-134">需求</span><span class="sxs-lookup"><span data-stu-id="04794-134">Requirement</span></span> | <span data-ttu-id="04794-135">值</span><span class="sxs-lookup"><span data-stu-id="04794-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="04794-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04794-136">Minimum supported client</span></span><br/> | <span data-ttu-id="04794-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04794-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04794-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04794-138">Minimum supported server</span></span><br/> | <span data-ttu-id="04794-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04794-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





