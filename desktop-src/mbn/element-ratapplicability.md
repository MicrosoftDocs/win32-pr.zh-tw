---
description: RATApplicability
MS-HAID: WWAN\_profile\_v4.element\_RATApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RATApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155f8e216b6ec00f123d0fe0f378fd9db2e4d75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848115"
---
# <a name="span-idwwan_profile_v4element_ratapplicabilityspanratapplicability"></a><span data-ttu-id="278d6-103"><span id="WWAN_profile_v4.element_RATApplicability"></span>RATApplicability</span><span class="sxs-lookup"><span data-stu-id="278d6-103"><span id="WWAN_profile_v4.element_RATApplicability"></span>RATApplicability</span></span>

<span data-ttu-id="278d6-104">指定只有當 RAT 類型是指定的時，才會啟用此設定檔。</span><span class="sxs-lookup"><span data-stu-id="278d6-104">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="278d6-105">否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="278d6-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="278d6-106">元素階層</span><span class="sxs-lookup"><span data-stu-id="278d6-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<RATApplicability>**

## <a name="syntax"></a><span data-ttu-id="278d6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="278d6-107">Syntax</span></span>

``` syntax
<RATApplicability>

  "LTE_eHRPD" | "3GPP_LEGACY"

</RATApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="278d6-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="278d6-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="278d6-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="278d6-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="278d6-110">無。</span><span class="sxs-lookup"><span data-stu-id="278d6-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="278d6-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="278d6-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="278d6-112">無。</span><span class="sxs-lookup"><span data-stu-id="278d6-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="278d6-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="278d6-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="278d6-114">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="278d6-114">Parent Element</span></span></th>
<th><span data-ttu-id="278d6-115">Description</span><span class="sxs-lookup"><span data-stu-id="278d6-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="278d6-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="278d6-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="278d6-117">指定必須滿足的條件，設定檔才適用。</span><span class="sxs-lookup"><span data-stu-id="278d6-117">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="278d6-118">此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="278d6-118">This element is new for v4.</span></span> <span data-ttu-id="278d6-119">它可讓您指定在不同條件下套用的多個設定檔，並在適用時自動使用適當的設定檔。</span><span class="sxs-lookup"><span data-stu-id="278d6-119">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="278d6-120">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="278d6-120">This element is optional.</span></span> <span data-ttu-id="278d6-121">如果您未指定，則設定檔一律適用于所列出的條件。</span><span class="sxs-lookup"><span data-stu-id="278d6-121">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="278d6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="278d6-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="278d6-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="278d6-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



