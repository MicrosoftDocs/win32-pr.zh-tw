---
description: PurposeGroups
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroups
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370cf6b0dc13848ca21a2a06e0b9806d753878c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973260"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span data-ttu-id="7819f-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span><span class="sxs-lookup"><span data-stu-id="7819f-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span></span>

<span data-ttu-id="7819f-104">選用的設定檔群組清單，其中每個群組都包含用於一般用途的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7819f-104">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span>

<span data-ttu-id="7819f-105">此元素是架構 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="7819f-105">This element is new for v4 of the schema.</span></span>

<span data-ttu-id="7819f-106">一個設定檔可以列在多個群組中。</span><span class="sxs-lookup"><span data-stu-id="7819f-106">One profile can be listed in multiple groups.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="7819f-107">元素階層</span><span class="sxs-lookup"><span data-stu-id="7819f-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a><span data-ttu-id="7819f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7819f-108">Syntax</span></span>

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a><span data-ttu-id="7819f-109">答案</span><span class="sxs-lookup"><span data-stu-id="7819f-109">Key</span></span>

<span data-ttu-id="7819f-110">`{}`   出現的特定範圍</span><span class="sxs-lookup"><span data-stu-id="7819f-110">`{}`   specific range of occurrences</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="7819f-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="7819f-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="7819f-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="7819f-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="7819f-113">無。</span><span class="sxs-lookup"><span data-stu-id="7819f-113">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="7819f-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="7819f-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7819f-115">子元素</span><span class="sxs-lookup"><span data-stu-id="7819f-115">Child Element</span></span></th>
<th><span data-ttu-id="7819f-116">Description</span><span class="sxs-lookup"><span data-stu-id="7819f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7819f-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span><span class="sxs-lookup"><span data-stu-id="7819f-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span></span></td>
<td><p><span data-ttu-id="7819f-118">代表 PurposeGroup 設定檔中的一個設定檔。</span><span class="sxs-lookup"><span data-stu-id="7819f-118">Represents one profile in a PurposeGroup of profiles.</span></span></p>
<p><span data-ttu-id="7819f-119">設定檔是由其 <a href="simpletype-guidtype.md"><strong>guidType</strong></a> 值指定。</span><span class="sxs-lookup"><span data-stu-id="7819f-119">Profiles are specified by their <a href="simpletype-guidtype.md"><strong>guidType</strong></a> value.</span></span></p>
<p><span data-ttu-id="7819f-120">定義四個 GUID 值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="7819f-120">Four GUID values are defined, as listed in the following table.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7819f-121">目的群組</span><span class="sxs-lookup"><span data-stu-id="7819f-121">Purpose group</span></span></th>
<th><span data-ttu-id="7819f-122">GUID</span><span class="sxs-lookup"><span data-stu-id="7819f-122">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7819f-123">網際網路</span><span class="sxs-lookup"><span data-stu-id="7819f-123">Internet</span></span></td>
<td><span data-ttu-id="7819f-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span><span class="sxs-lookup"><span data-stu-id="7819f-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7819f-125">mms</span><span class="sxs-lookup"><span data-stu-id="7819f-125">MMS</span></span></td>
<td><span data-ttu-id="7819f-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span><span class="sxs-lookup"><span data-stu-id="7819f-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7819f-127">IMS</span><span class="sxs-lookup"><span data-stu-id="7819f-127">IMS</span></span></td>
<td><span data-ttu-id="7819f-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span><span class="sxs-lookup"><span data-stu-id="7819f-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7819f-129">SUPL</span><span class="sxs-lookup"><span data-stu-id="7819f-129">SUPL</span></span></td>
<td><span data-ttu-id="7819f-130">6D42669F-52A9-408E-9493-1071DCC437BD</span><span class="sxs-lookup"><span data-stu-id="7819f-130">6D42669F-52A9-408E-9493-1071DCC437BD</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="7819f-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="7819f-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7819f-132">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="7819f-132">Parent Element</span></span></th>
<th><span data-ttu-id="7819f-133">Description</span><span class="sxs-lookup"><span data-stu-id="7819f-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7819f-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="7819f-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="7819f-135"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="7819f-135">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="7819f-136">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="7819f-136">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="7819f-137">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="7819f-137">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="7819f-138">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7819f-138">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="7819f-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="7819f-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7819f-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="7819f-140">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



