---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType=&\#0034;String&\#0034;> 。
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91332f0cc062e7ee4a83e3584776ecf09c5c4b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944329"
---
# <a name="booleanformat"></a><span data-ttu-id="71eec-104">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="71eec-104">booleanFormat</span></span>

<span data-ttu-id="71eec-105">指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。</span><span class="sxs-lookup"><span data-stu-id="71eec-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="71eec-106">這僅適用于 <displayInfo displayType="String"> 。</span><span class="sxs-lookup"><span data-stu-id="71eec-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="71eec-107">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[booleanFormat]()元素。</span><span class="sxs-lookup"><span data-stu-id="71eec-107">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="71eec-108">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="71eec-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="71eec-109">如果未提供任何 [booleanFormat]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="71eec-109">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="71eec-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="71eec-110">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="71eec-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="71eec-111">Element Information</span></span>



| <span data-ttu-id="71eec-112">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="71eec-112">Parent Element</span></span>                                   | <span data-ttu-id="71eec-113">子元素</span><span class="sxs-lookup"><span data-stu-id="71eec-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="71eec-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="71eec-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="71eec-115">無</span><span class="sxs-lookup"><span data-stu-id="71eec-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="71eec-116">屬性</span><span class="sxs-lookup"><span data-stu-id="71eec-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71eec-117">屬性</span><span class="sxs-lookup"><span data-stu-id="71eec-117">Attribute</span></span></th>
<th><span data-ttu-id="71eec-118">描述</span><span class="sxs-lookup"><span data-stu-id="71eec-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71eec-119">formatAs</span><span class="sxs-lookup"><span data-stu-id="71eec-119">formatAs</span></span></td>
<td><span data-ttu-id="71eec-120">公用。</span><span class="sxs-lookup"><span data-stu-id="71eec-120">Public.</span></span> <span data-ttu-id="71eec-121">選擇性。</span><span class="sxs-lookup"><span data-stu-id="71eec-121">Optional.</span></span> <span data-ttu-id="71eec-122">預設值為 &quot; YesNo &quot; 。</span><span class="sxs-lookup"><span data-stu-id="71eec-122">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="71eec-123">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="71eec-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="71eec-124">值</span><span class="sxs-lookup"><span data-stu-id="71eec-124">Value</span></span></th>
<th><span data-ttu-id="71eec-125">意義</span><span class="sxs-lookup"><span data-stu-id="71eec-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71eec-126">YesNo</span><span class="sxs-lookup"><span data-stu-id="71eec-126">YesNo</span></span></td>
<td><span data-ttu-id="71eec-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="71eec-127">Default.</span></span> <span data-ttu-id="71eec-128">將值格式化為 &quot; [是] &quot; 或 [否] &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="71eec-128">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="71eec-129">要求屬性類型必須是布林值。</span><span class="sxs-lookup"><span data-stu-id="71eec-129">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71eec-130">OnOff</span><span class="sxs-lookup"><span data-stu-id="71eec-130">OnOff</span></span></td>
<td><span data-ttu-id="71eec-131">將值格式化為 &quot; On &quot; 或 &quot; Off &quot; 。</span><span class="sxs-lookup"><span data-stu-id="71eec-131">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="71eec-132">要求屬性類型必須是布林值。</span><span class="sxs-lookup"><span data-stu-id="71eec-132">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71eec-133">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="71eec-133">TrueFalse</span></span></td>
<td><span data-ttu-id="71eec-134">將值格式化為 &quot; True &quot; 或 &quot; False &quot; 。</span><span class="sxs-lookup"><span data-stu-id="71eec-134">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="71eec-135">要求屬性類型必須是布林值。</span><span class="sxs-lookup"><span data-stu-id="71eec-135">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
