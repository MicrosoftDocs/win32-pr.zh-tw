---
description: 在 Windows 7 和更新版本中不支援。 指定要在查詢產生器中使用的控制項。
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974383"
---
# <a name="querycontrol"></a><span data-ttu-id="64eb9-104">queryControl</span><span class="sxs-lookup"><span data-stu-id="64eb9-104">queryControl</span></span>

<span data-ttu-id="64eb9-105">在 Windows 7 和更新版本中不支援。</span><span class="sxs-lookup"><span data-stu-id="64eb9-105">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="64eb9-106">指定要在查詢產生器中使用的控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-106">Specifies what control to use in the query builder.</span></span> <span data-ttu-id="64eb9-107">每個[displayInfo](./propdesc-schema-displayinfo.md)專案都只能有一個[queryControl]()元素。</span><span class="sxs-lookup"><span data-stu-id="64eb9-107">There should be only one [queryControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="64eb9-108">如果有多個元素，則會使用最後一個元素。</span><span class="sxs-lookup"><span data-stu-id="64eb9-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="64eb9-109">如果未提供任何 [queryControl]() 元素，則會將預設屬性設定套用至屬性描述。</span><span class="sxs-lookup"><span data-stu-id="64eb9-109">If no [queryControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="64eb9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="64eb9-110">Syntax</span></span>


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="64eb9-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="64eb9-111">Element Information</span></span>



| <span data-ttu-id="64eb9-112">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="64eb9-112">Parent Element</span></span>                                   | <span data-ttu-id="64eb9-113">子元素</span><span class="sxs-lookup"><span data-stu-id="64eb9-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="64eb9-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="64eb9-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="64eb9-115">無</span><span class="sxs-lookup"><span data-stu-id="64eb9-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="64eb9-116">屬性</span><span class="sxs-lookup"><span data-stu-id="64eb9-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64eb9-117">屬性</span><span class="sxs-lookup"><span data-stu-id="64eb9-117">Attribute</span></span></th>
<th><span data-ttu-id="64eb9-118">描述</span><span class="sxs-lookup"><span data-stu-id="64eb9-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64eb9-119">控制</span><span class="sxs-lookup"><span data-stu-id="64eb9-119">control</span></span></td>
<td><span data-ttu-id="64eb9-120">公用。</span><span class="sxs-lookup"><span data-stu-id="64eb9-120">Public.</span></span> <span data-ttu-id="64eb9-121">選擇性。</span><span class="sxs-lookup"><span data-stu-id="64eb9-121">Optional.</span></span> <span data-ttu-id="64eb9-122">預設值為預設值 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="64eb9-122">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="64eb9-123">以下是有效的值。</span><span class="sxs-lookup"><span data-stu-id="64eb9-123">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64eb9-124">值</span><span class="sxs-lookup"><span data-stu-id="64eb9-124">Value</span></span></th>
<th><span data-ttu-id="64eb9-125">意義</span><span class="sxs-lookup"><span data-stu-id="64eb9-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64eb9-126">預設</span><span class="sxs-lookup"><span data-stu-id="64eb9-126">Default</span></span></td>
<td><span data-ttu-id="64eb9-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="64eb9-127">Default.</span></span> <span data-ttu-id="64eb9-128">根據屬性使用預設控制項 <typeInfo type=&quot;&quot;> 。</span><span class="sxs-lookup"><span data-stu-id="64eb9-128">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="64eb9-129">預設類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="64eb9-129">The default types are listed below.</span></span> <span data-ttu-id="64eb9-130">任何其他類型都會導致使用 &quot; 文字 &quot; 控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-130">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="64eb9-131">ConditionType</span><span class="sxs-lookup"><span data-stu-id="64eb9-131">ConditionType</span></span></th>
<th><span data-ttu-id="64eb9-132">控制</span><span class="sxs-lookup"><span data-stu-id="64eb9-132">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64eb9-133">String</span><span class="sxs-lookup"><span data-stu-id="64eb9-133">String</span></span></td>
<td><span data-ttu-id="64eb9-134">Text</span><span class="sxs-lookup"><span data-stu-id="64eb9-134">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64eb9-135">字串 (多重值) </span><span class="sxs-lookup"><span data-stu-id="64eb9-135">String (multi-value)</span></span></td>
<td><span data-ttu-id="64eb9-136">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="64eb9-136">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64eb9-137">數位或大小</span><span class="sxs-lookup"><span data-stu-id="64eb9-137">Number or Size</span></span></td>
<td><span data-ttu-id="64eb9-138">NumericText</span><span class="sxs-lookup"><span data-stu-id="64eb9-138">NumericText</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64eb9-139"> (列舉) 的數目或大小</span><span class="sxs-lookup"><span data-stu-id="64eb9-139">Number or Size (enum)</span></span></td>
<td><span data-ttu-id="64eb9-140">List</span><span class="sxs-lookup"><span data-stu-id="64eb9-140">List</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64eb9-141">Datetime</span><span class="sxs-lookup"><span data-stu-id="64eb9-141">DateTime</span></span></td>
<td><span data-ttu-id="64eb9-142">Calendar</span><span class="sxs-lookup"><span data-stu-id="64eb9-142">Calendar</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64eb9-143">布林值</span><span class="sxs-lookup"><span data-stu-id="64eb9-143">Boolean</span></span></td>
<td><span data-ttu-id="64eb9-144">布林值</span><span class="sxs-lookup"><span data-stu-id="64eb9-144">Boolean</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64eb9-145">布林值</span><span class="sxs-lookup"><span data-stu-id="64eb9-145">Boolean</span></span></td>
<td><span data-ttu-id="64eb9-146">使用布林值控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-146">Uses the boolean control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64eb9-147">Calendar</span><span class="sxs-lookup"><span data-stu-id="64eb9-147">Calendar</span></span></td>
<td><span data-ttu-id="64eb9-148">使用下拉式月曆控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-148">Uses the dropdown calendar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64eb9-149">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="64eb9-149">CheckboxDropList</span></span></td>
<td><span data-ttu-id="64eb9-150">使用具有核取方塊的清單控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-150">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64eb9-151">DropList</span><span class="sxs-lookup"><span data-stu-id="64eb9-151">DropList</span></span></td>
<td><span data-ttu-id="64eb9-152">使用下拉式清單控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-152">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64eb9-153">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="64eb9-153">MultiValueText</span></span></td>
<td><span data-ttu-id="64eb9-154">使用多重值的文字編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-154">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64eb9-155">NumericText</span><span class="sxs-lookup"><span data-stu-id="64eb9-155">NumericText</span></span></td>
<td><span data-ttu-id="64eb9-156">使用數值文字編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-156">Uses the numeric text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64eb9-157">分級</span><span class="sxs-lookup"><span data-stu-id="64eb9-157">Rating</span></span></td>
<td><span data-ttu-id="64eb9-158">使用5顆星的評等控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-158">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64eb9-159">Text</span><span class="sxs-lookup"><span data-stu-id="64eb9-159">Text</span></span></td>
<td><span data-ttu-id="64eb9-160">使用文字編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="64eb9-160">Uses the text edit control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
