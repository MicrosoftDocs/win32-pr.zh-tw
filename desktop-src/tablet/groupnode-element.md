---
description: 包含一組&8212 的元素 \# ;在筆記本便箋中群組在一起的段落、InkWord、繪圖、文字、影像或旗標&\# 郵件;。
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: GroupNode 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992413"
---
# <a name="groupnode-element"></a><span data-ttu-id="be73e-103">GroupNode 元素</span><span class="sxs-lookup"><span data-stu-id="be73e-103">GroupNode Element</span></span>

<span data-ttu-id="be73e-104">包含在筆記本便箋中群組在一起的一組元素（[**段落**](paragraph-element.md)、 [**InkWord**](inkword-element.md)、 [**繪圖**](drawing-element.md)、 [**文字**](text-element.md)、 [**影像**](image-element.md)或 [**旗**](flag-element.md)標）。</span><span class="sxs-lookup"><span data-stu-id="be73e-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="be73e-105">定義</span><span class="sxs-lookup"><span data-stu-id="be73e-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="be73e-106">父項目</span><span class="sxs-lookup"><span data-stu-id="be73e-106">Parent Elements</span></span>

[<span data-ttu-id="be73e-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="be73e-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="be73e-108">子元素</span><span class="sxs-lookup"><span data-stu-id="be73e-108">Child Elements</span></span>

[<span data-ttu-id="be73e-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="be73e-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="be73e-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="be73e-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="be73e-111">**繪圖**</span><span class="sxs-lookup"><span data-stu-id="be73e-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="be73e-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="be73e-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="be73e-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="be73e-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="be73e-114">**旗標**</span><span class="sxs-lookup"><span data-stu-id="be73e-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="be73e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="be73e-115">Attributes</span></span>



| <span data-ttu-id="be73e-116">屬性</span><span class="sxs-lookup"><span data-stu-id="be73e-116">Attribute</span></span>  | <span data-ttu-id="be73e-117">類型</span><span class="sxs-lookup"><span data-stu-id="be73e-117">Type</span></span>                      | <span data-ttu-id="be73e-118">必要</span><span class="sxs-lookup"><span data-stu-id="be73e-118">Required</span></span> | <span data-ttu-id="be73e-119">描述</span><span class="sxs-lookup"><span data-stu-id="be73e-119">Description</span></span>                                                                             | <span data-ttu-id="be73e-120">可能的值</span><span class="sxs-lookup"><span data-stu-id="be73e-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="be73e-121">**離開**</span><span class="sxs-lookup"><span data-stu-id="be73e-121">**Left**</span></span>   | <span data-ttu-id="be73e-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="be73e-122">**xs:integer**</span></span>            | <span data-ttu-id="be73e-123">必要</span><span class="sxs-lookup"><span data-stu-id="be73e-123">Required</span></span> | <span data-ttu-id="be73e-124">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="be73e-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="be73e-125">任何整數。</span><span class="sxs-lookup"><span data-stu-id="be73e-125">Any integer.</span></span>              |
| <span data-ttu-id="be73e-126">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="be73e-126">**Top**</span></span>    | <span data-ttu-id="be73e-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="be73e-127">**xs:integer**</span></span>            | <span data-ttu-id="be73e-128">必要</span><span class="sxs-lookup"><span data-stu-id="be73e-128">Required</span></span> | <span data-ttu-id="be73e-129">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="be73e-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="be73e-130">任何整數。</span><span class="sxs-lookup"><span data-stu-id="be73e-130">Any integer.</span></span>              |
| <span data-ttu-id="be73e-131">**寬度**</span><span class="sxs-lookup"><span data-stu-id="be73e-131">**Width**</span></span>  | <span data-ttu-id="be73e-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="be73e-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="be73e-133">必要</span><span class="sxs-lookup"><span data-stu-id="be73e-133">Required</span></span> | <span data-ttu-id="be73e-134">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="be73e-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="be73e-135">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="be73e-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="be73e-136">**高度**</span><span class="sxs-lookup"><span data-stu-id="be73e-136">**Height**</span></span> | <span data-ttu-id="be73e-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="be73e-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="be73e-138">必要</span><span class="sxs-lookup"><span data-stu-id="be73e-138">Required</span></span> | <span data-ttu-id="be73e-139">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="be73e-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="be73e-140">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="be73e-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="be73e-141">項目資訊</span><span class="sxs-lookup"><span data-stu-id="be73e-141">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="be73e-142">項目類型</span><span class="sxs-lookup"><span data-stu-id="be73e-142">Element type</span></span> | <span data-ttu-id="be73e-143">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="be73e-143">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="be73e-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="be73e-144">Namespace</span></span>    | <span data-ttu-id="be73e-145">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="be73e-145">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="be73e-146">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="be73e-146">Schema name</span></span>  | <span data-ttu-id="be73e-147">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="be73e-147">Journal Reader</span></span>                                                  |



 

 

 



