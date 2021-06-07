---
description: 包含已由分析器或使用者分類為繪圖的內容。
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: 繪圖元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432510"
---
# <a name="drawing-element"></a><span data-ttu-id="29d60-103">繪圖元素</span><span class="sxs-lookup"><span data-stu-id="29d60-103">Drawing Element</span></span>

<span data-ttu-id="29d60-104">包含已由分析器或使用者分類為繪圖的內容。</span><span class="sxs-lookup"><span data-stu-id="29d60-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="29d60-105">定義</span><span class="sxs-lookup"><span data-stu-id="29d60-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="29d60-106">父項目</span><span class="sxs-lookup"><span data-stu-id="29d60-106">Parent Elements</span></span>

[<span data-ttu-id="29d60-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="29d60-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="29d60-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="29d60-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="29d60-109">子元素</span><span class="sxs-lookup"><span data-stu-id="29d60-109">Child Elements</span></span>

[<span data-ttu-id="29d60-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="29d60-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="29d60-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="29d60-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="29d60-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="29d60-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="29d60-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="29d60-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="29d60-114">屬性</span><span class="sxs-lookup"><span data-stu-id="29d60-114">Attributes</span></span>



| <span data-ttu-id="29d60-115">屬性</span><span class="sxs-lookup"><span data-stu-id="29d60-115">Attribute</span></span>  | <span data-ttu-id="29d60-116">類型</span><span class="sxs-lookup"><span data-stu-id="29d60-116">Type</span></span>                      | <span data-ttu-id="29d60-117">必要</span><span class="sxs-lookup"><span data-stu-id="29d60-117">Required</span></span> | <span data-ttu-id="29d60-118">描述</span><span class="sxs-lookup"><span data-stu-id="29d60-118">Description</span></span>                                                                             | <span data-ttu-id="29d60-119">可能的值</span><span class="sxs-lookup"><span data-stu-id="29d60-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="29d60-120">**離開**</span><span class="sxs-lookup"><span data-stu-id="29d60-120">**Left**</span></span>   | <span data-ttu-id="29d60-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="29d60-121">**xs:integer**</span></span>            | <span data-ttu-id="29d60-122">必要</span><span class="sxs-lookup"><span data-stu-id="29d60-122">Required</span></span> | <span data-ttu-id="29d60-123">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="29d60-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="29d60-124">任何整數。</span><span class="sxs-lookup"><span data-stu-id="29d60-124">Any integer.</span></span>              |
| <span data-ttu-id="29d60-125">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="29d60-125">**Top**</span></span>    | <span data-ttu-id="29d60-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="29d60-126">**xs:integer**</span></span>            | <span data-ttu-id="29d60-127">必要</span><span class="sxs-lookup"><span data-stu-id="29d60-127">Required</span></span> | <span data-ttu-id="29d60-128">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="29d60-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="29d60-129">任何整數。</span><span class="sxs-lookup"><span data-stu-id="29d60-129">Any integer.</span></span>              |
| <span data-ttu-id="29d60-130">**寬度**</span><span class="sxs-lookup"><span data-stu-id="29d60-130">**Width**</span></span>  | <span data-ttu-id="29d60-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="29d60-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="29d60-132">必要</span><span class="sxs-lookup"><span data-stu-id="29d60-132">Required</span></span> | <span data-ttu-id="29d60-133">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="29d60-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="29d60-134">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="29d60-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="29d60-135">**高度**</span><span class="sxs-lookup"><span data-stu-id="29d60-135">**Height**</span></span> | <span data-ttu-id="29d60-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="29d60-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="29d60-137">必要</span><span class="sxs-lookup"><span data-stu-id="29d60-137">Required</span></span> | <span data-ttu-id="29d60-138">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="29d60-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="29d60-139">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="29d60-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="29d60-140">項目資訊</span><span class="sxs-lookup"><span data-stu-id="29d60-140">Element Information</span></span>



|  <span data-ttu-id="29d60-141">元素</span><span class="sxs-lookup"><span data-stu-id="29d60-141">Element</span></span>     | <span data-ttu-id="29d60-142">值</span><span class="sxs-lookup"><span data-stu-id="29d60-142">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="29d60-143">項目類型</span><span class="sxs-lookup"><span data-stu-id="29d60-143">Element type</span></span> | <span data-ttu-id="29d60-144">[**DrawingType**](drawingtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="29d60-144">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="29d60-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="29d60-145">Namespace</span></span>    | <span data-ttu-id="29d60-146">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="29d60-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="29d60-147">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="29d60-147">Schema name</span></span>  | <span data-ttu-id="29d60-148">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="29d60-148">Journal Reader</span></span>                                              |



 

 

 



