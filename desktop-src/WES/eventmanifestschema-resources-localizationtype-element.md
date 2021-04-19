---
title: 資源 (LocalizationType) 元素
description: 定義字串資料表的群組，其中包含您在資訊清單中參考的當地語系化字串。
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- resources 元素 EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969554"
---
# <a name="resources-localizationtype-element"></a><span data-ttu-id="14720-104">資源 (LocalizationType) 元素</span><span class="sxs-lookup"><span data-stu-id="14720-104">resources (LocalizationType) Element</span></span>

<span data-ttu-id="14720-105">定義字串資料表的群組，其中包含您在資訊清單中參考的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="14720-105">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span>

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="14720-106">**Resources** 元素是由 [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="14720-106">The **resources** element is defined by the [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="14720-107">子元素</span><span class="sxs-lookup"><span data-stu-id="14720-107">Child elements</span></span>



| <span data-ttu-id="14720-108">元素</span><span class="sxs-lookup"><span data-stu-id="14720-108">Element</span></span>                                                                  | <span data-ttu-id="14720-109">類型</span><span class="sxs-lookup"><span data-stu-id="14720-109">Type</span></span>                                                                       | <span data-ttu-id="14720-110">Description</span><span class="sxs-lookup"><span data-stu-id="14720-110">Description</span></span>                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="14720-111">**stringTable**</span><span class="sxs-lookup"><span data-stu-id="14720-111">**stringTable**</span></span>](eventmanifestschema-stringtable-resources-element.md) | [<span data-ttu-id="14720-112">**StringTableType**</span><span class="sxs-lookup"><span data-stu-id="14720-112">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="14720-113">定義您可以在資訊清單中參考的當地語系化字串清單。</span><span class="sxs-lookup"><span data-stu-id="14720-113">Defines a list of localized strings that you can reference in your manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="14720-114">屬性</span><span class="sxs-lookup"><span data-stu-id="14720-114">Attributes</span></span>



| <span data-ttu-id="14720-115">名稱</span><span class="sxs-lookup"><span data-stu-id="14720-115">Name</span></span>    | <span data-ttu-id="14720-116">類型</span><span class="sxs-lookup"><span data-stu-id="14720-116">Type</span></span>   | <span data-ttu-id="14720-117">Description</span><span class="sxs-lookup"><span data-stu-id="14720-117">Description</span></span>                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14720-118">culture</span><span class="sxs-lookup"><span data-stu-id="14720-118">culture</span></span> | <span data-ttu-id="14720-119">字串</span><span class="sxs-lookup"><span data-stu-id="14720-119">string</span></span> | <span data-ttu-id="14720-120">用來識別字串資料表中當地語系化字串文化特性的語言名稱。</span><span class="sxs-lookup"><span data-stu-id="14720-120">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="14720-121">例如，"en-us" 代表英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="14720-121">For example, "en-US" for English (United States).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="14720-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="14720-122">Requirements</span></span>



| <span data-ttu-id="14720-123">需求</span><span class="sxs-lookup"><span data-stu-id="14720-123">Requirement</span></span> | <span data-ttu-id="14720-124">值</span><span class="sxs-lookup"><span data-stu-id="14720-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14720-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14720-125">Minimum supported client</span></span><br/> | <span data-ttu-id="14720-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14720-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14720-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14720-127">Minimum supported server</span></span><br/> | <span data-ttu-id="14720-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14720-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14720-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14720-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="14720-130">**父元素**</span><span class="sxs-lookup"><span data-stu-id="14720-130">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="14720-131">**當地語系化 (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="14720-131">**localization (instrumentationManifest)**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





