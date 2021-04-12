---
title: XmlTypeListType 複雜類型
description: 定義清單輸出類型，服務會使用此類型來判斷如何轉譯輸入資料類型。
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- XmlTypeListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317295"
---
# <a name="xmltypelisttype-complex-type"></a><span data-ttu-id="009c1-104">XmlTypeListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="009c1-104">XmlTypeListType Complex Type</span></span>

<span data-ttu-id="009c1-105">定義清單輸出類型，服務會使用此類型來判斷如何轉譯輸入資料類型。</span><span class="sxs-lookup"><span data-stu-id="009c1-105">Defines a list output types that the service uses to determine how to render an input data type.</span></span>

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension
                        base="XmlType"
                    >
                        <xs:attribute name="name"
                            type="QName"
                            use="required"
                         />
                        <xs:attribute name="value"
                            type="string"
                            use="required"
                         />
                        <xs:attribute name="symbol"
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="009c1-106">子元素</span><span class="sxs-lookup"><span data-stu-id="009c1-106">Child elements</span></span>



| <span data-ttu-id="009c1-107">元素</span><span class="sxs-lookup"><span data-stu-id="009c1-107">Element</span></span>                                                                | <span data-ttu-id="009c1-108">類型</span><span class="sxs-lookup"><span data-stu-id="009c1-108">Type</span></span> | <span data-ttu-id="009c1-109">Description</span><span class="sxs-lookup"><span data-stu-id="009c1-109">Description</span></span>                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [<span data-ttu-id="009c1-110">**xmlType**</span><span class="sxs-lookup"><span data-stu-id="009c1-110">**xmlType**</span></span>](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | <span data-ttu-id="009c1-111">定義 XML 類型。</span><span class="sxs-lookup"><span data-stu-id="009c1-111">Defines an XML type.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="009c1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="009c1-112">Attributes</span></span>



| <span data-ttu-id="009c1-113">名稱</span><span class="sxs-lookup"><span data-stu-id="009c1-113">Name</span></span>   | <span data-ttu-id="009c1-114">類型</span><span class="sxs-lookup"><span data-stu-id="009c1-114">Type</span></span>                                                              | <span data-ttu-id="009c1-115">描述</span><span class="sxs-lookup"><span data-stu-id="009c1-115">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="009c1-116">NAME</span><span class="sxs-lookup"><span data-stu-id="009c1-116">name</span></span>   | <span data-ttu-id="009c1-117">**QName**</span><span class="sxs-lookup"><span data-stu-id="009c1-117">**QName**</span></span>                                                         | <span data-ttu-id="009c1-118">輸出類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="009c1-118">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="009c1-119">符號</span><span class="sxs-lookup"><span data-stu-id="009c1-119">symbol</span></span> | [<span data-ttu-id="009c1-120">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="009c1-120">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="009c1-121">用來參考應用程式中輸出類型的符號。</span><span class="sxs-lookup"><span data-stu-id="009c1-121">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="009c1-122">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立輸出類型的常數。</span><span class="sxs-lookup"><span data-stu-id="009c1-122">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="009c1-123">value</span><span class="sxs-lookup"><span data-stu-id="009c1-123">value</span></span>  | <span data-ttu-id="009c1-124">字串</span><span class="sxs-lookup"><span data-stu-id="009c1-124">string</span></span>                                                            | <span data-ttu-id="009c1-125">整數值，可唯一識別您定義之輸出類型清單中的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="009c1-125">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="009c1-126">備註</span><span class="sxs-lookup"><span data-stu-id="009c1-126">Remarks</span></span>

<span data-ttu-id="009c1-127">包含 \\ \\ 在 Windows SDK 中的 IncludeWinmeta.xml 檔案包含預先定義之輸出類型的清單。</span><span class="sxs-lookup"><span data-stu-id="009c1-127">The \\Include\\Winmeta.xml file, which is included in the Windows SDK, contains a list of predefined output types.</span></span>

## <a name="requirements"></a><span data-ttu-id="009c1-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="009c1-128">Requirements</span></span>



| <span data-ttu-id="009c1-129">需求</span><span class="sxs-lookup"><span data-stu-id="009c1-129">Requirement</span></span> | <span data-ttu-id="009c1-130">值</span><span class="sxs-lookup"><span data-stu-id="009c1-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="009c1-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="009c1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="009c1-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="009c1-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="009c1-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="009c1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="009c1-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="009c1-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





