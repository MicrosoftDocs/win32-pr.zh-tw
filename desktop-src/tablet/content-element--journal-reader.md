---
description: 包含日誌頁面的內容。
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content 元素 [筆記本讀取器]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991887"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="f41f7-103">Content 元素 \[ 日誌讀取器\]</span><span class="sxs-lookup"><span data-stu-id="f41f7-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="f41f7-104">包含日誌頁面的內容。</span><span class="sxs-lookup"><span data-stu-id="f41f7-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="f41f7-105">定義</span><span class="sxs-lookup"><span data-stu-id="f41f7-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="f41f7-106">父項目</span><span class="sxs-lookup"><span data-stu-id="f41f7-106">Parent Elements</span></span>

[<span data-ttu-id="f41f7-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="f41f7-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="f41f7-108">子元素</span><span class="sxs-lookup"><span data-stu-id="f41f7-108">Child Elements</span></span>

[<span data-ttu-id="f41f7-109">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="f41f7-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="f41f7-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="f41f7-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="f41f7-111">**繪圖**</span><span class="sxs-lookup"><span data-stu-id="f41f7-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="f41f7-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="f41f7-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="f41f7-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="f41f7-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="f41f7-114">**旗標**</span><span class="sxs-lookup"><span data-stu-id="f41f7-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="f41f7-115">屬性</span><span class="sxs-lookup"><span data-stu-id="f41f7-115">Attributes</span></span>



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
<th><span data-ttu-id="f41f7-116">屬性</span><span class="sxs-lookup"><span data-stu-id="f41f7-116">Attribute</span></span></th>
<th><span data-ttu-id="f41f7-117">類型</span><span class="sxs-lookup"><span data-stu-id="f41f7-117">Type</span></span></th>
<th><span data-ttu-id="f41f7-118">必要</span><span class="sxs-lookup"><span data-stu-id="f41f7-118">Required</span></span></th>
<th><span data-ttu-id="f41f7-119">描述</span><span class="sxs-lookup"><span data-stu-id="f41f7-119">Description</span></span></th>
<th><span data-ttu-id="f41f7-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="f41f7-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f41f7-121"><strong>型別</strong></span><span class="sxs-lookup"><span data-stu-id="f41f7-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="f41f7-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span><span class="sxs-lookup"><span data-stu-id="f41f7-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="f41f7-123">必要</span><span class="sxs-lookup"><span data-stu-id="f41f7-123">Required</span></span></td>
<td><span data-ttu-id="f41f7-124">如果類型為 &quot; 惰性 &quot; ，則無法修改內容。</span><span class="sxs-lookup"><span data-stu-id="f41f7-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="f41f7-125">正常</span><span class="sxs-lookup"><span data-stu-id="f41f7-125">Normal</span></span></li>
<li><span data-ttu-id="f41f7-126">惰性</span><span class="sxs-lookup"><span data-stu-id="f41f7-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="f41f7-127">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f41f7-127">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="f41f7-128">項目類型</span><span class="sxs-lookup"><span data-stu-id="f41f7-128">Element type</span></span> | <span data-ttu-id="f41f7-129">[**ContentType**](contenttype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="f41f7-129">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="f41f7-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="f41f7-130">Namespace</span></span>    | <span data-ttu-id="f41f7-131">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="f41f7-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="f41f7-132">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="f41f7-132">Schema name</span></span>  | <span data-ttu-id="f41f7-133">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="f41f7-133">Journal Reader</span></span>                                              |



 

 

 




