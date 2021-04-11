---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112912"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span data-ttu-id="f9d9f-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span><span class="sxs-lookup"><span data-stu-id="f9d9f-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span></span>

<span data-ttu-id="f9d9f-104">指定必須滿足的條件，設定檔才適用。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-104">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span>

<span data-ttu-id="f9d9f-105">此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-105">This element is new for v4.</span></span> <span data-ttu-id="f9d9f-106">它可讓您指定在不同條件下套用的多個設定檔，並在適用時自動使用適當的設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-106">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="f9d9f-107">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-107">This element is optional.</span></span> <span data-ttu-id="f9d9f-108">如果您未指定，則設定檔一律適用于所列出的條件。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-108">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="f9d9f-109">元素階層</span><span class="sxs-lookup"><span data-stu-id="f9d9f-109">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a><span data-ttu-id="f9d9f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9d9f-110">Syntax</span></span>

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a><span data-ttu-id="f9d9f-111">答案</span><span class="sxs-lookup"><span data-stu-id="f9d9f-111">Key</span></span>

<span data-ttu-id="f9d9f-112">`?`   選擇性 (零或一) </span><span class="sxs-lookup"><span data-stu-id="f9d9f-112">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="f9d9f-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="f9d9f-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="f9d9f-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="f9d9f-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="f9d9f-115">無。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="f9d9f-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="f9d9f-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9d9f-117">子元素</span><span class="sxs-lookup"><span data-stu-id="f9d9f-117">Child Element</span></span></th>
<th><span data-ttu-id="f9d9f-118">Description</span><span class="sxs-lookup"><span data-stu-id="f9d9f-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9d9f-119"><a href="element-cellularclass.md">CellularClass</a></span><span class="sxs-lookup"><span data-stu-id="f9d9f-119"><a href="element-cellularclass.md">CellularClass</a></span></span></td>
<td><p><span data-ttu-id="f9d9f-120">指定只有當目前的行動電話類別是指定的時，才會使用此設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-120">Specifies that this profile is active only when the current cellular class is the one specified.</span></span> <span data-ttu-id="f9d9f-121">否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-121">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9d9f-122"><a href="element-imsi.md">IMSI</a></span><span class="sxs-lookup"><span data-stu-id="f9d9f-122"><a href="element-imsi.md">IMSI</a></span></span></td>
<td><p><span data-ttu-id="f9d9f-123">指定只有在 ICCID 中目前使用的 IMSI 為指定的時，才會使用此設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-123">Specifies that this profile is active only when the current IMSI being used in the ICCID is the one specified.</span></span> <span data-ttu-id="f9d9f-124">否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-124">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9d9f-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span><span class="sxs-lookup"><span data-stu-id="f9d9f-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span></span></td>
<td><p><span data-ttu-id="f9d9f-126">指定只有在連接到 IWLAN 網路時，才會使用此設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-126">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="f9d9f-127">否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-127">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="f9d9f-128">這個元素的值必須是有效的 <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> 值。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-128">The value of this element must be a valid <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9d9f-129"><a href="element-ratapplicability.md">RATApplicability</a></span><span class="sxs-lookup"><span data-stu-id="f9d9f-129"><a href="element-ratapplicability.md">RATApplicability</a></span></span></td>
<td><p><span data-ttu-id="f9d9f-130">指定只有當 RAT 類型是指定的時，才會啟用此設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-130">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="f9d9f-131">否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-131">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9d9f-132"><a href="element-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="f9d9f-132"><a href="element-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="f9d9f-133">指定只有在目前的漫遊條件是指定的漫遊條件時，才會使用此設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-133">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="f9d9f-134">否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-134">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="f9d9f-135">這個元素的值必須是有效的 <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> 值。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-135">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="f9d9f-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="f9d9f-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9d9f-137">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="f9d9f-137">Parent Element</span></span></th>
<th><span data-ttu-id="f9d9f-138">Description</span><span class="sxs-lookup"><span data-stu-id="f9d9f-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9d9f-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="f9d9f-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="f9d9f-140"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-140">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="f9d9f-141">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-141">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="f9d9f-142">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-142">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="f9d9f-143">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9d9f-143">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="f9d9f-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9d9f-144">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9d9f-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="f9d9f-145">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



