---
title: KeywordType 複雜類型
description: 定義可識別事件類別目錄的關鍵字。 |KeywordType 複雜類型
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- KeywordType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976661"
---
# <a name="keywordtype-complex-type"></a><span data-ttu-id="837db-105">KeywordType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="837db-105">KeywordType Complex Type</span></span>

<span data-ttu-id="837db-106">定義可識別事件類別目錄的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="837db-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="837db-107">關鍵字是您附加至事件的標籤，用來根據事件的使用方式將事件分組。</span><span class="sxs-lookup"><span data-stu-id="837db-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="837db-108">屬性</span><span class="sxs-lookup"><span data-stu-id="837db-108">Attributes</span></span>



| <span data-ttu-id="837db-109">名稱</span><span class="sxs-lookup"><span data-stu-id="837db-109">Name</span></span>    | <span data-ttu-id="837db-110">類型</span><span class="sxs-lookup"><span data-stu-id="837db-110">Type</span></span>                                                              | <span data-ttu-id="837db-111">Description</span><span class="sxs-lookup"><span data-stu-id="837db-111">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="837db-112">遮罩</span><span class="sxs-lookup"><span data-stu-id="837db-112">mask</span></span>    | [<span data-ttu-id="837db-113">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="837db-113">**HexInt64Type**</span></span>](eventmanifestschema-hex64type-simpletype.md)  | <span data-ttu-id="837db-114">位元遮罩，必須只有一個位集。</span><span class="sxs-lookup"><span data-stu-id="837db-114">A bitmask that must have only a single bit set.</span></span> <span data-ttu-id="837db-115">位代表事件的類別 (例如，讀取事件或寫入事件) 。</span><span class="sxs-lookup"><span data-stu-id="837db-115">The bit represents a category of events (for example, read events or write events).</span></span> <span data-ttu-id="837db-116">您可以從0x0000000000000001 到0x0000800000000000 的範圍中指定位值， (位0到 47) 。</span><span class="sxs-lookup"><span data-stu-id="837db-116">You can specify bit values in the range from 0x0000000000000001 through 0x0000800000000000 (bits 0 through 47).</span></span><br/>                                                         |
| <span data-ttu-id="837db-117">message</span><span class="sxs-lookup"><span data-stu-id="837db-117">message</span></span> | [<span data-ttu-id="837db-118">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="837db-118">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="837db-119">關鍵字的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="837db-119">The localized display name for the keyword.</span></span> <span data-ttu-id="837db-120">訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="837db-120">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                                                                                       |
| <span data-ttu-id="837db-121">NAME</span><span class="sxs-lookup"><span data-stu-id="837db-121">name</span></span>    | <span data-ttu-id="837db-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="837db-122">**QName**</span></span>                                                         | <span data-ttu-id="837db-123">關鍵字的名稱。</span><span class="sxs-lookup"><span data-stu-id="837db-123">The name of the keyword.</span></span> <span data-ttu-id="837db-124">在提供者定義的關鍵字清單中，此名稱必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="837db-124">The name must be unique within the list of keywords that the provider defines.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="837db-125">符號</span><span class="sxs-lookup"><span data-stu-id="837db-125">symbol</span></span>  | [<span data-ttu-id="837db-126">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="837db-126">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="837db-127">用來在應用程式中參考關鍵字的符號。</span><span class="sxs-lookup"><span data-stu-id="837db-127">The symbol to use to reference the keyword in your application.</span></span> <span data-ttu-id="837db-128">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立關鍵字的常數。</span><span class="sxs-lookup"><span data-stu-id="837db-128">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the keyword in the header file that the compiler generates.</span></span> <span data-ttu-id="837db-129">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="837db-129">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="837db-130">備註</span><span class="sxs-lookup"><span data-stu-id="837db-130">Remarks</span></span>

<span data-ttu-id="837db-131">包含在 Windows SDK 中的 Winmeta.xml 檔案包含關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="837db-131">The Winmeta.xml file that is included in the Windows SDK contains a list of keywords.</span></span> <span data-ttu-id="837db-132">這些關鍵字是保留的，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="837db-132">These keywords are reserved and should not be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="837db-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="837db-133">Requirements</span></span>



| <span data-ttu-id="837db-134">需求</span><span class="sxs-lookup"><span data-stu-id="837db-134">Requirement</span></span> | <span data-ttu-id="837db-135">值</span><span class="sxs-lookup"><span data-stu-id="837db-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="837db-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="837db-136">Minimum supported client</span></span><br/> | <span data-ttu-id="837db-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="837db-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="837db-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="837db-138">Minimum supported server</span></span><br/> | <span data-ttu-id="837db-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="837db-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





