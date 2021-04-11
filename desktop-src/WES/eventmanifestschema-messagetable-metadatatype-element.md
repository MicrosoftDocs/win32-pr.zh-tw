---
title: messageTable (MetadataType) 元素
description: 包含事件檢測資訊清單中繼資料區段中所使用之字串的參考。 這些字串會儲存在一組訊息元素和識別碼一起的識別碼。
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
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
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094031"
---
# <a name="messagetable-metadatatype-element"></a><span data-ttu-id="445fe-105">messageTable (MetadataType) 元素</span><span class="sxs-lookup"><span data-stu-id="445fe-105">messageTable (MetadataType) Element</span></span>

<span data-ttu-id="445fe-106">包含事件檢測資訊清單中繼資料區段中所使用之字串的參考。</span><span class="sxs-lookup"><span data-stu-id="445fe-106">Contains references to strings that are used in the event instrumentation manifest metadata section.</span></span> <span data-ttu-id="445fe-107">這些字串會儲存在一組 [**訊息**](eventmanifestschema-message-messagetable-element.md) 元素和識別碼一起的識別碼。</span><span class="sxs-lookup"><span data-stu-id="445fe-107">The strings are stored in a group of [**message**](eventmanifestschema-message-messagetable-element.md) elements and IDs paired together.</span></span>

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

<span data-ttu-id="445fe-108">**MessageTable** 元素是由 [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="445fe-108">The **messageTable** element is defined by the [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="445fe-109">子元素</span><span class="sxs-lookup"><span data-stu-id="445fe-109">Child elements</span></span>



| <span data-ttu-id="445fe-110">元素</span><span class="sxs-lookup"><span data-stu-id="445fe-110">Element</span></span>                                                             | <span data-ttu-id="445fe-111">類型</span><span class="sxs-lookup"><span data-stu-id="445fe-111">Type</span></span> | <span data-ttu-id="445fe-112">Description</span><span class="sxs-lookup"><span data-stu-id="445fe-112">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="445fe-113">**message**</span><span class="sxs-lookup"><span data-stu-id="445fe-113">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="445fe-114">指定資訊清單當地語系化區段中字串的參考。</span><span class="sxs-lookup"><span data-stu-id="445fe-114">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="445fe-115">屬性</span><span class="sxs-lookup"><span data-stu-id="445fe-115">Attributes</span></span>



| <span data-ttu-id="445fe-116">名稱</span><span class="sxs-lookup"><span data-stu-id="445fe-116">Name</span></span>    | <span data-ttu-id="445fe-117">類型</span><span class="sxs-lookup"><span data-stu-id="445fe-117">Type</span></span>   | <span data-ttu-id="445fe-118">Description</span><span class="sxs-lookup"><span data-stu-id="445fe-118">Description</span></span>                                                              |
|---------|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="445fe-119">message</span><span class="sxs-lookup"><span data-stu-id="445fe-119">message</span></span> | <span data-ttu-id="445fe-120">字串</span><span class="sxs-lookup"><span data-stu-id="445fe-120">string</span></span> | <span data-ttu-id="445fe-121">字串資料表中當地語系化字串的參考。</span><span class="sxs-lookup"><span data-stu-id="445fe-121">A reference to the localized string in the string table.</span></span><br/>      |
| <span data-ttu-id="445fe-122">mid</span><span class="sxs-lookup"><span data-stu-id="445fe-122">mid</span></span>     | <span data-ttu-id="445fe-123">字串</span><span class="sxs-lookup"><span data-stu-id="445fe-123">string</span></span> | <span data-ttu-id="445fe-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="445fe-124">Not used.</span></span><br/>                                                     |
| <span data-ttu-id="445fe-125">符號</span><span class="sxs-lookup"><span data-stu-id="445fe-125">symbol</span></span>  | <span data-ttu-id="445fe-126">字串</span><span class="sxs-lookup"><span data-stu-id="445fe-126">string</span></span> | <span data-ttu-id="445fe-127">用來參考訊息的符號。</span><span class="sxs-lookup"><span data-stu-id="445fe-127">The symbol used to reference the message.</span></span><br/>                     |
| <span data-ttu-id="445fe-128">value</span><span class="sxs-lookup"><span data-stu-id="445fe-128">value</span></span>   | <span data-ttu-id="445fe-129">字串</span><span class="sxs-lookup"><span data-stu-id="445fe-129">string</span></span> | <span data-ttu-id="445fe-130">要用來做為此訊息之訊息識別碼的數位。</span><span class="sxs-lookup"><span data-stu-id="445fe-130">The number to use as the message identifier for this message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="445fe-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="445fe-131">Requirements</span></span>



| <span data-ttu-id="445fe-132">需求</span><span class="sxs-lookup"><span data-stu-id="445fe-132">Requirement</span></span> | <span data-ttu-id="445fe-133">值</span><span class="sxs-lookup"><span data-stu-id="445fe-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="445fe-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="445fe-134">Minimum supported client</span></span><br/> | <span data-ttu-id="445fe-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="445fe-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="445fe-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="445fe-136">Minimum supported server</span></span><br/> | <span data-ttu-id="445fe-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="445fe-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="445fe-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="445fe-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="445fe-139">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="445fe-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="445fe-140">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="445fe-140">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

<span data-ttu-id="445fe-141">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="445fe-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="445fe-142">**中繼資料 (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="445fe-142">**metadata (instrumentationManifest)**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





