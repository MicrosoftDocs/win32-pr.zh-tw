---
title: message (messageTable) 元素
description: 包含資訊清單當地語系化區段中之字串的參考。 |message (messageTable) 元素
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- message 元素 EventLog
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986464"
---
# <a name="message-messagetable-element"></a><span data-ttu-id="f1187-105">message (messageTable) 元素</span><span class="sxs-lookup"><span data-stu-id="f1187-105">message (messageTable) Element</span></span>

<span data-ttu-id="f1187-106">包含資訊清單當地語系化區段中之字串的參考。</span><span class="sxs-lookup"><span data-stu-id="f1187-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="message">
    <xs:complexType>
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="mid"
            type="string"
            use="optional"
         />
        <xs:attribute name="message"
            type="string"
            use="required"
         />
        <xs:attribute name="symbol"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="f1187-107">**Message** 元素是由 [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="f1187-107">The **message** element is defined by the [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="f1187-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f1187-108">Attributes</span></span>



| <span data-ttu-id="f1187-109">名稱</span><span class="sxs-lookup"><span data-stu-id="f1187-109">Name</span></span>    | <span data-ttu-id="f1187-110">類型</span><span class="sxs-lookup"><span data-stu-id="f1187-110">Type</span></span>   | <span data-ttu-id="f1187-111">Description</span><span class="sxs-lookup"><span data-stu-id="f1187-111">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1187-112">message</span><span class="sxs-lookup"><span data-stu-id="f1187-112">message</span></span> | <span data-ttu-id="f1187-113">字串</span><span class="sxs-lookup"><span data-stu-id="f1187-113">string</span></span> | <span data-ttu-id="f1187-114">字串資料表中當地語系化字串的參考。</span><span class="sxs-lookup"><span data-stu-id="f1187-114">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="f1187-115">mid</span><span class="sxs-lookup"><span data-stu-id="f1187-115">mid</span></span>     | <span data-ttu-id="f1187-116">字串</span><span class="sxs-lookup"><span data-stu-id="f1187-116">string</span></span> | <span data-ttu-id="f1187-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="f1187-117">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="f1187-118">符號</span><span class="sxs-lookup"><span data-stu-id="f1187-118">symbol</span></span>  | <span data-ttu-id="f1187-119">字串</span><span class="sxs-lookup"><span data-stu-id="f1187-119">string</span></span> | <span data-ttu-id="f1187-120">您希望訊息編譯器為此訊息字串建立的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="f1187-120">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="f1187-121">value</span><span class="sxs-lookup"><span data-stu-id="f1187-121">value</span></span>   | <span data-ttu-id="f1187-122">字串</span><span class="sxs-lookup"><span data-stu-id="f1187-122">string</span></span> | <span data-ttu-id="f1187-123">要用來做為此訊息之訊息識別碼的數位。</span><span class="sxs-lookup"><span data-stu-id="f1187-123">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="f1187-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1187-124">Requirements</span></span>



| <span data-ttu-id="f1187-125">需求</span><span class="sxs-lookup"><span data-stu-id="f1187-125">Requirement</span></span> | <span data-ttu-id="f1187-126">值</span><span class="sxs-lookup"><span data-stu-id="f1187-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1187-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1187-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f1187-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1187-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1187-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1187-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f1187-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1187-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1187-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1187-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1187-132">**父元素**</span><span class="sxs-lookup"><span data-stu-id="f1187-132">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="f1187-133">**messageTable (EventsType)**</span><span class="sxs-lookup"><span data-stu-id="f1187-133">**messageTable (EventsType)**</span></span>](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[<span data-ttu-id="f1187-134">**messageTable (MetadataType)**</span><span class="sxs-lookup"><span data-stu-id="f1187-134">**messageTable (MetadataType)**</span></span>](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





