---
description: 包含筆記本便箋的標題資訊。
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Title 項目
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432220"
---
# <a name="title-element"></a><span data-ttu-id="bb96c-103">Title 項目</span><span class="sxs-lookup"><span data-stu-id="bb96c-103">Title Element</span></span>

<span data-ttu-id="bb96c-104">包含筆記本便箋的標題資訊。</span><span class="sxs-lookup"><span data-stu-id="bb96c-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="bb96c-105">定義</span><span class="sxs-lookup"><span data-stu-id="bb96c-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="bb96c-106">父項目</span><span class="sxs-lookup"><span data-stu-id="bb96c-106">Parent Elements</span></span>

[<span data-ttu-id="bb96c-107">**信箋**</span><span class="sxs-lookup"><span data-stu-id="bb96c-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="bb96c-108">子元素</span><span class="sxs-lookup"><span data-stu-id="bb96c-108">Child Elements</span></span>

[<span data-ttu-id="bb96c-109">**TitleArea**</span><span class="sxs-lookup"><span data-stu-id="bb96c-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="bb96c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bb96c-110">Attributes</span></span>



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
<th><span data-ttu-id="bb96c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bb96c-111">Attribute</span></span></th>
<th><span data-ttu-id="bb96c-112">類型</span><span class="sxs-lookup"><span data-stu-id="bb96c-112">Type</span></span></th>
<th><span data-ttu-id="bb96c-113">必要</span><span class="sxs-lookup"><span data-stu-id="bb96c-113">Required</span></span></th>
<th><span data-ttu-id="bb96c-114">描述</span><span class="sxs-lookup"><span data-stu-id="bb96c-114">Description</span></span></th>
<th><span data-ttu-id="bb96c-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="bb96c-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb96c-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="bb96c-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="bb96c-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="bb96c-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="bb96c-118">必要</span><span class="sxs-lookup"><span data-stu-id="bb96c-118">Required</span></span></td>
<td><span data-ttu-id="bb96c-119">指定附注標題周圍的框線類型。</span><span class="sxs-lookup"><span data-stu-id="bb96c-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="bb96c-120">None</span><span class="sxs-lookup"><span data-stu-id="bb96c-120">None</span></span></li>
<li><span data-ttu-id="bb96c-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="bb96c-121">SolidSquare</span></span></li>
<li><span data-ttu-id="bb96c-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="bb96c-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="bb96c-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="bb96c-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="bb96c-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="bb96c-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="bb96c-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="bb96c-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb96c-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="bb96c-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="bb96c-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="bb96c-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="bb96c-128">必要</span><span class="sxs-lookup"><span data-stu-id="bb96c-128">Required</span></span></td>
<td><span data-ttu-id="bb96c-129">定義標題是否包含日期。</span><span class="sxs-lookup"><span data-stu-id="bb96c-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="bb96c-130">None</span><span class="sxs-lookup"><span data-stu-id="bb96c-130">None</span></span></li>
<li><span data-ttu-id="bb96c-131">Short</span><span class="sxs-lookup"><span data-stu-id="bb96c-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb96c-132"><strong>色彩</strong></span><span class="sxs-lookup"><span data-stu-id="bb96c-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="bb96c-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb96c-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="bb96c-134">選用</span><span class="sxs-lookup"><span data-stu-id="bb96c-134">Optional</span></span></td>
<td><span data-ttu-id="bb96c-135">指定背景的色彩。</span><span class="sxs-lookup"><span data-stu-id="bb96c-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="bb96c-136">請參閱 <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="bb96c-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="bb96c-137">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bb96c-137">Element Information</span></span>



| <span data-ttu-id="bb96c-138">元素</span><span class="sxs-lookup"><span data-stu-id="bb96c-138">Element</span></span>      | <span data-ttu-id="bb96c-139">值</span><span class="sxs-lookup"><span data-stu-id="bb96c-139">Value</span></span>                                                   |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="bb96c-140">項目類型</span><span class="sxs-lookup"><span data-stu-id="bb96c-140">Element type</span></span> | <span data-ttu-id="bb96c-141">[**TitleType**](titletype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="bb96c-141">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="bb96c-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="bb96c-142">Namespace</span></span>    | <span data-ttu-id="bb96c-143">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="bb96c-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="bb96c-144">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="bb96c-144">Schema name</span></span>  | <span data-ttu-id="bb96c-145">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="bb96c-145">Journal Reader</span></span>                                          |



 

 

 



