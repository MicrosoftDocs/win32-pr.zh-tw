---
description: " (Mobile 寬頻) 的描述-描述"
MS-HAID: WWAN\_profile\_v4.element\_Description
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: " (Mobile 寬頻) 的描述"
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7adc4b26-1202-4f80-8b26-7879df687bb0
api_name:
- Description
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e72b2fca1df6ba76d933d289b5d73b717cb6af6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107016"
---
# <a name="description-mobile-broadband"></a><span data-ttu-id="5078c-103"> (Mobile 寬頻) 的描述</span><span class="sxs-lookup"><span data-stu-id="5078c-103">Description (Mobile Broadband)</span></span>

<span data-ttu-id="5078c-104">設定檔的描述。</span><span class="sxs-lookup"><span data-stu-id="5078c-104">A description of the profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="5078c-105">元素階層</span><span class="sxs-lookup"><span data-stu-id="5078c-105">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<Description>**

## <a name="syntax"></a><span data-ttu-id="5078c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5078c-106">Syntax</span></span>

``` syntax
<Description>

  nameType

</Description>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="5078c-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="5078c-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="5078c-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="5078c-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="5078c-109">無。</span><span class="sxs-lookup"><span data-stu-id="5078c-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="5078c-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="5078c-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="5078c-111">無。</span><span class="sxs-lookup"><span data-stu-id="5078c-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="5078c-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="5078c-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5078c-113">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="5078c-113">Parent Element</span></span></th>
<th><span data-ttu-id="5078c-114">Description</span><span class="sxs-lookup"><span data-stu-id="5078c-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5078c-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="5078c-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="5078c-116"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="5078c-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="5078c-117">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="5078c-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="5078c-118">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="5078c-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="5078c-119">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="5078c-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="5078c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5078c-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5078c-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="5078c-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



