---
title: LocalizationType 複雜類型
description: 定義您在資訊清單中參考的當地語系化資源群組。 |LocalizationType 複雜類型
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- LocalizationType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981070"
---
# <a name="localizationtype-complex-type"></a><span data-ttu-id="3f3f7-105">LocalizationType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="3f3f7-105">LocalizationType Complex Type</span></span>

<span data-ttu-id="3f3f7-106">定義您在資訊清單中參考的當地語系化資源群組。</span><span class="sxs-lookup"><span data-stu-id="3f3f7-106">Defines a group of localized resources that you reference in your manifest.</span></span>

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3f3f7-107">子元素</span><span class="sxs-lookup"><span data-stu-id="3f3f7-107">Child elements</span></span>



| <span data-ttu-id="3f3f7-108">元素</span><span class="sxs-lookup"><span data-stu-id="3f3f7-108">Element</span></span>                                                                         | <span data-ttu-id="3f3f7-109">類型</span><span class="sxs-lookup"><span data-stu-id="3f3f7-109">Type</span></span>                                                                       | <span data-ttu-id="3f3f7-110">Description</span><span class="sxs-lookup"><span data-stu-id="3f3f7-110">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f3f7-111">**資源**</span><span class="sxs-lookup"><span data-stu-id="3f3f7-111">**resources**</span></span>](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | <span data-ttu-id="3f3f7-112">定義字串資料表的群組，其中包含您在資訊清單中參考的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="3f3f7-112">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span><br/> |
| [<span data-ttu-id="3f3f7-113">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="3f3f7-113">**stringTable**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md) | [<span data-ttu-id="3f3f7-114">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="3f3f7-114">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="3f3f7-115">定義您可以在資訊清單中參考的當地語系化字串清單。</span><span class="sxs-lookup"><span data-stu-id="3f3f7-115">Defines a list of localized strings that you can reference in your manifest.</span></span><br/>                             |



## <a name="attributes"></a><span data-ttu-id="3f3f7-116">屬性</span><span class="sxs-lookup"><span data-stu-id="3f3f7-116">Attributes</span></span>



| <span data-ttu-id="3f3f7-117">名稱</span><span class="sxs-lookup"><span data-stu-id="3f3f7-117">Name</span></span>            | <span data-ttu-id="3f3f7-118">類型</span><span class="sxs-lookup"><span data-stu-id="3f3f7-118">Type</span></span>   | <span data-ttu-id="3f3f7-119">Description</span><span class="sxs-lookup"><span data-stu-id="3f3f7-119">Description</span></span>                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3f7-120">culture</span><span class="sxs-lookup"><span data-stu-id="3f3f7-120">culture</span></span>         | <span data-ttu-id="3f3f7-121">字串</span><span class="sxs-lookup"><span data-stu-id="3f3f7-121">string</span></span> | <span data-ttu-id="3f3f7-122">用來識別字串資料表中當地語系化字串文化特性的語言名稱。</span><span class="sxs-lookup"><span data-stu-id="3f3f7-122">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="3f3f7-123">例如，"en-us" 代表英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="3f3f7-123">For example, "en-US" for English (United States).</span></span><br/> |
| <span data-ttu-id="3f3f7-124">fallbackCulture</span><span class="sxs-lookup"><span data-stu-id="3f3f7-124">fallbackCulture</span></span> | <span data-ttu-id="3f3f7-125">字串</span><span class="sxs-lookup"><span data-stu-id="3f3f7-125">string</span></span> | <span data-ttu-id="3f3f7-126">未使用。</span><span class="sxs-lookup"><span data-stu-id="3f3f7-126">Not used.</span></span><br/>                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="3f3f7-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f3f7-127">Requirements</span></span>



| <span data-ttu-id="3f3f7-128">需求</span><span class="sxs-lookup"><span data-stu-id="3f3f7-128">Requirement</span></span> | <span data-ttu-id="3f3f7-129">值</span><span class="sxs-lookup"><span data-stu-id="3f3f7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f3f7-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f3f7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3f7-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f3f7-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f3f7-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f3f7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3f7-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f3f7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





