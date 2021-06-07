---
description: 包含日誌頁面的內容。
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content 元素 [筆記本讀取器]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432150"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="d005d-103">Content 元素 \[ 日誌讀取器\]</span><span class="sxs-lookup"><span data-stu-id="d005d-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="d005d-104">包含日誌頁面的內容。</span><span class="sxs-lookup"><span data-stu-id="d005d-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="d005d-105">定義</span><span class="sxs-lookup"><span data-stu-id="d005d-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="d005d-106">父項目</span><span class="sxs-lookup"><span data-stu-id="d005d-106">Parent Elements</span></span>

[<span data-ttu-id="d005d-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="d005d-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="d005d-108">子元素</span><span class="sxs-lookup"><span data-stu-id="d005d-108">Child Elements</span></span>

[<span data-ttu-id="d005d-109">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="d005d-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="d005d-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="d005d-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="d005d-111">**繪圖**</span><span class="sxs-lookup"><span data-stu-id="d005d-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="d005d-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="d005d-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="d005d-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="d005d-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="d005d-114">**旗標**</span><span class="sxs-lookup"><span data-stu-id="d005d-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="d005d-115">屬性</span><span class="sxs-lookup"><span data-stu-id="d005d-115">Attributes</span></span>



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
<th><span data-ttu-id="d005d-116">屬性</span><span class="sxs-lookup"><span data-stu-id="d005d-116">Attribute</span></span></th>
<th><span data-ttu-id="d005d-117">類型</span><span class="sxs-lookup"><span data-stu-id="d005d-117">Type</span></span></th>
<th><span data-ttu-id="d005d-118">必要</span><span class="sxs-lookup"><span data-stu-id="d005d-118">Required</span></span></th>
<th><span data-ttu-id="d005d-119">描述</span><span class="sxs-lookup"><span data-stu-id="d005d-119">Description</span></span></th>
<th><span data-ttu-id="d005d-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="d005d-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d005d-121"><strong>類型</strong></span><span class="sxs-lookup"><span data-stu-id="d005d-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="d005d-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d005d-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="d005d-123">必要</span><span class="sxs-lookup"><span data-stu-id="d005d-123">Required</span></span></td>
<td><span data-ttu-id="d005d-124">如果類型為 &quot; 惰性 &quot; ，則無法修改內容。</span><span class="sxs-lookup"><span data-stu-id="d005d-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d005d-125">正常</span><span class="sxs-lookup"><span data-stu-id="d005d-125">Normal</span></span></li>
<li><span data-ttu-id="d005d-126">惰性</span><span class="sxs-lookup"><span data-stu-id="d005d-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="d005d-127">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d005d-127">Element Information</span></span>



|  <span data-ttu-id="d005d-128">元素</span><span class="sxs-lookup"><span data-stu-id="d005d-128">Element</span></span>     | <span data-ttu-id="d005d-129">值</span><span class="sxs-lookup"><span data-stu-id="d005d-129">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="d005d-130">項目類型</span><span class="sxs-lookup"><span data-stu-id="d005d-130">Element type</span></span> | <span data-ttu-id="d005d-131">[**ContentType**](contenttype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="d005d-131">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d005d-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="d005d-132">Namespace</span></span>    | <span data-ttu-id="d005d-133">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="d005d-133">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="d005d-134">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="d005d-134">Schema name</span></span>  | <span data-ttu-id="d005d-135">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="d005d-135">Journal Reader</span></span>                                              |



 

 

 




