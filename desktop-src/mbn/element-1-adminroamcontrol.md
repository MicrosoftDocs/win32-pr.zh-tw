---
description: 'ModemDMConfigProfile \/ AdminRoamControl (v4) '
MS-HAID: WWAN\_profile\_v4.element\_1\_AdminRoamControl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'AdminRoamControl (v4) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92ba97fd2657b28d1c845598825aae648124d36
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106990871"
---
# <a name="span-idwwan_profile_v4element_1_adminroamcontrolspanmodemdmconfigprofileadminroamcontrol-v4"></a><span data-ttu-id="ed6bf-103"><span id="WWAN_profile_v4.element_1_AdminRoamControl"></span>ModemDMConfigProfile \/ AdminRoamControl (v4) </span><span class="sxs-lookup"><span data-stu-id="ed6bf-103"><span id="WWAN_profile_v4.element_1_AdminRoamControl"></span>ModemDMConfigProfile\/AdminRoamControl (v4)</span></span>

<span data-ttu-id="ed6bf-104">指定設定檔是否為系統管理漫遊控制。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-104">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="ed6bf-105">此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-105">This element is new for v4.</span></span> <span data-ttu-id="ed6bf-106">這個元素的值是 [**roamControlType**](simpletype-roamcontroltype.md) 值。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-106">The value of this element is a [**roamControlType**](simpletype-roamcontroltype.md) value.</span></span> <span data-ttu-id="ed6bf-107">這是選擇性元素;如果未指定任何值，則 **AllRoamAllowed** 為預設值。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-107">This is an optional element; if no value is specified, then **AllRoamAllowed** is the default.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="ed6bf-108">元素階層</span><span class="sxs-lookup"><span data-stu-id="ed6bf-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

## <a name="syntax"></a><span data-ttu-id="ed6bf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed6bf-109">Syntax</span></span>

``` syntax
<AdminRoamControl>

  "AllRoamAllowed" | "PartnerRoamAllowed" | "NoRoamAllowed"

</AdminRoamControl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="ed6bf-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="ed6bf-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="ed6bf-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="ed6bf-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="ed6bf-112">無。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="ed6bf-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="ed6bf-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="ed6bf-114">無。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="ed6bf-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="ed6bf-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed6bf-116">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="ed6bf-116">Parent Element</span></span></th>
<th><span data-ttu-id="ed6bf-117">Description</span><span class="sxs-lookup"><span data-stu-id="ed6bf-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed6bf-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="ed6bf-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="ed6bf-119"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-119">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="ed6bf-120">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-120">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="ed6bf-121">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-121">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="ed6bf-122">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-122">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed6bf-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="ed6bf-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="ed6bf-124">數據機 DM 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ed6bf-124">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="ed6bf-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed6bf-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed6bf-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="ed6bf-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



