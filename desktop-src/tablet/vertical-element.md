---
description: 包含描述筆記本便箋所用信紙中線條垂直元件的資訊。 例如，當便箋具有格線時使用。
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: 垂直元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42565e6f2828c4ef27d1b28830502303a03e6f13
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432120"
---
# <a name="vertical-element"></a><span data-ttu-id="33baa-104">垂直元素</span><span class="sxs-lookup"><span data-stu-id="33baa-104">Vertical Element</span></span>

<span data-ttu-id="33baa-105">包含描述筆記本便箋所用信紙中線條垂直元件的資訊。</span><span class="sxs-lookup"><span data-stu-id="33baa-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="33baa-106">例如，當便箋具有格線時使用。</span><span class="sxs-lookup"><span data-stu-id="33baa-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="33baa-107">定義</span><span class="sxs-lookup"><span data-stu-id="33baa-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="33baa-108">父項目</span><span class="sxs-lookup"><span data-stu-id="33baa-108">Parent Elements</span></span>

[<span data-ttu-id="33baa-109">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="33baa-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="33baa-110">子元素</span><span class="sxs-lookup"><span data-stu-id="33baa-110">Child Elements</span></span>

<span data-ttu-id="33baa-111">無。</span><span class="sxs-lookup"><span data-stu-id="33baa-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="33baa-112">屬性</span><span class="sxs-lookup"><span data-stu-id="33baa-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33baa-113">屬性</span><span class="sxs-lookup"><span data-stu-id="33baa-113">Attribute</span></span></th>
<th><span data-ttu-id="33baa-114">類型</span><span class="sxs-lookup"><span data-stu-id="33baa-114">Type</span></span></th>
<th><span data-ttu-id="33baa-115">必要</span><span class="sxs-lookup"><span data-stu-id="33baa-115">Required</span></span></th>
<th><span data-ttu-id="33baa-116">描述</span><span class="sxs-lookup"><span data-stu-id="33baa-116">Description</span></span></th>
<th><span data-ttu-id="33baa-117">可能的值</span><span class="sxs-lookup"><span data-stu-id="33baa-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33baa-118"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="33baa-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="33baa-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="33baa-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="33baa-120">必要</span><span class="sxs-lookup"><span data-stu-id="33baa-120">Required</span></span></td>
<td><span data-ttu-id="33baa-121">指定要繪製的線條類型。</span><span class="sxs-lookup"><span data-stu-id="33baa-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="33baa-122">None</span><span class="sxs-lookup"><span data-stu-id="33baa-122">None</span></span></li>
<li><span data-ttu-id="33baa-123">實線</span><span class="sxs-lookup"><span data-stu-id="33baa-123">Solid</span></span></li>
<li><span data-ttu-id="33baa-124">虛線</span><span class="sxs-lookup"><span data-stu-id="33baa-124">Dash</span></span></li>
<li><span data-ttu-id="33baa-125">點</span><span class="sxs-lookup"><span data-stu-id="33baa-125">Dot</span></span></li>
<li><span data-ttu-id="33baa-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="33baa-126">DashDot</span></span></li>
<li><span data-ttu-id="33baa-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="33baa-127">DashDotDot</span></span></li>
<li><span data-ttu-id="33baa-128">Double</span><span class="sxs-lookup"><span data-stu-id="33baa-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33baa-129"><strong>色彩</strong></span><span class="sxs-lookup"><span data-stu-id="33baa-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="33baa-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="33baa-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="33baa-131">選用</span><span class="sxs-lookup"><span data-stu-id="33baa-131">Optional</span></span></td>
<td><span data-ttu-id="33baa-132">元素的色彩。</span><span class="sxs-lookup"><span data-stu-id="33baa-132">Color of the element.</span></span></td>
<td><span data-ttu-id="33baa-133">十六進位的 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="33baa-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="33baa-134">符合下列正則運算式： # [0-9a-南非-Z] {6} 。</span><span class="sxs-lookup"><span data-stu-id="33baa-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="33baa-135">例如，#4a79B5。</span><span class="sxs-lookup"><span data-stu-id="33baa-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33baa-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="33baa-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="33baa-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="33baa-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="33baa-138">選用</span><span class="sxs-lookup"><span data-stu-id="33baa-138">Optional</span></span></td>
<td><span data-ttu-id="33baa-139">元素之前的間距。</span><span class="sxs-lookup"><span data-stu-id="33baa-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="33baa-140">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="33baa-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33baa-141"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="33baa-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="33baa-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="33baa-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="33baa-143">選用</span><span class="sxs-lookup"><span data-stu-id="33baa-143">Optional</span></span></td>
<td><span data-ttu-id="33baa-144">此元素與周圍元素之間的間距。</span><span class="sxs-lookup"><span data-stu-id="33baa-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="33baa-145">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="33baa-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="33baa-146">項目資訊</span><span class="sxs-lookup"><span data-stu-id="33baa-146">Element Information</span></span>



|  <span data-ttu-id="33baa-147">元素</span><span class="sxs-lookup"><span data-stu-id="33baa-147">Element</span></span>     | <span data-ttu-id="33baa-148">值</span><span class="sxs-lookup"><span data-stu-id="33baa-148">Value</span></span>                                                         |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="33baa-149">項目類型</span><span class="sxs-lookup"><span data-stu-id="33baa-149">Element type</span></span> | <span data-ttu-id="33baa-150">[**VerticalType**](verticaltype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="33baa-150">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="33baa-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="33baa-151">Namespace</span></span>    | <span data-ttu-id="33baa-152">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="33baa-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="33baa-153">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="33baa-153">Schema name</span></span>  | <span data-ttu-id="33baa-154">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="33baa-154">Journal Reader</span></span>                                                |



 

 

 




