---
title: messageTable (EventsType) 元素
description: 包含資訊清單當地語系化區段中之字串的參考。 |messageTable (EventsType) 元素
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- messageTable 元素 EventLog
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986463"
---
# <a name="messagetable-eventstype-element"></a><span data-ttu-id="26c65-105">messageTable (EventsType) 元素</span><span class="sxs-lookup"><span data-stu-id="26c65-105">messageTable (EventsType) Element</span></span>

<span data-ttu-id="26c65-106">包含資訊清單當地語系化區段中之字串的參考。</span><span class="sxs-lookup"><span data-stu-id="26c65-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="26c65-107">**MessageTable** 元素是由 [**EventsType**](eventmanifestschema-eventstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="26c65-107">The **messageTable** element is defined by the [**EventsType**](eventmanifestschema-eventstype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="26c65-108">子元素</span><span class="sxs-lookup"><span data-stu-id="26c65-108">Child elements</span></span>



| <span data-ttu-id="26c65-109">元素</span><span class="sxs-lookup"><span data-stu-id="26c65-109">Element</span></span>                                                             | <span data-ttu-id="26c65-110">類型</span><span class="sxs-lookup"><span data-stu-id="26c65-110">Type</span></span> | <span data-ttu-id="26c65-111">Description</span><span class="sxs-lookup"><span data-stu-id="26c65-111">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26c65-112">**message**</span><span class="sxs-lookup"><span data-stu-id="26c65-112">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="26c65-113">指定資訊清單當地語系化區段中字串的參考。</span><span class="sxs-lookup"><span data-stu-id="26c65-113">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="26c65-114">屬性</span><span class="sxs-lookup"><span data-stu-id="26c65-114">Attributes</span></span>



| <span data-ttu-id="26c65-115">名稱</span><span class="sxs-lookup"><span data-stu-id="26c65-115">Name</span></span>    | <span data-ttu-id="26c65-116">類型</span><span class="sxs-lookup"><span data-stu-id="26c65-116">Type</span></span>   | <span data-ttu-id="26c65-117">Description</span><span class="sxs-lookup"><span data-stu-id="26c65-117">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26c65-118">message</span><span class="sxs-lookup"><span data-stu-id="26c65-118">message</span></span> | <span data-ttu-id="26c65-119">字串</span><span class="sxs-lookup"><span data-stu-id="26c65-119">string</span></span> | <span data-ttu-id="26c65-120">字串資料表中當地語系化字串的參考。</span><span class="sxs-lookup"><span data-stu-id="26c65-120">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="26c65-121">mid</span><span class="sxs-lookup"><span data-stu-id="26c65-121">mid</span></span>     | <span data-ttu-id="26c65-122">字串</span><span class="sxs-lookup"><span data-stu-id="26c65-122">string</span></span> | <span data-ttu-id="26c65-123">未使用。</span><span class="sxs-lookup"><span data-stu-id="26c65-123">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="26c65-124">符號</span><span class="sxs-lookup"><span data-stu-id="26c65-124">symbol</span></span>  | <span data-ttu-id="26c65-125">字串</span><span class="sxs-lookup"><span data-stu-id="26c65-125">string</span></span> | <span data-ttu-id="26c65-126">您希望訊息編譯器為此訊息字串建立的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="26c65-126">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="26c65-127">value</span><span class="sxs-lookup"><span data-stu-id="26c65-127">value</span></span>   | <span data-ttu-id="26c65-128">字串</span><span class="sxs-lookup"><span data-stu-id="26c65-128">string</span></span> | <span data-ttu-id="26c65-129">要用來做為此訊息之訊息識別碼的數位。</span><span class="sxs-lookup"><span data-stu-id="26c65-129">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="26c65-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="26c65-130">Requirements</span></span>



| <span data-ttu-id="26c65-131">需求</span><span class="sxs-lookup"><span data-stu-id="26c65-131">Requirement</span></span> | <span data-ttu-id="26c65-132">值</span><span class="sxs-lookup"><span data-stu-id="26c65-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26c65-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26c65-133">Minimum supported client</span></span><br/> | <span data-ttu-id="26c65-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26c65-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26c65-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26c65-135">Minimum supported server</span></span><br/> | <span data-ttu-id="26c65-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26c65-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26c65-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26c65-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="26c65-138">**父元素**</span><span class="sxs-lookup"><span data-stu-id="26c65-138">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="26c65-139">**事件 (Instrumentationtype.event) 元素**</span><span class="sxs-lookup"><span data-stu-id="26c65-139">**events (InstrumentationType) Element**</span></span>](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





