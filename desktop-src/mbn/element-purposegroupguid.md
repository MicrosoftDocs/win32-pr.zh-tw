---
description: PurposeGroupGuid
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroupGuid
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroupGuid
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d20d6c9d1687ea0e3fca344fd3b534ccc0b3ee57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386158"
---
# <a name="span-idwwan_profile_v4element_purposegroupguidspanpurposegroupguid"></a><span data-ttu-id="fca59-103"><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>PurposeGroupGuid</span><span class="sxs-lookup"><span data-stu-id="fca59-103"><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>PurposeGroupGuid</span></span>

<span data-ttu-id="fca59-104">代表 PurposeGroup 設定檔中的一個設定檔。</span><span class="sxs-lookup"><span data-stu-id="fca59-104">Represents one profile in a PurposeGroup of profiles.</span></span>

<span data-ttu-id="fca59-105">設定檔是由其 [**guidType**](simpletype-guidtype.md) 值指定。</span><span class="sxs-lookup"><span data-stu-id="fca59-105">Profiles are specified by their [**guidType**](simpletype-guidtype.md) value.</span></span>

<span data-ttu-id="fca59-106">定義四個 GUID 值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="fca59-106">Four GUID values are defined, as listed in the following table.</span></span>

| <span data-ttu-id="fca59-107">目的群組</span><span class="sxs-lookup"><span data-stu-id="fca59-107">Purpose group</span></span> | <span data-ttu-id="fca59-108">GUID</span><span class="sxs-lookup"><span data-stu-id="fca59-108">GUID</span></span>                                 |
|---------------|--------------------------------------|
| <span data-ttu-id="fca59-109">網際網路</span><span class="sxs-lookup"><span data-stu-id="fca59-109">Internet</span></span>      | <span data-ttu-id="fca59-110">3E5545D2-1137-4DC8-A198-33F1C657515F</span><span class="sxs-lookup"><span data-stu-id="fca59-110">3E5545D2-1137-4DC8-A198-33F1C657515F</span></span> |
| <span data-ttu-id="fca59-111">mms</span><span class="sxs-lookup"><span data-stu-id="fca59-111">MMS</span></span>           | <span data-ttu-id="fca59-112">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span><span class="sxs-lookup"><span data-stu-id="fca59-112">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span></span> |
| <span data-ttu-id="fca59-113">IMS</span><span class="sxs-lookup"><span data-stu-id="fca59-113">IMS</span></span>           | <span data-ttu-id="fca59-114">474D66ED-0E4B-476B-A455-19BB1239ED13</span><span class="sxs-lookup"><span data-stu-id="fca59-114">474D66ED-0E4B-476B-A455-19BB1239ED13</span></span> |
| <span data-ttu-id="fca59-115">SUPL</span><span class="sxs-lookup"><span data-stu-id="fca59-115">SUPL</span></span>          | <span data-ttu-id="fca59-116">6D42669F-52A9-408E-9493-1071DCC437BD</span><span class="sxs-lookup"><span data-stu-id="fca59-116">6D42669F-52A9-408E-9493-1071DCC437BD</span></span> |

 

## <a name="element-hierarchy"></a><span data-ttu-id="fca59-117">元素階層</span><span class="sxs-lookup"><span data-stu-id="fca59-117">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<PurposeGroups>](element-purposegroups.md)  
**<PurposeGroupGuid>**

## <a name="syntax"></a><span data-ttu-id="fca59-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="fca59-118">Syntax</span></span>

``` syntax
<PurposeGroupGuid>

  guidType

</PurposeGroupGuid>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="fca59-119"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="fca59-119"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="fca59-120"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="fca59-120"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="fca59-121">無。</span><span class="sxs-lookup"><span data-stu-id="fca59-121">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="fca59-122"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="fca59-122"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="fca59-123">無。</span><span class="sxs-lookup"><span data-stu-id="fca59-123">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="fca59-124"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="fca59-124"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fca59-125">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="fca59-125">Parent Element</span></span></th>
<th><span data-ttu-id="fca59-126">Description</span><span class="sxs-lookup"><span data-stu-id="fca59-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fca59-127"><a href="element-purposegroups.md">PurposeGroups</a></span><span class="sxs-lookup"><span data-stu-id="fca59-127"><a href="element-purposegroups.md">PurposeGroups</a></span></span></td>
<td><p><span data-ttu-id="fca59-128">選用的設定檔群組清單，其中每個群組都包含用於一般用途的設定檔。</span><span class="sxs-lookup"><span data-stu-id="fca59-128">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span></p>
<p><span data-ttu-id="fca59-129">此元素是架構 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="fca59-129">This element is new for v4 of the schema.</span></span></p>
<p><span data-ttu-id="fca59-130">一個設定檔可以列在多個群組中。</span><span class="sxs-lookup"><span data-stu-id="fca59-130">One profile can be listed in multiple groups.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="fca59-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fca59-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fca59-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="fca59-132">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



