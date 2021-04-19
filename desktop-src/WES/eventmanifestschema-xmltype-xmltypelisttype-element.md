---
title: xmlType (XmlTypeListType) 元素
description: 定義 XML 類型。
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- xmlType 元素 EventLog
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969780"
---
# <a name="xmltype-xmltypelisttype-element"></a><span data-ttu-id="cb9e3-104">xmlType (XmlTypeListType) 元素</span><span class="sxs-lookup"><span data-stu-id="cb9e3-104">xmlType (XmlTypeListType) Element</span></span>

<span data-ttu-id="cb9e3-105">定義 XML 類型。</span><span class="sxs-lookup"><span data-stu-id="cb9e3-105">Defines an XML type.</span></span>

``` syntax
<xs:element name="xmlType">
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
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="cb9e3-106">**XmlType** 元素是由 [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="cb9e3-106">The **xmlType** element is defined by the [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="cb9e3-107">屬性</span><span class="sxs-lookup"><span data-stu-id="cb9e3-107">Attributes</span></span>



| <span data-ttu-id="cb9e3-108">名稱</span><span class="sxs-lookup"><span data-stu-id="cb9e3-108">Name</span></span>   | <span data-ttu-id="cb9e3-109">類型</span><span class="sxs-lookup"><span data-stu-id="cb9e3-109">Type</span></span>      | <span data-ttu-id="cb9e3-110">描述</span><span class="sxs-lookup"><span data-stu-id="cb9e3-110">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9e3-111">NAME</span><span class="sxs-lookup"><span data-stu-id="cb9e3-111">name</span></span>   | <span data-ttu-id="cb9e3-112">**QName**</span><span class="sxs-lookup"><span data-stu-id="cb9e3-112">**QName**</span></span> | <span data-ttu-id="cb9e3-113">輸出類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb9e3-113">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="cb9e3-114">符號</span><span class="sxs-lookup"><span data-stu-id="cb9e3-114">symbol</span></span> | <span data-ttu-id="cb9e3-115">字串</span><span class="sxs-lookup"><span data-stu-id="cb9e3-115">string</span></span>    | <span data-ttu-id="cb9e3-116">用來參考應用程式中輸出類型的符號。</span><span class="sxs-lookup"><span data-stu-id="cb9e3-116">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="cb9e3-117">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立輸出類型的常數。</span><span class="sxs-lookup"><span data-stu-id="cb9e3-117">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="cb9e3-118">value</span><span class="sxs-lookup"><span data-stu-id="cb9e3-118">value</span></span>  | <span data-ttu-id="cb9e3-119">字串</span><span class="sxs-lookup"><span data-stu-id="cb9e3-119">string</span></span>    | <span data-ttu-id="cb9e3-120">整數值，可唯一識別您定義之輸出類型清單中的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="cb9e3-120">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="cb9e3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb9e3-121">Requirements</span></span>



| <span data-ttu-id="cb9e3-122">需求</span><span class="sxs-lookup"><span data-stu-id="cb9e3-122">Requirement</span></span> | <span data-ttu-id="cb9e3-123">值</span><span class="sxs-lookup"><span data-stu-id="cb9e3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb9e3-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb9e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cb9e3-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb9e3-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cb9e3-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb9e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cb9e3-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb9e3-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb9e3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb9e3-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb9e3-129">**父元素**</span><span class="sxs-lookup"><span data-stu-id="cb9e3-129">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="cb9e3-130">**xmlTypes (TypeListType)**</span><span class="sxs-lookup"><span data-stu-id="cb9e3-130">**xmlTypes (TypeListType)**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





