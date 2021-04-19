---
title: StringTableType 複雜類型
description: 定義您可以在資訊清單中參考的當地語系化字串清單。 |StringTableType 複雜類型
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- StringTableType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981787"
---
# <a name="stringtabletype-complex-type"></a><span data-ttu-id="80f9c-105">StringTableType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="80f9c-105">StringTableType Complex Type</span></span>

<span data-ttu-id="80f9c-106">定義您可以在資訊清單中參考的當地語系化字串清單。</span><span class="sxs-lookup"><span data-stu-id="80f9c-106">Defines a list of localized strings that you can reference in your manifest.</span></span>

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="80f9c-107">子元素</span><span class="sxs-lookup"><span data-stu-id="80f9c-107">Child elements</span></span>



| <span data-ttu-id="80f9c-108">元素</span><span class="sxs-lookup"><span data-stu-id="80f9c-108">Element</span></span>                                                              | <span data-ttu-id="80f9c-109">類型</span><span class="sxs-lookup"><span data-stu-id="80f9c-109">Type</span></span> | <span data-ttu-id="80f9c-110">Description</span><span class="sxs-lookup"><span data-stu-id="80f9c-110">Description</span></span>                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [<span data-ttu-id="80f9c-111">**字串**</span><span class="sxs-lookup"><span data-stu-id="80f9c-111">**string**</span></span>](eventmanifestschema-string-stringtabletype-element.md) |      | <span data-ttu-id="80f9c-112">定義當地語系化的字串。</span><span class="sxs-lookup"><span data-stu-id="80f9c-112">Defines a localized string.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="80f9c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="80f9c-113">Attributes</span></span>



| <span data-ttu-id="80f9c-114">名稱</span><span class="sxs-lookup"><span data-stu-id="80f9c-114">Name</span></span>       | <span data-ttu-id="80f9c-115">類型</span><span class="sxs-lookup"><span data-stu-id="80f9c-115">Type</span></span>   | <span data-ttu-id="80f9c-116">描述</span><span class="sxs-lookup"><span data-stu-id="80f9c-116">Description</span></span>                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f9c-117">id</span><span class="sxs-lookup"><span data-stu-id="80f9c-117">id</span></span>         | <span data-ttu-id="80f9c-118">字串</span><span class="sxs-lookup"><span data-stu-id="80f9c-118">string</span></span> | <span data-ttu-id="80f9c-119">唯一識別字串資料表內之字串的識別碼。</span><span class="sxs-lookup"><span data-stu-id="80f9c-119">An identifier that uniquely identifies the string within the string table.</span></span> <span data-ttu-id="80f9c-120">例如，「印表機連接」。</span><span class="sxs-lookup"><span data-stu-id="80f9c-120">For example, "Printer.Connection".</span></span><br/> |
| <span data-ttu-id="80f9c-121">stringType</span><span class="sxs-lookup"><span data-stu-id="80f9c-121">stringType</span></span> | <span data-ttu-id="80f9c-122">字串</span><span class="sxs-lookup"><span data-stu-id="80f9c-122">string</span></span> | <span data-ttu-id="80f9c-123">未使用。</span><span class="sxs-lookup"><span data-stu-id="80f9c-123">Not used.</span></span><br/>                                                                                                     |
| <span data-ttu-id="80f9c-124">value</span><span class="sxs-lookup"><span data-stu-id="80f9c-124">value</span></span>      | <span data-ttu-id="80f9c-125">字串</span><span class="sxs-lookup"><span data-stu-id="80f9c-125">string</span></span> | <span data-ttu-id="80f9c-126">當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="80f9c-126">The localized string.</span></span><br/>                                                                                         |



## <a name="remarks"></a><span data-ttu-id="80f9c-127">備註</span><span class="sxs-lookup"><span data-stu-id="80f9c-127">Remarks</span></span>

<span data-ttu-id="80f9c-128">您可以參考任何包含 message 屬性之資訊清單類型的字串。</span><span class="sxs-lookup"><span data-stu-id="80f9c-128">You can reference the strings from any manifest type that contains the message attribute.</span></span> <span data-ttu-id="80f9c-129">若要參考 stringType 為 "string" 且識別碼為 "Printer" 的字串，請使用 $ (字串。[連接) ] 作為 [訊息屬性] 的值。</span><span class="sxs-lookup"><span data-stu-id="80f9c-129">To reference a string with a stringType of "string" and an id of "Printer.Connection", use $(string.Printer.Connection) as the value of the message attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="80f9c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="80f9c-130">Requirements</span></span>



| <span data-ttu-id="80f9c-131">需求</span><span class="sxs-lookup"><span data-stu-id="80f9c-131">Requirement</span></span> | <span data-ttu-id="80f9c-132">值</span><span class="sxs-lookup"><span data-stu-id="80f9c-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80f9c-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80f9c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="80f9c-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80f9c-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80f9c-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80f9c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="80f9c-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80f9c-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





