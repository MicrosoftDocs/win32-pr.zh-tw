---
description: 包含筆記本便箋的標題資訊。
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Title 項目
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981214"
---
# <a name="title-element"></a><span data-ttu-id="ac1c0-103">Title 項目</span><span class="sxs-lookup"><span data-stu-id="ac1c0-103">Title Element</span></span>

<span data-ttu-id="ac1c0-104">包含筆記本便箋的標題資訊。</span><span class="sxs-lookup"><span data-stu-id="ac1c0-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="ac1c0-105">定義</span><span class="sxs-lookup"><span data-stu-id="ac1c0-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="ac1c0-106">父項目</span><span class="sxs-lookup"><span data-stu-id="ac1c0-106">Parent Elements</span></span>

[<span data-ttu-id="ac1c0-107">**信箋**</span><span class="sxs-lookup"><span data-stu-id="ac1c0-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="ac1c0-108">子元素</span><span class="sxs-lookup"><span data-stu-id="ac1c0-108">Child Elements</span></span>

[<span data-ttu-id="ac1c0-109">**TitleArea**</span><span class="sxs-lookup"><span data-stu-id="ac1c0-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="ac1c0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ac1c0-110">Attributes</span></span>



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
<th><span data-ttu-id="ac1c0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ac1c0-111">Attribute</span></span></th>
<th><span data-ttu-id="ac1c0-112">類型</span><span class="sxs-lookup"><span data-stu-id="ac1c0-112">Type</span></span></th>
<th><span data-ttu-id="ac1c0-113">必要</span><span class="sxs-lookup"><span data-stu-id="ac1c0-113">Required</span></span></th>
<th><span data-ttu-id="ac1c0-114">描述</span><span class="sxs-lookup"><span data-stu-id="ac1c0-114">Description</span></span></th>
<th><span data-ttu-id="ac1c0-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="ac1c0-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac1c0-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="ac1c0-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="ac1c0-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="ac1c0-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="ac1c0-118">必要</span><span class="sxs-lookup"><span data-stu-id="ac1c0-118">Required</span></span></td>
<td><span data-ttu-id="ac1c0-119">指定附注標題周圍的框線類型。</span><span class="sxs-lookup"><span data-stu-id="ac1c0-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="ac1c0-120">無</span><span class="sxs-lookup"><span data-stu-id="ac1c0-120">None</span></span></li>
<li><span data-ttu-id="ac1c0-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="ac1c0-121">SolidSquare</span></span></li>
<li><span data-ttu-id="ac1c0-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="ac1c0-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="ac1c0-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="ac1c0-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="ac1c0-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="ac1c0-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="ac1c0-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="ac1c0-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac1c0-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="ac1c0-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="ac1c0-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="ac1c0-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="ac1c0-128">必要</span><span class="sxs-lookup"><span data-stu-id="ac1c0-128">Required</span></span></td>
<td><span data-ttu-id="ac1c0-129">定義標題是否包含日期。</span><span class="sxs-lookup"><span data-stu-id="ac1c0-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="ac1c0-130">無</span><span class="sxs-lookup"><span data-stu-id="ac1c0-130">None</span></span></li>
<li><span data-ttu-id="ac1c0-131">Short</span><span class="sxs-lookup"><span data-stu-id="ac1c0-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac1c0-132"><strong>色彩</strong></span><span class="sxs-lookup"><span data-stu-id="ac1c0-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="ac1c0-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="ac1c0-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="ac1c0-134">選擇性</span><span class="sxs-lookup"><span data-stu-id="ac1c0-134">Optional</span></span></td>
<td><span data-ttu-id="ac1c0-135">指定背景的色彩。</span><span class="sxs-lookup"><span data-stu-id="ac1c0-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="ac1c0-136">請參閱 <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="ac1c0-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="ac1c0-137">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ac1c0-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="ac1c0-138">項目類型</span><span class="sxs-lookup"><span data-stu-id="ac1c0-138">Element type</span></span> | <span data-ttu-id="ac1c0-139">[**TitleType**](titletype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="ac1c0-139">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="ac1c0-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="ac1c0-140">Namespace</span></span>    | <span data-ttu-id="ac1c0-141">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="ac1c0-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="ac1c0-142">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="ac1c0-142">Schema name</span></span>  | <span data-ttu-id="ac1c0-143">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="ac1c0-143">Journal Reader</span></span>                                          |



 

 

 



