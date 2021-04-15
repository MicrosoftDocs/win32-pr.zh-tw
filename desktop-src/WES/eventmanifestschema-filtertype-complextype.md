---
title: FilterType 複雜類型
description: 定義會話用來根據事件資料篩選事件的資料篩選。
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- FilterType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467013"
---
# <a name="filtertype-complex-type"></a><span data-ttu-id="b47b7-104">FilterType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="b47b7-104">FilterType Complex Type</span></span>

<span data-ttu-id="b47b7-105">定義會話用來根據事件資料篩選事件的資料篩選。</span><span class="sxs-lookup"><span data-stu-id="b47b7-105">Defines a data filter that a session uses to filter events based on event data.</span></span>

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="b47b7-106">屬性</span><span class="sxs-lookup"><span data-stu-id="b47b7-106">Attributes</span></span>



| <span data-ttu-id="b47b7-107">名稱</span><span class="sxs-lookup"><span data-stu-id="b47b7-107">Name</span></span>    | <span data-ttu-id="b47b7-108">類型</span><span class="sxs-lookup"><span data-stu-id="b47b7-108">Type</span></span>                                                              | <span data-ttu-id="b47b7-109">Description</span><span class="sxs-lookup"><span data-stu-id="b47b7-109">Description</span></span>                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47b7-110">message</span><span class="sxs-lookup"><span data-stu-id="b47b7-110">message</span></span> | [<span data-ttu-id="b47b7-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="b47b7-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="b47b7-112">篩選的當地語系化描述。</span><span class="sxs-lookup"><span data-stu-id="b47b7-112">The localized description for the filter.</span></span> <span data-ttu-id="b47b7-113">訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="b47b7-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                   |
| <span data-ttu-id="b47b7-114">NAME</span><span class="sxs-lookup"><span data-stu-id="b47b7-114">name</span></span>    | <span data-ttu-id="b47b7-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="b47b7-115">**QName**</span></span>                                                         | <span data-ttu-id="b47b7-116">識別篩選準則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b47b7-116">A name that identifies the filter.</span></span><br/>                                                                                                                                                                                                    |
| <span data-ttu-id="b47b7-117">符號</span><span class="sxs-lookup"><span data-stu-id="b47b7-117">symbol</span></span>  | [<span data-ttu-id="b47b7-118">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="b47b7-118">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="b47b7-119">用來參考應用程式中之篩選準則的符號。</span><span class="sxs-lookup"><span data-stu-id="b47b7-119">The symbol to use to reference the filter in your application.</span></span> <span data-ttu-id="b47b7-120">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立篩選的常數。</span><span class="sxs-lookup"><span data-stu-id="b47b7-120">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the filter in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="b47b7-121">tid</span><span class="sxs-lookup"><span data-stu-id="b47b7-121">tid</span></span>     | <span data-ttu-id="b47b7-122">token</span><span class="sxs-lookup"><span data-stu-id="b47b7-122">token</span></span>                                                             | <span data-ttu-id="b47b7-123">範本識別碼，描述當會話啟用提供者時，會話傳遞給提供者的篩選資料。</span><span class="sxs-lookup"><span data-stu-id="b47b7-123">A template identifier that describes the filter data that the session passes to the provider when it enables the provider.</span></span><br/>                                                                                                            |
| <span data-ttu-id="b47b7-124">value</span><span class="sxs-lookup"><span data-stu-id="b47b7-124">value</span></span>   | [<span data-ttu-id="b47b7-125">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="b47b7-125">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="b47b7-126">整數值，可唯一識別您定義之篩選器清單內的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="b47b7-126">An integer value that uniquely identifies the filter within the list of filters that you define.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b47b7-127">version</span><span class="sxs-lookup"><span data-stu-id="b47b7-127">version</span></span> | [<span data-ttu-id="b47b7-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="b47b7-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="b47b7-129">識別此篩選版本的整數值。</span><span class="sxs-lookup"><span data-stu-id="b47b7-129">An integer value that identifies this version of the filter.</span></span> <span data-ttu-id="b47b7-130">如果未指定，則值為零。</span><span class="sxs-lookup"><span data-stu-id="b47b7-130">If not specified, the value is zero.</span></span><br/>                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="b47b7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b47b7-131">Requirements</span></span>



| <span data-ttu-id="b47b7-132">需求</span><span class="sxs-lookup"><span data-stu-id="b47b7-132">Requirement</span></span> | <span data-ttu-id="b47b7-133">值</span><span class="sxs-lookup"><span data-stu-id="b47b7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b47b7-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b47b7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b47b7-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b47b7-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b47b7-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b47b7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b47b7-137">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b47b7-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





