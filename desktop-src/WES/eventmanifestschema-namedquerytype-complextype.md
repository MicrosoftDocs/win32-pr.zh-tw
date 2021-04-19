---
title: NamedQueryType 複雜類型
description: 未使用。 定義已命名查詢的清單，這些查詢會查詢事件訊息字串中的值，並執行指定的動作（如果找到的話）。 |NamedQueryType 複雜類型
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- NamedQueryType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981238"
---
# <a name="namedquerytype-complex-type"></a><span data-ttu-id="33e26-106">NamedQueryType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="33e26-106">NamedQueryType Complex Type</span></span>

<span data-ttu-id="33e26-107">未使用。</span><span class="sxs-lookup"><span data-stu-id="33e26-107">Not used.</span></span> <span data-ttu-id="33e26-108">定義已命名查詢的清單，這些查詢會查詢事件訊息字串中的值，並執行指定的動作（如果找到的話）。</span><span class="sxs-lookup"><span data-stu-id="33e26-108">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span>

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="33e26-109">子元素</span><span class="sxs-lookup"><span data-stu-id="33e26-109">Child elements</span></span>



| <span data-ttu-id="33e26-110">元素</span><span class="sxs-lookup"><span data-stu-id="33e26-110">Element</span></span>                                                                       | <span data-ttu-id="33e26-111">類型</span><span class="sxs-lookup"><span data-stu-id="33e26-111">Type</span></span>                                                                             | <span data-ttu-id="33e26-112">Description</span><span class="sxs-lookup"><span data-stu-id="33e26-112">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33e26-113">**patternMaps**</span><span class="sxs-lookup"><span data-stu-id="33e26-113">**patternMaps**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md) | [<span data-ttu-id="33e26-114">**PatternMapListType**</span><span class="sxs-lookup"><span data-stu-id="33e26-114">**PatternMapListType**</span></span>](eventmanifestschema-patternmaplisttype-complextype.md) | <span data-ttu-id="33e26-115">定義用來改變訊息字串的正則運算式組清單。</span><span class="sxs-lookup"><span data-stu-id="33e26-115">Defines a list of regular expression pairs that are used to alter the message string.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="33e26-116">範例</span><span class="sxs-lookup"><span data-stu-id="33e26-116">Examples</span></span>

<span data-ttu-id="33e26-117">下列範例示範如何使用 [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="33e26-117">The following example shows how to use the [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) element.</span></span> <span data-ttu-id="33e26-118">此範例會取得訊息字串的內容，並將其插入字串 https://www 。*messagestring*.com。</span><span class="sxs-lookup"><span data-stu-id="33e26-118">This example takes the contents of the message string and inserts it into the string https://www.*messagestring*.com.</span></span> <span data-ttu-id="33e26-119">然後，它會將訊息字串取代為結果。</span><span class="sxs-lookup"><span data-stu-id="33e26-119">It then replaces the message string with the result.</span></span> <span data-ttu-id="33e26-120">例如，如果訊息字串包含 Microsoft，則查詢會將 Microsoft message 字串取代為 https://www.Microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="33e26-120">For example, if the message string contained Microsoft, the query would replace the Microsoft message string with https://www.Microsoft.com.</span></span>


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a><span data-ttu-id="33e26-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="33e26-121">Requirements</span></span>



| <span data-ttu-id="33e26-122">需求</span><span class="sxs-lookup"><span data-stu-id="33e26-122">Requirement</span></span> | <span data-ttu-id="33e26-123">值</span><span class="sxs-lookup"><span data-stu-id="33e26-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="33e26-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33e26-124">Minimum supported client</span></span><br/> | <span data-ttu-id="33e26-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33e26-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="33e26-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33e26-126">Minimum supported server</span></span><br/> | <span data-ttu-id="33e26-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33e26-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





