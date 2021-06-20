---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將 booleanFormat 屬性的值格式化為字串。
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 528458d9c31d54ef43eca8325b1daeef4eee1195
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405961"
---
# <a name="booleanformat"></a><span data-ttu-id="41439-103">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="41439-103">booleanFormat</span></span>

<span data-ttu-id="41439-104">指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。</span><span class="sxs-lookup"><span data-stu-id="41439-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="41439-105">這僅適用于 <displayInfo displayType="String"> 。</span><span class="sxs-lookup"><span data-stu-id="41439-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="41439-106">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[booleanFormat]()元素。</span><span class="sxs-lookup"><span data-stu-id="41439-106">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="41439-107">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="41439-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="41439-108">如果未提供任何 [booleanFormat]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="41439-108">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="41439-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="41439-109">Syntax</span></span>


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="41439-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="41439-110">Element Information</span></span>



| <span data-ttu-id="41439-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="41439-111">Parent Element</span></span>                                   | <span data-ttu-id="41439-112">子元素</span><span class="sxs-lookup"><span data-stu-id="41439-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="41439-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="41439-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="41439-114">無</span><span class="sxs-lookup"><span data-stu-id="41439-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="41439-115">屬性</span><span class="sxs-lookup"><span data-stu-id="41439-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41439-116">屬性</span><span class="sxs-lookup"><span data-stu-id="41439-116">Attribute</span></span></th>
<th><span data-ttu-id="41439-117">描述</span><span class="sxs-lookup"><span data-stu-id="41439-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41439-118">formatAs</span><span class="sxs-lookup"><span data-stu-id="41439-118">formatAs</span></span></td>
<td><span data-ttu-id="41439-119">公用。</span><span class="sxs-lookup"><span data-stu-id="41439-119">Public.</span></span> <span data-ttu-id="41439-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="41439-120">Optional.</span></span> <span data-ttu-id="41439-121">預設值為 &quot; YesNo &quot; 。</span><span class="sxs-lookup"><span data-stu-id="41439-121">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="41439-122">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="41439-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="41439-123">值</span><span class="sxs-lookup"><span data-stu-id="41439-123">Value</span></span></th>
<th><span data-ttu-id="41439-124">意義</span><span class="sxs-lookup"><span data-stu-id="41439-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41439-125">YesNo</span><span class="sxs-lookup"><span data-stu-id="41439-125">YesNo</span></span></td>
<td><span data-ttu-id="41439-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="41439-126">Default.</span></span> <span data-ttu-id="41439-127">將值格式化為 &quot; [是] &quot; 或 [否] &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="41439-127">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="41439-128">要求屬性類型必須是布林值。</span><span class="sxs-lookup"><span data-stu-id="41439-128">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41439-129">OnOff</span><span class="sxs-lookup"><span data-stu-id="41439-129">OnOff</span></span></td>
<td><span data-ttu-id="41439-130">將值格式化為 &quot; On &quot; 或 &quot; Off &quot; 。</span><span class="sxs-lookup"><span data-stu-id="41439-130">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="41439-131">要求屬性類型必須是布林值。</span><span class="sxs-lookup"><span data-stu-id="41439-131">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41439-132">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="41439-132">TrueFalse</span></span></td>
<td><span data-ttu-id="41439-133">將值格式化為 &quot; True &quot; 或 &quot; False &quot; 。</span><span class="sxs-lookup"><span data-stu-id="41439-133">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="41439-134">要求屬性類型必須是布林值。</span><span class="sxs-lookup"><span data-stu-id="41439-134">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
