---
description: 包含在筆記本便箋中用於信紙的水平線格式資訊。
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: 水準元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690624"
---
# <a name="horizontal-element"></a><span data-ttu-id="38c17-103">水準元素</span><span class="sxs-lookup"><span data-stu-id="38c17-103">Horizontal Element</span></span>

<span data-ttu-id="38c17-104">包含在筆記本便箋中用於信紙的水平線格式資訊。</span><span class="sxs-lookup"><span data-stu-id="38c17-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="38c17-105">定義</span><span class="sxs-lookup"><span data-stu-id="38c17-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="38c17-106">父項目</span><span class="sxs-lookup"><span data-stu-id="38c17-106">Parent Elements</span></span>

[<span data-ttu-id="38c17-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="38c17-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="38c17-108">子元素</span><span class="sxs-lookup"><span data-stu-id="38c17-108">Child Elements</span></span>

<span data-ttu-id="38c17-109">無。</span><span class="sxs-lookup"><span data-stu-id="38c17-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="38c17-110">屬性</span><span class="sxs-lookup"><span data-stu-id="38c17-110">Attributes</span></span>



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
<th><span data-ttu-id="38c17-111">屬性</span><span class="sxs-lookup"><span data-stu-id="38c17-111">Attribute</span></span></th>
<th><span data-ttu-id="38c17-112">類型</span><span class="sxs-lookup"><span data-stu-id="38c17-112">Type</span></span></th>
<th><span data-ttu-id="38c17-113">必要</span><span class="sxs-lookup"><span data-stu-id="38c17-113">Required</span></span></th>
<th><span data-ttu-id="38c17-114">描述</span><span class="sxs-lookup"><span data-stu-id="38c17-114">Description</span></span></th>
<th><span data-ttu-id="38c17-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="38c17-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38c17-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="38c17-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="38c17-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="38c17-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="38c17-118">必要</span><span class="sxs-lookup"><span data-stu-id="38c17-118">Required</span></span></td>
<td><span data-ttu-id="38c17-119">指定要繪製的線條類型。</span><span class="sxs-lookup"><span data-stu-id="38c17-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="38c17-120">無</span><span class="sxs-lookup"><span data-stu-id="38c17-120">None</span></span></li>
<li><span data-ttu-id="38c17-121">實線</span><span class="sxs-lookup"><span data-stu-id="38c17-121">Solid</span></span></li>
<li><span data-ttu-id="38c17-122">虛線</span><span class="sxs-lookup"><span data-stu-id="38c17-122">Dash</span></span></li>
<li><span data-ttu-id="38c17-123">點</span><span class="sxs-lookup"><span data-stu-id="38c17-123">Dot</span></span></li>
<li><span data-ttu-id="38c17-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="38c17-124">DashDot</span></span></li>
<li><span data-ttu-id="38c17-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="38c17-125">DashDotDot</span></span></li>
<li><span data-ttu-id="38c17-126">Double</span><span class="sxs-lookup"><span data-stu-id="38c17-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38c17-127"><strong>色彩</strong></span><span class="sxs-lookup"><span data-stu-id="38c17-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="38c17-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="38c17-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="38c17-129">選擇性</span><span class="sxs-lookup"><span data-stu-id="38c17-129">Optional</span></span></td>
<td><span data-ttu-id="38c17-130">元素的色彩。</span><span class="sxs-lookup"><span data-stu-id="38c17-130">Color of the element.</span></span></td>
<td><span data-ttu-id="38c17-131">十六進位的 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="38c17-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="38c17-132">符合下列正則運算式： # [0-9a-南非-Z] {6} 。</span><span class="sxs-lookup"><span data-stu-id="38c17-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="38c17-133">例如，#4a79B5。</span><span class="sxs-lookup"><span data-stu-id="38c17-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38c17-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="38c17-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="38c17-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="38c17-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="38c17-136">選擇性</span><span class="sxs-lookup"><span data-stu-id="38c17-136">Optional</span></span></td>
<td><span data-ttu-id="38c17-137">元素之前的間距。</span><span class="sxs-lookup"><span data-stu-id="38c17-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="38c17-138">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="38c17-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38c17-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="38c17-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="38c17-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="38c17-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="38c17-141">選擇性</span><span class="sxs-lookup"><span data-stu-id="38c17-141">Optional</span></span></td>
<td><span data-ttu-id="38c17-142">此元素與周圍元素之間的間距。</span><span class="sxs-lookup"><span data-stu-id="38c17-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="38c17-143">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="38c17-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="38c17-144">項目資訊</span><span class="sxs-lookup"><span data-stu-id="38c17-144">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="38c17-145">項目類型</span><span class="sxs-lookup"><span data-stu-id="38c17-145">Element type</span></span> | [<span data-ttu-id="38c17-146">**HorizontalType complexType**</span><span class="sxs-lookup"><span data-stu-id="38c17-146">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="38c17-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="38c17-147">Namespace</span></span>    | <span data-ttu-id="38c17-148">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="38c17-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="38c17-149">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="38c17-149">Schema name</span></span>  | <span data-ttu-id="38c17-150">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="38c17-150">Journal Reader</span></span>                                                    |



 

 

 




