---
description: 指定 IPropertyDescription：： FormatForDisplay 應該如何將 stringFormat 屬性的值格式化為字串。
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730355507b78d99eba02e82666427dd29425c942
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408351"
---
# <a name="stringformat"></a><span data-ttu-id="0c86e-103">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0c86e-103">stringFormat</span></span>

<span data-ttu-id="0c86e-104">指定 [**IPropertyDescription：： FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) 應該如何將屬性的值格式化為字串。</span><span class="sxs-lookup"><span data-stu-id="0c86e-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="0c86e-105">這僅適用于 <displayInfo displayType="String"> 。</span><span class="sxs-lookup"><span data-stu-id="0c86e-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="0c86e-106">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[stringFormat]()元素。</span><span class="sxs-lookup"><span data-stu-id="0c86e-106">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="0c86e-107">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="0c86e-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="0c86e-108">如果未提供任何 [stringFormat]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="0c86e-108">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c86e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c86e-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="0c86e-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0c86e-110">Element Information</span></span>



| <span data-ttu-id="0c86e-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="0c86e-111">Parent Element</span></span>                                   | <span data-ttu-id="0c86e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0c86e-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="0c86e-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0c86e-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="0c86e-114">無</span><span class="sxs-lookup"><span data-stu-id="0c86e-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0c86e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="0c86e-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c86e-116">屬性</span><span class="sxs-lookup"><span data-stu-id="0c86e-116">Attribute</span></span></th>
<th><span data-ttu-id="0c86e-117">描述</span><span class="sxs-lookup"><span data-stu-id="0c86e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c86e-118">formatAs</span><span class="sxs-lookup"><span data-stu-id="0c86e-118">formatAs</span></span></td>
<td><span data-ttu-id="0c86e-119">公用。</span><span class="sxs-lookup"><span data-stu-id="0c86e-119">Public.</span></span> <span data-ttu-id="0c86e-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0c86e-120">Optional.</span></span> <span data-ttu-id="0c86e-121">預設值為 &quot; [一般] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="0c86e-121">Default is &quot;General&quot;.</span></span> <span data-ttu-id="0c86e-122">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="0c86e-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0c86e-123">值</span><span class="sxs-lookup"><span data-stu-id="0c86e-123">Value</span></span></th>
<th><span data-ttu-id="0c86e-124">意義</span><span class="sxs-lookup"><span data-stu-id="0c86e-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c86e-125">一般</span><span class="sxs-lookup"><span data-stu-id="0c86e-125">General</span></span></td>
<td><span data-ttu-id="0c86e-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="0c86e-126">Default.</span></span> <span data-ttu-id="0c86e-127">以未格式化的字串形式傳回值。</span><span class="sxs-lookup"><span data-stu-id="0c86e-127">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c86e-128">FileName</span><span class="sxs-lookup"><span data-stu-id="0c86e-128">FileName</span></span></td>
<td><span data-ttu-id="0c86e-129">將值格式化為檔案名。</span><span class="sxs-lookup"><span data-stu-id="0c86e-129">Formats the value as a file name.</span></span> <span data-ttu-id="0c86e-130">根據使用者設定隱藏延伸模組。</span><span class="sxs-lookup"><span data-stu-id="0c86e-130">Hides the extension according to user settings.</span></span> <span data-ttu-id="0c86e-131">要求屬性類型必須是字串。</span><span class="sxs-lookup"><span data-stu-id="0c86e-131">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c86e-132">FilePath</span><span class="sxs-lookup"><span data-stu-id="0c86e-132">FilePath</span></span></td>
<td><span data-ttu-id="0c86e-133">將值格式化為檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="0c86e-133">Formats the value as a file path.</span></span> <span data-ttu-id="0c86e-134">根據使用者設定隱藏延伸模組。</span><span class="sxs-lookup"><span data-stu-id="0c86e-134">Hides the extension according to user settings.</span></span> <span data-ttu-id="0c86e-135">要求屬性類型必須是字串。</span><span class="sxs-lookup"><span data-stu-id="0c86e-135">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c86e-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="0c86e-136">Hyperlink</span></span></td>
<td><span data-ttu-id="0c86e-137">將值格式化為超連結。</span><span class="sxs-lookup"><span data-stu-id="0c86e-137">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
