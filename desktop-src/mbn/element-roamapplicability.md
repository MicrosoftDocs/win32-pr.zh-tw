---
description: 'MBNProfileExt \/ RoamApplicability (v4) '
MS-HAID: WWAN\_profile\_v4.element\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RoamApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29438df96a3a12bb791870b1cc0d59e84f77d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970413"
---
# <a name="span-idwwan_profile_v4element_roamapplicabilityspanmbnprofileextroamapplicability-v4"></a><span data-ttu-id="9c7c5-103"><span id="WWAN_profile_v4.element_RoamApplicability"></span>MBNProfileExt \/ RoamApplicability (v4) </span><span class="sxs-lookup"><span data-stu-id="9c7c5-103"><span id="WWAN_profile_v4.element_RoamApplicability"></span>MBNProfileExt\/RoamApplicability (v4)</span></span>

<span data-ttu-id="9c7c5-104">指定只有在目前的漫遊條件是指定的漫遊條件時，才會使用此設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-104">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="9c7c5-105">否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="9c7c5-106">這個元素的值必須是有效的 [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) 值。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-106">The value of this element must be a valid [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="9c7c5-107">元素階層</span><span class="sxs-lookup"><span data-stu-id="9c7c5-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a><span data-ttu-id="9c7c5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c7c5-108">Syntax</span></span>

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="9c7c5-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="9c7c5-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="9c7c5-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="9c7c5-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="9c7c5-111">無。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="9c7c5-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="9c7c5-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="9c7c5-113">無。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="9c7c5-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="9c7c5-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c7c5-115">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="9c7c5-115">Parent Element</span></span></th>
<th><span data-ttu-id="9c7c5-116">Description</span><span class="sxs-lookup"><span data-stu-id="9c7c5-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c7c5-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="9c7c5-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="9c7c5-118">數據機 DM 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-118">Modem DM configuration profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c7c5-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="9c7c5-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="9c7c5-120">指定必須滿足的條件，設定檔才適用。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-120">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="9c7c5-121">此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-121">This element is new for v4.</span></span> <span data-ttu-id="9c7c5-122">它可讓您指定在不同條件下套用的多個設定檔，並在適用時自動使用適當的設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-122">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="9c7c5-123">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-123">This element is optional.</span></span> <span data-ttu-id="9c7c5-124">如果您未指定，則設定檔一律適用于所列出的條件。</span><span class="sxs-lookup"><span data-stu-id="9c7c5-124">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="9c7c5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c7c5-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c7c5-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="9c7c5-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



