---
description: IwlanApplicability
MS-HAID: WWAN\_profile\_v4.element\_IwlanApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IwlanApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6b8b0376f2ee882a57e4c71e392fb7b02f6eeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972211"
---
# <a name="span-idwwan_profile_v4element_iwlanapplicabilityspaniwlanapplicability"></a><span data-ttu-id="4fab0-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>IwlanApplicability</span><span class="sxs-lookup"><span data-stu-id="4fab0-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>IwlanApplicability</span></span>

<span data-ttu-id="4fab0-104">指定只有在連接到 IWLAN 網路時，才會使用此設定檔。</span><span class="sxs-lookup"><span data-stu-id="4fab0-104">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="4fab0-105">否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4fab0-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="4fab0-106">這個元素的值必須是有效的 [**iwlanApplicabilityType**](simpletype-iwlanapplicabilitytype.md) 值。</span><span class="sxs-lookup"><span data-stu-id="4fab0-106">The value of this element must be a valid [**iwlanApplicabilityType**](simpletype-iwlanapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="4fab0-107">元素階層</span><span class="sxs-lookup"><span data-stu-id="4fab0-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<IwlanApplicability>**

## <a name="syntax"></a><span data-ttu-id="4fab0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fab0-108">Syntax</span></span>

``` syntax
<IwlanApplicability>

  "CellularOnly" | "CellularAndIwlan" | "IwlanOnly"

</IwlanApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="4fab0-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="4fab0-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="4fab0-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="4fab0-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="4fab0-111">無。</span><span class="sxs-lookup"><span data-stu-id="4fab0-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="4fab0-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="4fab0-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="4fab0-113">無。</span><span class="sxs-lookup"><span data-stu-id="4fab0-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="4fab0-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="4fab0-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4fab0-115">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="4fab0-115">Parent Element</span></span></th>
<th><span data-ttu-id="4fab0-116">Description</span><span class="sxs-lookup"><span data-stu-id="4fab0-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4fab0-117"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="4fab0-117"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="4fab0-118">指定必須滿足的條件，設定檔才適用。</span><span class="sxs-lookup"><span data-stu-id="4fab0-118">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="4fab0-119">此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="4fab0-119">This element is new for v4.</span></span> <span data-ttu-id="4fab0-120">它可讓您指定在不同條件下套用的多個設定檔，並在適用時自動使用適當的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4fab0-120">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="4fab0-121">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="4fab0-121">This element is optional.</span></span> <span data-ttu-id="4fab0-122">如果您未指定，則設定檔一律適用于所列出的條件。</span><span class="sxs-lookup"><span data-stu-id="4fab0-122">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="4fab0-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fab0-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fab0-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="4fab0-124">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



