---
description: IsExclusiveToOther
MS-HAID: WWAN\_profile\_v4.element\_IsExclusiveToOther
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsExclusiveToOther
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a948ad9b6a457f74e98eab745d851bdd2399c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970986"
---
# <a name="span-idwwan_profile_v4element_isexclusivetootherspanisexclusivetoother"></a><span data-ttu-id="b6b53-103"><span id="WWAN_profile_v4.element_IsExclusiveToOther"></span>IsExclusiveToOther</span><span class="sxs-lookup"><span data-stu-id="b6b53-103"><span id="WWAN_profile_v4.element_IsExclusiveToOther"></span>IsExclusiveToOther</span></span>

<span data-ttu-id="b6b53-104">指定此設定檔對於相同設定檔集 (s) 的其他設定檔是專屬的。此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="b6b53-104">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="b6b53-105">元素階層</span><span class="sxs-lookup"><span data-stu-id="b6b53-105">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<IsExclusiveToOther>**

## <a name="syntax"></a><span data-ttu-id="b6b53-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6b53-106">Syntax</span></span>

``` syntax
<IsExclusiveToOther>

  boolean

</IsExclusiveToOther>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="b6b53-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="b6b53-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="b6b53-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="b6b53-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="b6b53-109">無。</span><span class="sxs-lookup"><span data-stu-id="b6b53-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="b6b53-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="b6b53-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="b6b53-111">無。</span><span class="sxs-lookup"><span data-stu-id="b6b53-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="b6b53-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="b6b53-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6b53-113">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="b6b53-113">Parent Element</span></span></th>
<th><span data-ttu-id="b6b53-114">Description</span><span class="sxs-lookup"><span data-stu-id="b6b53-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6b53-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="b6b53-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="b6b53-116"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="b6b53-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="b6b53-117">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6b53-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="b6b53-118">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="b6b53-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="b6b53-119">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6b53-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="b6b53-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6b53-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6b53-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="b6b53-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



