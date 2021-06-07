---
description: 包含在筆記本便箋中用於信紙的水平線格式資訊。
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: 水準元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432372"
---
# <a name="horizontal-element"></a><span data-ttu-id="43185-103">水準元素</span><span class="sxs-lookup"><span data-stu-id="43185-103">Horizontal Element</span></span>

<span data-ttu-id="43185-104">包含在筆記本便箋中用於信紙的水平線格式資訊。</span><span class="sxs-lookup"><span data-stu-id="43185-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="43185-105">定義</span><span class="sxs-lookup"><span data-stu-id="43185-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="43185-106">父項目</span><span class="sxs-lookup"><span data-stu-id="43185-106">Parent Elements</span></span>

[<span data-ttu-id="43185-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="43185-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="43185-108">子元素</span><span class="sxs-lookup"><span data-stu-id="43185-108">Child Elements</span></span>

<span data-ttu-id="43185-109">無。</span><span class="sxs-lookup"><span data-stu-id="43185-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="43185-110">屬性</span><span class="sxs-lookup"><span data-stu-id="43185-110">Attributes</span></span>



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
<th><span data-ttu-id="43185-111">屬性</span><span class="sxs-lookup"><span data-stu-id="43185-111">Attribute</span></span></th>
<th><span data-ttu-id="43185-112">類型</span><span class="sxs-lookup"><span data-stu-id="43185-112">Type</span></span></th>
<th><span data-ttu-id="43185-113">必要</span><span class="sxs-lookup"><span data-stu-id="43185-113">Required</span></span></th>
<th><span data-ttu-id="43185-114">描述</span><span class="sxs-lookup"><span data-stu-id="43185-114">Description</span></span></th>
<th><span data-ttu-id="43185-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="43185-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43185-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="43185-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="43185-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="43185-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="43185-118">必要</span><span class="sxs-lookup"><span data-stu-id="43185-118">Required</span></span></td>
<td><span data-ttu-id="43185-119">指定要繪製的線條類型。</span><span class="sxs-lookup"><span data-stu-id="43185-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="43185-120">None</span><span class="sxs-lookup"><span data-stu-id="43185-120">None</span></span></li>
<li><span data-ttu-id="43185-121">實線</span><span class="sxs-lookup"><span data-stu-id="43185-121">Solid</span></span></li>
<li><span data-ttu-id="43185-122">虛線</span><span class="sxs-lookup"><span data-stu-id="43185-122">Dash</span></span></li>
<li><span data-ttu-id="43185-123">點</span><span class="sxs-lookup"><span data-stu-id="43185-123">Dot</span></span></li>
<li><span data-ttu-id="43185-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="43185-124">DashDot</span></span></li>
<li><span data-ttu-id="43185-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="43185-125">DashDotDot</span></span></li>
<li><span data-ttu-id="43185-126">Double</span><span class="sxs-lookup"><span data-stu-id="43185-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43185-127"><strong>色彩</strong></span><span class="sxs-lookup"><span data-stu-id="43185-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="43185-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="43185-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="43185-129">選用</span><span class="sxs-lookup"><span data-stu-id="43185-129">Optional</span></span></td>
<td><span data-ttu-id="43185-130">元素的色彩。</span><span class="sxs-lookup"><span data-stu-id="43185-130">Color of the element.</span></span></td>
<td><span data-ttu-id="43185-131">十六進位的 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="43185-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="43185-132">符合下列正則運算式： # [0-9a-南非-Z] {6} 。</span><span class="sxs-lookup"><span data-stu-id="43185-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="43185-133">例如，#4a79B5。</span><span class="sxs-lookup"><span data-stu-id="43185-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43185-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="43185-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="43185-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="43185-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="43185-136">選用</span><span class="sxs-lookup"><span data-stu-id="43185-136">Optional</span></span></td>
<td><span data-ttu-id="43185-137">元素之前的間距。</span><span class="sxs-lookup"><span data-stu-id="43185-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="43185-138">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="43185-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43185-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="43185-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="43185-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="43185-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="43185-141">選用</span><span class="sxs-lookup"><span data-stu-id="43185-141">Optional</span></span></td>
<td><span data-ttu-id="43185-142">此元素與周圍元素之間的間距。</span><span class="sxs-lookup"><span data-stu-id="43185-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="43185-143">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="43185-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="43185-144">項目資訊</span><span class="sxs-lookup"><span data-stu-id="43185-144">Element Information</span></span>



|  <span data-ttu-id="43185-145">元素</span><span class="sxs-lookup"><span data-stu-id="43185-145">Element</span></span>     | <span data-ttu-id="43185-146">值</span><span class="sxs-lookup"><span data-stu-id="43185-146">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="43185-147">項目類型</span><span class="sxs-lookup"><span data-stu-id="43185-147">Element type</span></span> | [<span data-ttu-id="43185-148">**HorizontalType complexType**</span><span class="sxs-lookup"><span data-stu-id="43185-148">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="43185-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="43185-149">Namespace</span></span>    | <span data-ttu-id="43185-150">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="43185-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="43185-151">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="43185-151">Schema name</span></span>  | <span data-ttu-id="43185-152">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="43185-152">Journal Reader</span></span>                                                    |



 

 

 




