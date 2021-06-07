---
description: 定義在頁面上繪製的邊界線。
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547177a10fc3724f3b9bf3dde65f857d03f0f2a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432130"
---
# <a name="margin-element"></a><span data-ttu-id="a9bb3-103">Margin 元素</span><span class="sxs-lookup"><span data-stu-id="a9bb3-103">Margin Element</span></span>

<span data-ttu-id="a9bb3-104">定義在頁面上繪製的邊界線。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="a9bb3-105">定義</span><span class="sxs-lookup"><span data-stu-id="a9bb3-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="a9bb3-106">父項目</span><span class="sxs-lookup"><span data-stu-id="a9bb3-106">Parent Elements</span></span>

<span data-ttu-id="a9bb3-107">無。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a9bb3-108">子元素</span><span class="sxs-lookup"><span data-stu-id="a9bb3-108">Child Elements</span></span>

<span data-ttu-id="a9bb3-109">沒有。。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="a9bb3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a9bb3-110">Attributes</span></span>



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
<th><span data-ttu-id="a9bb3-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a9bb3-111">Attribute</span></span></th>
<th><span data-ttu-id="a9bb3-112">類型</span><span class="sxs-lookup"><span data-stu-id="a9bb3-112">Type</span></span></th>
<th><span data-ttu-id="a9bb3-113">必要</span><span class="sxs-lookup"><span data-stu-id="a9bb3-113">Required</span></span></th>
<th><span data-ttu-id="a9bb3-114">描述</span><span class="sxs-lookup"><span data-stu-id="a9bb3-114">Description</span></span></th>
<th><span data-ttu-id="a9bb3-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="a9bb3-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9bb3-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="a9bb3-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="a9bb3-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="a9bb3-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="a9bb3-118">必要</span><span class="sxs-lookup"><span data-stu-id="a9bb3-118">Required</span></span></td>
<td><span data-ttu-id="a9bb3-119">指定要繪製的線條類型。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="a9bb3-120">None</span><span class="sxs-lookup"><span data-stu-id="a9bb3-120">None</span></span></li>
<li><span data-ttu-id="a9bb3-121">實線</span><span class="sxs-lookup"><span data-stu-id="a9bb3-121">Solid</span></span></li>
<li><span data-ttu-id="a9bb3-122">虛線</span><span class="sxs-lookup"><span data-stu-id="a9bb3-122">Dash</span></span></li>
<li><span data-ttu-id="a9bb3-123">點</span><span class="sxs-lookup"><span data-stu-id="a9bb3-123">Dot</span></span></li>
<li><span data-ttu-id="a9bb3-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="a9bb3-124">DashDot</span></span></li>
<li><span data-ttu-id="a9bb3-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="a9bb3-125">DashDotDot</span></span></li>
<li><span data-ttu-id="a9bb3-126">Double</span><span class="sxs-lookup"><span data-stu-id="a9bb3-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9bb3-127"><strong>色彩</strong></span><span class="sxs-lookup"><span data-stu-id="a9bb3-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="a9bb3-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="a9bb3-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="a9bb3-129">選用</span><span class="sxs-lookup"><span data-stu-id="a9bb3-129">Optional</span></span></td>
<td><span data-ttu-id="a9bb3-130">元素的色彩。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-130">Color of the element.</span></span></td>
<td><span data-ttu-id="a9bb3-131">十六進位的 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="a9bb3-132">符合下列正則運算式： # [0-9a-南非-Z] {6} 。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="a9bb3-133">例如，#4a79B5。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9bb3-134"><strong>類型</strong></span><span class="sxs-lookup"><span data-stu-id="a9bb3-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="a9bb3-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="a9bb3-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="a9bb3-136">選用</span><span class="sxs-lookup"><span data-stu-id="a9bb3-136">Optional</span></span></td>
<td><span data-ttu-id="a9bb3-137">表示左邊界或右邊界。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="a9bb3-138">Left</span><span class="sxs-lookup"><span data-stu-id="a9bb3-138">Left</span></span></li>
<li><span data-ttu-id="a9bb3-139">Right</span><span class="sxs-lookup"><span data-stu-id="a9bb3-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9bb3-140"><strong>間距</strong></span><span class="sxs-lookup"><span data-stu-id="a9bb3-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="a9bb3-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="a9bb3-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="a9bb3-142">選用</span><span class="sxs-lookup"><span data-stu-id="a9bb3-142">Optional</span></span></td>
<td><span data-ttu-id="a9bb3-143">頁面邊緣和邊界之間的間距。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="a9bb3-144">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="a9bb3-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="a9bb3-145">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a9bb3-145">Element Information</span></span>



|  <span data-ttu-id="a9bb3-146">元素</span><span class="sxs-lookup"><span data-stu-id="a9bb3-146">Element</span></span>     | <span data-ttu-id="a9bb3-147">值</span><span class="sxs-lookup"><span data-stu-id="a9bb3-147">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="a9bb3-148">項目類型</span><span class="sxs-lookup"><span data-stu-id="a9bb3-148">Element type</span></span> | <span data-ttu-id="a9bb3-149">[**MarginType**](margintype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="a9bb3-149">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a9bb3-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="a9bb3-150">Namespace</span></span>    | <span data-ttu-id="a9bb3-151">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="a9bb3-151">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="a9bb3-152">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="a9bb3-152">Schema name</span></span>  | <span data-ttu-id="a9bb3-153">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="a9bb3-153">Journal Reader</span></span>                                            |



 

 

 




