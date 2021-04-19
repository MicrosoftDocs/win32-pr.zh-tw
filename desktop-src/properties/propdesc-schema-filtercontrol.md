---
description: 指定要在標頭篩選功能表中使用的控制項。
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996666"
---
# <a name="filtercontrol"></a><span data-ttu-id="dfc9d-103">filterControl</span><span class="sxs-lookup"><span data-stu-id="dfc9d-103">filterControl</span></span>

<span data-ttu-id="dfc9d-104">指定要在標頭篩選功能表中使用的控制項。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-104">Specifies what control to use in the header filter menu.</span></span> <span data-ttu-id="dfc9d-105">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[filterControl]()元素。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-105">There should be only one [filterControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="dfc9d-106">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="dfc9d-107">如果未提供任何 [filterControl]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-107">If no [filterControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc9d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfc9d-108">Syntax</span></span>


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="dfc9d-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="dfc9d-109">Element Information</span></span>



| <span data-ttu-id="dfc9d-110">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="dfc9d-110">Parent Element</span></span>                                   | <span data-ttu-id="dfc9d-111">子元素</span><span class="sxs-lookup"><span data-stu-id="dfc9d-111">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="dfc9d-112">displayInfo</span><span class="sxs-lookup"><span data-stu-id="dfc9d-112">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="dfc9d-113">無</span><span class="sxs-lookup"><span data-stu-id="dfc9d-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="dfc9d-114">屬性</span><span class="sxs-lookup"><span data-stu-id="dfc9d-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dfc9d-115">屬性</span><span class="sxs-lookup"><span data-stu-id="dfc9d-115">Attribute</span></span></th>
<th><span data-ttu-id="dfc9d-116">描述</span><span class="sxs-lookup"><span data-stu-id="dfc9d-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfc9d-117">控制</span><span class="sxs-lookup"><span data-stu-id="dfc9d-117">control</span></span></td>
<td><span data-ttu-id="dfc9d-118">公用。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-118">Public.</span></span> <span data-ttu-id="dfc9d-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-119">Optional.</span></span> <span data-ttu-id="dfc9d-120">預設值為預設值 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-120">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="dfc9d-121">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-121">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dfc9d-122">值</span><span class="sxs-lookup"><span data-stu-id="dfc9d-122">Value</span></span></th>
<th><span data-ttu-id="dfc9d-123">意義</span><span class="sxs-lookup"><span data-stu-id="dfc9d-123">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfc9d-124">預設</span><span class="sxs-lookup"><span data-stu-id="dfc9d-124">Default</span></span></td>
<td><span data-ttu-id="dfc9d-125">預設值。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-125">Default.</span></span> <span data-ttu-id="dfc9d-126">根據屬性使用預設控制項 <typeInfo type=&quot;&quot;> 。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-126">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="dfc9d-127">預設類型為 &quot; DateTime &quot; ，預設控制項為行事 &quot; 曆 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-127">The default type is &quot;DateTime&quot; and the default control is &quot;Calendar&quot;.</span></span> <span data-ttu-id="dfc9d-128">任何其他類型都不會產生特殊的篩選控制項。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-128">Any other type results in no special filter control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfc9d-129">Calendar</span><span class="sxs-lookup"><span data-stu-id="dfc9d-129">Calendar</span></span></td>
<td><span data-ttu-id="dfc9d-130">使用行事曆控制項。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-130">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfc9d-131">分級</span><span class="sxs-lookup"><span data-stu-id="dfc9d-131">Rating</span></span></td>
<td><span data-ttu-id="dfc9d-132">使用5顆星的評等控制項。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-132">Uses the 5-star rating control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
