---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將屬性的值格式化為字串。 這僅適用于 <displayInfo displayType=&\#0034;String&\#0034;> 。
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec05a6eedf1734c1d62c0503027810ad05916160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976818"
---
# <a name="stringformat"></a><span data-ttu-id="4b12f-104">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4b12f-104">stringFormat</span></span>

<span data-ttu-id="4b12f-105">指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。</span><span class="sxs-lookup"><span data-stu-id="4b12f-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="4b12f-106">這僅適用于 <displayInfo displayType="String"> 。</span><span class="sxs-lookup"><span data-stu-id="4b12f-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="4b12f-107">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[stringFormat]()元素。</span><span class="sxs-lookup"><span data-stu-id="4b12f-107">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="4b12f-108">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="4b12f-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="4b12f-109">如果未提供任何 [stringFormat]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="4b12f-109">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b12f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b12f-110">Syntax</span></span>


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="4b12f-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4b12f-111">Element Information</span></span>



| <span data-ttu-id="4b12f-112">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="4b12f-112">Parent Element</span></span>                                   | <span data-ttu-id="4b12f-113">子元素</span><span class="sxs-lookup"><span data-stu-id="4b12f-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="4b12f-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4b12f-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="4b12f-115">無</span><span class="sxs-lookup"><span data-stu-id="4b12f-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="4b12f-116">屬性</span><span class="sxs-lookup"><span data-stu-id="4b12f-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b12f-117">屬性</span><span class="sxs-lookup"><span data-stu-id="4b12f-117">Attribute</span></span></th>
<th><span data-ttu-id="4b12f-118">描述</span><span class="sxs-lookup"><span data-stu-id="4b12f-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b12f-119">formatAs</span><span class="sxs-lookup"><span data-stu-id="4b12f-119">formatAs</span></span></td>
<td><span data-ttu-id="4b12f-120">公用。</span><span class="sxs-lookup"><span data-stu-id="4b12f-120">Public.</span></span> <span data-ttu-id="4b12f-121">選擇性。</span><span class="sxs-lookup"><span data-stu-id="4b12f-121">Optional.</span></span> <span data-ttu-id="4b12f-122">預設值為 &quot; [一般] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="4b12f-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="4b12f-123">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="4b12f-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4b12f-124">值</span><span class="sxs-lookup"><span data-stu-id="4b12f-124">Value</span></span></th>
<th><span data-ttu-id="4b12f-125">意義</span><span class="sxs-lookup"><span data-stu-id="4b12f-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b12f-126">一般</span><span class="sxs-lookup"><span data-stu-id="4b12f-126">General</span></span></td>
<td><span data-ttu-id="4b12f-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="4b12f-127">Default.</span></span> <span data-ttu-id="4b12f-128">以未格式化的字串形式傳回值。</span><span class="sxs-lookup"><span data-stu-id="4b12f-128">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b12f-129">FileName</span><span class="sxs-lookup"><span data-stu-id="4b12f-129">FileName</span></span></td>
<td><span data-ttu-id="4b12f-130">將值格式化為檔案名。</span><span class="sxs-lookup"><span data-stu-id="4b12f-130">Formats the value as a file name.</span></span> <span data-ttu-id="4b12f-131">根據使用者設定隱藏延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4b12f-131">Hides the extension according to user settings.</span></span> <span data-ttu-id="4b12f-132">要求屬性類型必須是字串。</span><span class="sxs-lookup"><span data-stu-id="4b12f-132">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b12f-133">FilePath</span><span class="sxs-lookup"><span data-stu-id="4b12f-133">FilePath</span></span></td>
<td><span data-ttu-id="4b12f-134">將值格式化為檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="4b12f-134">Formats the value as a file path.</span></span> <span data-ttu-id="4b12f-135">根據使用者設定隱藏延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4b12f-135">Hides the extension according to user settings.</span></span> <span data-ttu-id="4b12f-136">要求屬性類型必須是字串。</span><span class="sxs-lookup"><span data-stu-id="4b12f-136">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b12f-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="4b12f-137">Hyperlink</span></span></td>
<td><span data-ttu-id="4b12f-138">將值格式化為超連結。</span><span class="sxs-lookup"><span data-stu-id="4b12f-138">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
