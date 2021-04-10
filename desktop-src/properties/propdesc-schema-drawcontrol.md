---
description: 指定只顯示內容時要使用的控制項。
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026520"
---
# <a name="drawcontrol"></a><span data-ttu-id="91f93-103">drawControl</span><span class="sxs-lookup"><span data-stu-id="91f93-103">drawControl</span></span>

<span data-ttu-id="91f93-104">指定只顯示內容時要使用的控制項。</span><span class="sxs-lookup"><span data-stu-id="91f93-104">Specifies what control to use when simply displaying the property.</span></span> <span data-ttu-id="91f93-105">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[drawControl]()元素。</span><span class="sxs-lookup"><span data-stu-id="91f93-105">There should be only one [drawControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="91f93-106">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="91f93-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="91f93-107">如果未提供任何 [drawControl]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="91f93-107">If no [drawControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="91f93-108">這種形式的控制項不允許編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="91f93-108">This form of the control does not allow for property editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="91f93-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="91f93-109">Syntax</span></span>


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="91f93-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="91f93-110">Element Information</span></span>



| <span data-ttu-id="91f93-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="91f93-111">Parent Element</span></span>                                   | <span data-ttu-id="91f93-112">子元素</span><span class="sxs-lookup"><span data-stu-id="91f93-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="91f93-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="91f93-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="91f93-114">無</span><span class="sxs-lookup"><span data-stu-id="91f93-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="91f93-115">屬性</span><span class="sxs-lookup"><span data-stu-id="91f93-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91f93-116">屬性</span><span class="sxs-lookup"><span data-stu-id="91f93-116">Attribute</span></span></th>
<th><span data-ttu-id="91f93-117">描述</span><span class="sxs-lookup"><span data-stu-id="91f93-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91f93-118">控制</span><span class="sxs-lookup"><span data-stu-id="91f93-118">control</span></span></td>
<td><span data-ttu-id="91f93-119">公用。</span><span class="sxs-lookup"><span data-stu-id="91f93-119">Public.</span></span> <span data-ttu-id="91f93-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="91f93-120">Optional.</span></span> <span data-ttu-id="91f93-121">預設值為預設值 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="91f93-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="91f93-122">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="91f93-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="91f93-123">值</span><span class="sxs-lookup"><span data-stu-id="91f93-123">Value</span></span></th>
<th><span data-ttu-id="91f93-124">意義</span><span class="sxs-lookup"><span data-stu-id="91f93-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91f93-125">預設</span><span class="sxs-lookup"><span data-stu-id="91f93-125">Default</span></span></td>
<td><span data-ttu-id="91f93-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="91f93-126">Default.</span></span> <span data-ttu-id="91f93-127">根據屬性使用預設控制項 <typeInfo type=&quot;&quot;> 。</span><span class="sxs-lookup"><span data-stu-id="91f93-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="91f93-128">預設類型為 &quot; 字串 &quot; (多重值) ，而且預設控制項為 &quot; MultiValueText &quot; 。</span><span class="sxs-lookup"><span data-stu-id="91f93-128">The default type is &quot;String&quot; (multi-value) and the default control is &quot;MultiValueText&quot;.</span></span> <span data-ttu-id="91f93-129">任何其他類型都會導致使用 &quot; StaticText &quot; 控制項。</span><span class="sxs-lookup"><span data-stu-id="91f93-129">Any other type results in using the &quot;StaticText&quot; control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91f93-130">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="91f93-130">MultiLineText</span></span></td>
<td><span data-ttu-id="91f93-131">使用多行文字控制項。</span><span class="sxs-lookup"><span data-stu-id="91f93-131">Uses the multi-line text control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91f93-132">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="91f93-132">MultiValueText</span></span></td>
<td><span data-ttu-id="91f93-133">使用多重值文字控制項。</span><span class="sxs-lookup"><span data-stu-id="91f93-133">Uses the multi-value text control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91f93-134">PercentBar</span><span class="sxs-lookup"><span data-stu-id="91f93-134">PercentBar</span></span></td>
<td><span data-ttu-id="91f93-135">使用百分比 bar 控制項。</span><span class="sxs-lookup"><span data-stu-id="91f93-135">Uses the percent bar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91f93-136">進度列</span><span class="sxs-lookup"><span data-stu-id="91f93-136">ProgressBar</span></span></td>
<td><span data-ttu-id="91f93-137">使用進度列控制項。</span><span class="sxs-lookup"><span data-stu-id="91f93-137">Uses the progress bar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91f93-138">分級</span><span class="sxs-lookup"><span data-stu-id="91f93-138">Rating</span></span></td>
<td><span data-ttu-id="91f93-139">使用5顆星的評等控制項。</span><span class="sxs-lookup"><span data-stu-id="91f93-139">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91f93-140">StaticText</span><span class="sxs-lookup"><span data-stu-id="91f93-140">StaticText</span></span></td>
<td><span data-ttu-id="91f93-141">使用 <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription：： FormatForDisplay</strong></a> 來顯示內容值。</span><span class="sxs-lookup"><span data-stu-id="91f93-141">Uses <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription::FormatForDisplay</strong></a> to display the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91f93-142">IconList</span><span class="sxs-lookup"><span data-stu-id="91f93-142">IconList</span></span></td>
<td><span data-ttu-id="91f93-143"><strong>Windows 7 和更新版本。</strong></span><span class="sxs-lookup"><span data-stu-id="91f93-143"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="91f93-144">圖示的列舉。</span><span class="sxs-lookup"><span data-stu-id="91f93-144">An enumeration of icons.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91f93-145">BooleanCheckMark</span><span class="sxs-lookup"><span data-stu-id="91f93-145">BooleanCheckMark</span></span></td>
<td><span data-ttu-id="91f93-146"><strong>Windows 7 和更新版本。</strong></span><span class="sxs-lookup"><span data-stu-id="91f93-146"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
