---
description: 指定包含排序屬性或排序屬性清單的元素，以指定排序別名或排序別名的清單。
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: System.management.automation.aliasinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974608"
---
# <a name="aliasinfo"></a><span data-ttu-id="e06e6-103">System.management.automation.aliasinfo</span><span class="sxs-lookup"><span data-stu-id="e06e6-103">aliasInfo</span></span>

<span data-ttu-id="e06e6-104">指定包含排序屬性或排序屬性清單的元素，以指定排序別名或排序別名的清單。</span><span class="sxs-lookup"><span data-stu-id="e06e6-104">Specifies a sort alias or list of sort aliases by specifying an element that contains a sort property or list of sort properties.</span></span> <span data-ttu-id="e06e6-105">每個[propertyDescription](./propdesc-schema-propertydescription.md)專案都只能有一個[system.management.automation.aliasinfo]()元素。</span><span class="sxs-lookup"><span data-stu-id="e06e6-105">There should be only one [aliasInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span> <span data-ttu-id="e06e6-106">針對設定 canGroupBy = true 的屬性，除非指定了次要 sort 屬性 (aliasInfo/@additionalSortByAliases =： example) ，否則使用者可能會在依屬性分組的視圖中變更排序次序時遇到非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="e06e6-106">For properties that set canGroupBy=true, unless a secondary sort property is specified (aliasInfo/@additionalSortByAliases=prop:example), the user may experience unexpected behavior when changing the sort order in a view that is grouped by the property.</span></span> <span data-ttu-id="e06e6-107">具體來說，群組的順序將會變更，但群組內的專案順序則不會變更。</span><span class="sxs-lookup"><span data-stu-id="e06e6-107">Specifically, the order of the groups will change, but the order of items within the groups will not.</span></span>

## <a name="syntax"></a><span data-ttu-id="e06e6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e06e6-108">Syntax</span></span>


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="e06e6-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e06e6-109">Element Information</span></span>



| <span data-ttu-id="e06e6-110">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="e06e6-110">Parent Element</span></span>                                                   | <span data-ttu-id="e06e6-111">子元素</span><span class="sxs-lookup"><span data-stu-id="e06e6-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="e06e6-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e06e6-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="e06e6-113">無</span><span class="sxs-lookup"><span data-stu-id="e06e6-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="e06e6-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e06e6-114">Attributes</span></span>



| <span data-ttu-id="e06e6-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e06e6-115">Attribute</span></span>               | <span data-ttu-id="e06e6-116">描述</span><span class="sxs-lookup"><span data-stu-id="e06e6-116">Description</span></span>                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e06e6-117">sortByAlias</span><span class="sxs-lookup"><span data-stu-id="e06e6-117">sortByAlias</span></span>             | <span data-ttu-id="e06e6-118">公用。</span><span class="sxs-lookup"><span data-stu-id="e06e6-118">Public.</span></span> <span data-ttu-id="e06e6-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e06e6-119">Optional.</span></span> <span data-ttu-id="e06e6-120">應該用來排序的屬性的標準名稱。</span><span class="sxs-lookup"><span data-stu-id="e06e6-120">The canonical name of the property that should be used to sort by.</span></span> <span data-ttu-id="e06e6-121">這個字串的型別是標準型別。</span><span class="sxs-lookup"><span data-stu-id="e06e6-121">This string is of type canonical-type.</span></span>                                            |
| <span data-ttu-id="e06e6-122">additionalSortByAliases</span><span class="sxs-lookup"><span data-stu-id="e06e6-122">additionalSortByAliases</span></span> | <span data-ttu-id="e06e6-123">公用。</span><span class="sxs-lookup"><span data-stu-id="e06e6-123">Public.</span></span> <span data-ttu-id="e06e6-124">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e06e6-124">Optional.</span></span> <span data-ttu-id="e06e6-125">要在排序時使用的其他屬性清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="e06e6-125">A semi-colon delimited list of additional properties to be used when sorting.</span></span> <span data-ttu-id="e06e6-126">這些屬性會套用到其指定順序中的排序。</span><span class="sxs-lookup"><span data-stu-id="e06e6-126">The properties are applied to the sort in the sequence they are given.</span></span> |



 

 

 
