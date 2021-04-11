---
description: 指定編輯屬性時所要使用的控制項。
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944328"
---
# <a name="editcontrol"></a><span data-ttu-id="512ef-103">editControl</span><span class="sxs-lookup"><span data-stu-id="512ef-103">editControl</span></span>

<span data-ttu-id="512ef-104">指定編輯屬性時所要使用的控制項。</span><span class="sxs-lookup"><span data-stu-id="512ef-104">Specifies what control to use when editing the property.</span></span> <span data-ttu-id="512ef-105">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[editControl]()元素。</span><span class="sxs-lookup"><span data-stu-id="512ef-105">There should be only one [editControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="512ef-106">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="512ef-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="512ef-107">如果未提供任何 [editControl]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="512ef-107">If no [editControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="512ef-108">如果為 <typeInfo isInnate="true"> ，則會忽略這個元素，因為無法編輯固有屬性。</span><span class="sxs-lookup"><span data-stu-id="512ef-108">If <typeInfo isInnate="true">, this element is ignored because an innate property cannot be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="512ef-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="512ef-109">Syntax</span></span>


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="512ef-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="512ef-110">Element Information</span></span>



| <span data-ttu-id="512ef-111">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="512ef-111">Parent Element</span></span>                                   | <span data-ttu-id="512ef-112">子元素</span><span class="sxs-lookup"><span data-stu-id="512ef-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="512ef-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="512ef-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="512ef-114">無</span><span class="sxs-lookup"><span data-stu-id="512ef-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="512ef-115">屬性</span><span class="sxs-lookup"><span data-stu-id="512ef-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="512ef-116">屬性</span><span class="sxs-lookup"><span data-stu-id="512ef-116">Attribute</span></span></th>
<th><span data-ttu-id="512ef-117">描述</span><span class="sxs-lookup"><span data-stu-id="512ef-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="512ef-118">控制</span><span class="sxs-lookup"><span data-stu-id="512ef-118">control</span></span></td>
<td><span data-ttu-id="512ef-119">公用。</span><span class="sxs-lookup"><span data-stu-id="512ef-119">Public.</span></span> <span data-ttu-id="512ef-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="512ef-120">Optional.</span></span> <span data-ttu-id="512ef-121">預設值為預設值 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="512ef-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="512ef-122">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="512ef-122">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="512ef-123">值</span><span class="sxs-lookup"><span data-stu-id="512ef-123">Value</span></span></th>
<th><span data-ttu-id="512ef-124">意義</span><span class="sxs-lookup"><span data-stu-id="512ef-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="512ef-125">預設</span><span class="sxs-lookup"><span data-stu-id="512ef-125">Default</span></span></td>
<td><span data-ttu-id="512ef-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="512ef-126">Default.</span></span> <span data-ttu-id="512ef-127">根據屬性使用預設控制項 <typeInfo type=&quot;&quot;> 。</span><span class="sxs-lookup"><span data-stu-id="512ef-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="512ef-128">預設類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="512ef-128">The default types are listed below.</span></span> <span data-ttu-id="512ef-129">任何其他類型都會導致使用 &quot; 文字 &quot; 控制項。</span><span class="sxs-lookup"><span data-stu-id="512ef-129">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="512ef-130">類型</span><span class="sxs-lookup"><span data-stu-id="512ef-130">Type</span></span></th>
<th><span data-ttu-id="512ef-131">控制</span><span class="sxs-lookup"><span data-stu-id="512ef-131">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="512ef-132">String</span><span class="sxs-lookup"><span data-stu-id="512ef-132">String</span></span></td>
<td><span data-ttu-id="512ef-133">Text</span><span class="sxs-lookup"><span data-stu-id="512ef-133">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="512ef-134">字串 (多重值) </span><span class="sxs-lookup"><span data-stu-id="512ef-134">String (multi-value)</span></span></td>
<td><span data-ttu-id="512ef-135">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="512ef-135">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="512ef-136">Datetime</span><span class="sxs-lookup"><span data-stu-id="512ef-136">DateTime</span></span></td>
<td><span data-ttu-id="512ef-137">Calendar</span><span class="sxs-lookup"><span data-stu-id="512ef-137">Calendar</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="512ef-138">Calendar</span><span class="sxs-lookup"><span data-stu-id="512ef-138">Calendar</span></span></td>
<td><span data-ttu-id="512ef-139">使用行事曆控制項。</span><span class="sxs-lookup"><span data-stu-id="512ef-139">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="512ef-140">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="512ef-140">CheckboxDropList</span></span></td>
<td><span data-ttu-id="512ef-141">使用具有核取方塊的清單控制項。</span><span class="sxs-lookup"><span data-stu-id="512ef-141">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="512ef-142">DropList</span><span class="sxs-lookup"><span data-stu-id="512ef-142">DropList</span></span></td>
<td><span data-ttu-id="512ef-143">使用下拉式清單控制項。</span><span class="sxs-lookup"><span data-stu-id="512ef-143">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="512ef-144">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="512ef-144">MultiLineText</span></span></td>
<td><span data-ttu-id="512ef-145">使用多行文字編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="512ef-145">Uses the multi-line text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="512ef-146">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="512ef-146">MultiValueText</span></span></td>
<td><span data-ttu-id="512ef-147">使用多重值的文字編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="512ef-147">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="512ef-148">分級</span><span class="sxs-lookup"><span data-stu-id="512ef-148">Rating</span></span></td>
<td><span data-ttu-id="512ef-149">使用5顆星的評等控制項。</span><span class="sxs-lookup"><span data-stu-id="512ef-149">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="512ef-150">Text</span><span class="sxs-lookup"><span data-stu-id="512ef-150">Text</span></span></td>
<td><span data-ttu-id="512ef-151">使用文字編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="512ef-151">Uses the text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="512ef-152">IconList</span><span class="sxs-lookup"><span data-stu-id="512ef-152">IconList</span></span></td>
<td><span data-ttu-id="512ef-153"><strong>Windows 7 和更新版本。</strong></span><span class="sxs-lookup"><span data-stu-id="512ef-153"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
