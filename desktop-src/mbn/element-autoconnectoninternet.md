---
description: AutoConnectOnInternet
MS-HAID: WWAN\_profile\_v4.element\_AutoConnectOnInternet
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AutoConnectOnInternet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e42d42285ba97e8415fdd1c8e8ddddb329338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973083"
---
# <a name="span-idwwan_profile_v4element_autoconnectoninternetspanautoconnectoninternet"></a><span data-ttu-id="025c0-103"><span id="WWAN_profile_v4.element_AutoConnectOnInternet"></span>AutoConnectOnInternet</span><span class="sxs-lookup"><span data-stu-id="025c0-103"><span id="WWAN_profile_v4.element_AutoConnectOnInternet"></span>AutoConnectOnInternet</span></span>

<span data-ttu-id="025c0-104">指定行動寬頻裝置是否會自動連接到網路。</span><span class="sxs-lookup"><span data-stu-id="025c0-104">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="025c0-105">如需詳細資訊，請參閱 v1 [**AutoConnectOnInternet**](./schema-autoconnectoninternet-mbnprofile-element.md) 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="025c0-105">For more information, see the documentation for the v1 [**AutoConnectOnInternet**](./schema-autoconnectoninternet-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="025c0-106">元素階層</span><span class="sxs-lookup"><span data-stu-id="025c0-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<AutoConnectOnInternet>**

## <a name="syntax"></a><span data-ttu-id="025c0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="025c0-107">Syntax</span></span>

``` syntax
<AutoConnectOnInternet>

  boolean

</AutoConnectOnInternet>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="025c0-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="025c0-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="025c0-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="025c0-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="025c0-110">無。</span><span class="sxs-lookup"><span data-stu-id="025c0-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="025c0-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="025c0-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="025c0-112">無。</span><span class="sxs-lookup"><span data-stu-id="025c0-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="025c0-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="025c0-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="025c0-114">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="025c0-114">Parent Element</span></span></th>
<th><span data-ttu-id="025c0-115">Description</span><span class="sxs-lookup"><span data-stu-id="025c0-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="025c0-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="025c0-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="025c0-117"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="025c0-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="025c0-118">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="025c0-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="025c0-119">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="025c0-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="025c0-120">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="025c0-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="025c0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="025c0-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="025c0-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="025c0-122">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
