---
description: 包含 JournalDocument 元素或 JournalPage 元素的背景。
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Background 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980418"
---
# <a name="background-element"></a><span data-ttu-id="b4726-103">Background 元素</span><span class="sxs-lookup"><span data-stu-id="b4726-103">Background Element</span></span>

<span data-ttu-id="b4726-104">包含 [**JournalDocument**](journaldocument-element.md) 元素或 [**JournalPage**](journalpage-element.md) 元素的背景。</span><span class="sxs-lookup"><span data-stu-id="b4726-104">Contains the background for a [**JournalDocument**](journaldocument-element.md) element or [**JournalPage**](journalpage-element.md) element.</span></span>

## <a name="definition"></a><span data-ttu-id="b4726-105">定義</span><span class="sxs-lookup"><span data-stu-id="b4726-105">Definition</span></span>

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="b4726-106">父項目</span><span class="sxs-lookup"><span data-stu-id="b4726-106">Parent Elements</span></span>

[<span data-ttu-id="b4726-107">**信箋**</span><span class="sxs-lookup"><span data-stu-id="b4726-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="b4726-108">子元素</span><span class="sxs-lookup"><span data-stu-id="b4726-108">Child Elements</span></span>

[<span data-ttu-id="b4726-109">**Image**</span><span class="sxs-lookup"><span data-stu-id="b4726-109">**Image**</span></span>](image-element.md)

## <a name="attributes"></a><span data-ttu-id="b4726-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b4726-110">Attributes</span></span>



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
<th><span data-ttu-id="b4726-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b4726-111">Attribute</span></span></th>
<th><span data-ttu-id="b4726-112">類型</span><span class="sxs-lookup"><span data-stu-id="b4726-112">Type</span></span></th>
<th><span data-ttu-id="b4726-113">必要</span><span class="sxs-lookup"><span data-stu-id="b4726-113">Required</span></span></th>
<th><span data-ttu-id="b4726-114">描述</span><span class="sxs-lookup"><span data-stu-id="b4726-114">Description</span></span></th>
<th><span data-ttu-id="b4726-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="b4726-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4726-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="b4726-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="b4726-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="b4726-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="b4726-118">必要</span><span class="sxs-lookup"><span data-stu-id="b4726-118">Required</span></span></td>
<td><span data-ttu-id="b4726-119">指定背景的樣式。</span><span class="sxs-lookup"><span data-stu-id="b4726-119">Specifies the style of the background.</span></span></td>
<td><ul>
<li><span data-ttu-id="b4726-120">無</span><span class="sxs-lookup"><span data-stu-id="b4726-120">None</span></span></li>
<li><span data-ttu-id="b4726-121">實線</span><span class="sxs-lookup"><span data-stu-id="b4726-121">Solid</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4726-122"><strong>色彩</strong></span><span class="sxs-lookup"><span data-stu-id="b4726-122"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="b4726-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="b4726-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="b4726-124">選擇性</span><span class="sxs-lookup"><span data-stu-id="b4726-124">Optional</span></span></td>
<td><span data-ttu-id="b4726-125">指定背景的色彩。</span><span class="sxs-lookup"><span data-stu-id="b4726-125">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="b4726-126">請參閱 <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType。</span><span class="sxs-lookup"><span data-stu-id="b4726-126">See <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="b4726-127">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b4726-127">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="b4726-128">項目類型</span><span class="sxs-lookup"><span data-stu-id="b4726-128">Element type</span></span> | <span data-ttu-id="b4726-129">[**BackgroundType**](backgroundtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="b4726-129">[**BackgroundType**](backgroundtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="b4726-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="b4726-130">Namespace</span></span>    | <span data-ttu-id="b4726-131">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="b4726-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="b4726-132">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="b4726-132">Schema name</span></span>  | <span data-ttu-id="b4726-133">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="b4726-133">Journal Reader</span></span>                                                    |



 

 

 



