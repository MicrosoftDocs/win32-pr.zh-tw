---
description: ICONFilePath
MS-HAID: WWAN\_profile\_v4.element\_ICONFilePath
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ICONFilePath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273f8a48cb099c95aaa0b54d438e06b3e1f0bb63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974029"
---
# <a name="span-idwwan_profile_v4element_iconfilepathspaniconfilepath"></a><span data-ttu-id="40de7-103"><span id="WWAN_profile_v4.element_ICONFilePath"></span>ICONFilePath</span><span class="sxs-lookup"><span data-stu-id="40de7-103"><span id="WWAN_profile_v4.element_ICONFilePath"></span>ICONFilePath</span></span>

<span data-ttu-id="40de7-104">連接的圖示檔路徑。</span><span class="sxs-lookup"><span data-stu-id="40de7-104">The path to the icon file for the connection.</span></span> <span data-ttu-id="40de7-105">當使用此設定檔建立連接時，作業系統連接使用者介面會顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="40de7-105">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span>

<span data-ttu-id="40de7-106">如需使用此元素的詳細資訊，請參閱 [**ICONFilePath**](./schema-iconfilepath-mbnprofile-element.md)的 v1 檔。</span><span class="sxs-lookup"><span data-stu-id="40de7-106">For more details on using this element, see the v1 documentation for [**ICONFilePath**](./schema-iconfilepath-mbnprofile-element.md).</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="40de7-107">元素階層</span><span class="sxs-lookup"><span data-stu-id="40de7-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ICONFilePath>**

## <a name="syntax"></a><span data-ttu-id="40de7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="40de7-108">Syntax</span></span>

``` syntax
<ICONFilePath>

  iconFileType

</ICONFilePath>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="40de7-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="40de7-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="40de7-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="40de7-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="40de7-111">無。</span><span class="sxs-lookup"><span data-stu-id="40de7-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="40de7-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="40de7-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="40de7-113">無。</span><span class="sxs-lookup"><span data-stu-id="40de7-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="40de7-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="40de7-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40de7-115">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="40de7-115">Parent Element</span></span></th>
<th><span data-ttu-id="40de7-116">Description</span><span class="sxs-lookup"><span data-stu-id="40de7-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40de7-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="40de7-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="40de7-118"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="40de7-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="40de7-119">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="40de7-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="40de7-120">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="40de7-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="40de7-121">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="40de7-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="40de7-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="40de7-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40de7-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="40de7-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
