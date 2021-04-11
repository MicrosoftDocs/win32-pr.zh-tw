---
description: 定義在頁面上繪製的邊界線。
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195105"
---
# <a name="margin-element"></a><span data-ttu-id="876d1-103">Margin 元素</span><span class="sxs-lookup"><span data-stu-id="876d1-103">Margin Element</span></span>

<span data-ttu-id="876d1-104">定義在頁面上繪製的邊界線。</span><span class="sxs-lookup"><span data-stu-id="876d1-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="876d1-105">定義</span><span class="sxs-lookup"><span data-stu-id="876d1-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="876d1-106">父項目</span><span class="sxs-lookup"><span data-stu-id="876d1-106">Parent Elements</span></span>

<span data-ttu-id="876d1-107">無。</span><span class="sxs-lookup"><span data-stu-id="876d1-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="876d1-108">子元素</span><span class="sxs-lookup"><span data-stu-id="876d1-108">Child Elements</span></span>

<span data-ttu-id="876d1-109">沒有。。</span><span class="sxs-lookup"><span data-stu-id="876d1-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="876d1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="876d1-110">Attributes</span></span>



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
<th><span data-ttu-id="876d1-111">屬性</span><span class="sxs-lookup"><span data-stu-id="876d1-111">Attribute</span></span></th>
<th><span data-ttu-id="876d1-112">類型</span><span class="sxs-lookup"><span data-stu-id="876d1-112">Type</span></span></th>
<th><span data-ttu-id="876d1-113">必要</span><span class="sxs-lookup"><span data-stu-id="876d1-113">Required</span></span></th>
<th><span data-ttu-id="876d1-114">描述</span><span class="sxs-lookup"><span data-stu-id="876d1-114">Description</span></span></th>
<th><span data-ttu-id="876d1-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="876d1-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="876d1-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="876d1-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="876d1-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="876d1-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="876d1-118">必要</span><span class="sxs-lookup"><span data-stu-id="876d1-118">Required</span></span></td>
<td><span data-ttu-id="876d1-119">指定要繪製的線條類型。</span><span class="sxs-lookup"><span data-stu-id="876d1-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="876d1-120">無</span><span class="sxs-lookup"><span data-stu-id="876d1-120">None</span></span></li>
<li><span data-ttu-id="876d1-121">實線</span><span class="sxs-lookup"><span data-stu-id="876d1-121">Solid</span></span></li>
<li><span data-ttu-id="876d1-122">虛線</span><span class="sxs-lookup"><span data-stu-id="876d1-122">Dash</span></span></li>
<li><span data-ttu-id="876d1-123">點</span><span class="sxs-lookup"><span data-stu-id="876d1-123">Dot</span></span></li>
<li><span data-ttu-id="876d1-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="876d1-124">DashDot</span></span></li>
<li><span data-ttu-id="876d1-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="876d1-125">DashDotDot</span></span></li>
<li><span data-ttu-id="876d1-126">Double</span><span class="sxs-lookup"><span data-stu-id="876d1-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="876d1-127"><strong>色彩</strong></span><span class="sxs-lookup"><span data-stu-id="876d1-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="876d1-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="876d1-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="876d1-129">選擇性</span><span class="sxs-lookup"><span data-stu-id="876d1-129">Optional</span></span></td>
<td><span data-ttu-id="876d1-130">元素的色彩。</span><span class="sxs-lookup"><span data-stu-id="876d1-130">Color of the element.</span></span></td>
<td><span data-ttu-id="876d1-131">十六進位的 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="876d1-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="876d1-132">符合下列正則運算式： # [0-9a-南非-Z] {6} 。</span><span class="sxs-lookup"><span data-stu-id="876d1-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="876d1-133">例如，#4a79B5。</span><span class="sxs-lookup"><span data-stu-id="876d1-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="876d1-134"><strong>型別</strong></span><span class="sxs-lookup"><span data-stu-id="876d1-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="876d1-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="876d1-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="876d1-136">選擇性</span><span class="sxs-lookup"><span data-stu-id="876d1-136">Optional</span></span></td>
<td><span data-ttu-id="876d1-137">表示左邊界或右邊界。</span><span class="sxs-lookup"><span data-stu-id="876d1-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="876d1-138">Left</span><span class="sxs-lookup"><span data-stu-id="876d1-138">Left</span></span></li>
<li><span data-ttu-id="876d1-139">Right</span><span class="sxs-lookup"><span data-stu-id="876d1-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="876d1-140"><strong>間距</strong></span><span class="sxs-lookup"><span data-stu-id="876d1-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="876d1-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="876d1-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="876d1-142">選擇性</span><span class="sxs-lookup"><span data-stu-id="876d1-142">Optional</span></span></td>
<td><span data-ttu-id="876d1-143">頁面邊緣和邊界之間的間距。</span><span class="sxs-lookup"><span data-stu-id="876d1-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="876d1-144">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="876d1-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="876d1-145">項目資訊</span><span class="sxs-lookup"><span data-stu-id="876d1-145">Element Information</span></span>



|              |                                                           |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="876d1-146">項目類型</span><span class="sxs-lookup"><span data-stu-id="876d1-146">Element type</span></span> | <span data-ttu-id="876d1-147">[**MarginType**](margintype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="876d1-147">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="876d1-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="876d1-148">Namespace</span></span>    | <span data-ttu-id="876d1-149">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="876d1-149">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="876d1-150">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="876d1-150">Schema name</span></span>  | <span data-ttu-id="876d1-151">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="876d1-151">Journal Reader</span></span>                                            |



 

 

 




