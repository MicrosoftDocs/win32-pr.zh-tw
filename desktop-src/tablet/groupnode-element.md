---
description: 包含一組&8212 的元素 \# ;在筆記本便箋中群組在一起的段落、InkWord、繪圖、文字、影像或旗標&\# 郵件;。
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: GroupNode 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432569"
---
# <a name="groupnode-element"></a><span data-ttu-id="5c6fe-103">GroupNode 元素</span><span class="sxs-lookup"><span data-stu-id="5c6fe-103">GroupNode Element</span></span>

<span data-ttu-id="5c6fe-104">包含在筆記本便箋中群組在一起的一組元素（[**段落**](paragraph-element.md)、 [**InkWord**](inkword-element.md)、 [**繪圖**](drawing-element.md)、 [**文字**](text-element.md)、 [**影像**](image-element.md)或 [**旗**](flag-element.md)標）。</span><span class="sxs-lookup"><span data-stu-id="5c6fe-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="5c6fe-105">定義</span><span class="sxs-lookup"><span data-stu-id="5c6fe-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="5c6fe-106">父項目</span><span class="sxs-lookup"><span data-stu-id="5c6fe-106">Parent Elements</span></span>

[<span data-ttu-id="5c6fe-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="5c6fe-108">子元素</span><span class="sxs-lookup"><span data-stu-id="5c6fe-108">Child Elements</span></span>

[<span data-ttu-id="5c6fe-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="5c6fe-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="5c6fe-111">**繪圖**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="5c6fe-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="5c6fe-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="5c6fe-114">**旗標**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="5c6fe-115">屬性</span><span class="sxs-lookup"><span data-stu-id="5c6fe-115">Attributes</span></span>



| <span data-ttu-id="5c6fe-116">屬性</span><span class="sxs-lookup"><span data-stu-id="5c6fe-116">Attribute</span></span>  | <span data-ttu-id="5c6fe-117">類型</span><span class="sxs-lookup"><span data-stu-id="5c6fe-117">Type</span></span>                      | <span data-ttu-id="5c6fe-118">必要</span><span class="sxs-lookup"><span data-stu-id="5c6fe-118">Required</span></span> | <span data-ttu-id="5c6fe-119">描述</span><span class="sxs-lookup"><span data-stu-id="5c6fe-119">Description</span></span>                                                                             | <span data-ttu-id="5c6fe-120">可能的值</span><span class="sxs-lookup"><span data-stu-id="5c6fe-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="5c6fe-121">**離開**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-121">**Left**</span></span>   | <span data-ttu-id="5c6fe-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-122">**xs:integer**</span></span>            | <span data-ttu-id="5c6fe-123">必要</span><span class="sxs-lookup"><span data-stu-id="5c6fe-123">Required</span></span> | <span data-ttu-id="5c6fe-124">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="5c6fe-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="5c6fe-125">任何整數。</span><span class="sxs-lookup"><span data-stu-id="5c6fe-125">Any integer.</span></span>              |
| <span data-ttu-id="5c6fe-126">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-126">**Top**</span></span>    | <span data-ttu-id="5c6fe-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-127">**xs:integer**</span></span>            | <span data-ttu-id="5c6fe-128">必要</span><span class="sxs-lookup"><span data-stu-id="5c6fe-128">Required</span></span> | <span data-ttu-id="5c6fe-129">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="5c6fe-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="5c6fe-130">任何整數。</span><span class="sxs-lookup"><span data-stu-id="5c6fe-130">Any integer.</span></span>              |
| <span data-ttu-id="5c6fe-131">**寬度**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-131">**Width**</span></span>  | <span data-ttu-id="5c6fe-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5c6fe-133">必要</span><span class="sxs-lookup"><span data-stu-id="5c6fe-133">Required</span></span> | <span data-ttu-id="5c6fe-134">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="5c6fe-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="5c6fe-135">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="5c6fe-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="5c6fe-136">**高度**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-136">**Height**</span></span> | <span data-ttu-id="5c6fe-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5c6fe-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5c6fe-138">必要</span><span class="sxs-lookup"><span data-stu-id="5c6fe-138">Required</span></span> | <span data-ttu-id="5c6fe-139">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="5c6fe-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="5c6fe-140">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="5c6fe-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="5c6fe-141">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5c6fe-141">Element Information</span></span>



|  <span data-ttu-id="5c6fe-142">元素</span><span class="sxs-lookup"><span data-stu-id="5c6fe-142">Element</span></span>     | <span data-ttu-id="5c6fe-143">值</span><span class="sxs-lookup"><span data-stu-id="5c6fe-143">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="5c6fe-144">項目類型</span><span class="sxs-lookup"><span data-stu-id="5c6fe-144">Element type</span></span> | <span data-ttu-id="5c6fe-145">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="5c6fe-145">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="5c6fe-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="5c6fe-146">Namespace</span></span>    | <span data-ttu-id="5c6fe-147">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="5c6fe-147">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="5c6fe-148">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="5c6fe-148">Schema name</span></span>  | <span data-ttu-id="5c6fe-149">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="5c6fe-149">Journal Reader</span></span>                                                  |



 

 

 



