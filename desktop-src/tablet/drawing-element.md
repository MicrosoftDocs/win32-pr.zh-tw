---
description: 包含已由分析器或使用者分類為繪圖的內容。
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: 繪圖元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe516a4ba33e6e597b17ce8365d792f19468c3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982766"
---
# <a name="drawing-element"></a><span data-ttu-id="e0bf7-103">繪圖元素</span><span class="sxs-lookup"><span data-stu-id="e0bf7-103">Drawing Element</span></span>

<span data-ttu-id="e0bf7-104">包含已由分析器或使用者分類為繪圖的內容。</span><span class="sxs-lookup"><span data-stu-id="e0bf7-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="e0bf7-105">定義</span><span class="sxs-lookup"><span data-stu-id="e0bf7-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="e0bf7-106">父項目</span><span class="sxs-lookup"><span data-stu-id="e0bf7-106">Parent Elements</span></span>

[<span data-ttu-id="e0bf7-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="e0bf7-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="e0bf7-109">子元素</span><span class="sxs-lookup"><span data-stu-id="e0bf7-109">Child Elements</span></span>

[<span data-ttu-id="e0bf7-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="e0bf7-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="e0bf7-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="e0bf7-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="e0bf7-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e0bf7-114">Attributes</span></span>



| <span data-ttu-id="e0bf7-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e0bf7-115">Attribute</span></span>  | <span data-ttu-id="e0bf7-116">類型</span><span class="sxs-lookup"><span data-stu-id="e0bf7-116">Type</span></span>                      | <span data-ttu-id="e0bf7-117">必要</span><span class="sxs-lookup"><span data-stu-id="e0bf7-117">Required</span></span> | <span data-ttu-id="e0bf7-118">描述</span><span class="sxs-lookup"><span data-stu-id="e0bf7-118">Description</span></span>                                                                             | <span data-ttu-id="e0bf7-119">可能的值</span><span class="sxs-lookup"><span data-stu-id="e0bf7-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="e0bf7-120">**離開**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-120">**Left**</span></span>   | <span data-ttu-id="e0bf7-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-121">**xs:integer**</span></span>            | <span data-ttu-id="e0bf7-122">必要</span><span class="sxs-lookup"><span data-stu-id="e0bf7-122">Required</span></span> | <span data-ttu-id="e0bf7-123">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="e0bf7-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="e0bf7-124">任何整數。</span><span class="sxs-lookup"><span data-stu-id="e0bf7-124">Any integer.</span></span>              |
| <span data-ttu-id="e0bf7-125">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-125">**Top**</span></span>    | <span data-ttu-id="e0bf7-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-126">**xs:integer**</span></span>            | <span data-ttu-id="e0bf7-127">必要</span><span class="sxs-lookup"><span data-stu-id="e0bf7-127">Required</span></span> | <span data-ttu-id="e0bf7-128">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="e0bf7-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="e0bf7-129">任何整數。</span><span class="sxs-lookup"><span data-stu-id="e0bf7-129">Any integer.</span></span>              |
| <span data-ttu-id="e0bf7-130">**寬度**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-130">**Width**</span></span>  | <span data-ttu-id="e0bf7-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e0bf7-132">必要</span><span class="sxs-lookup"><span data-stu-id="e0bf7-132">Required</span></span> | <span data-ttu-id="e0bf7-133">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="e0bf7-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="e0bf7-134">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="e0bf7-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="e0bf7-135">**高度**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-135">**Height**</span></span> | <span data-ttu-id="e0bf7-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="e0bf7-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="e0bf7-137">必要</span><span class="sxs-lookup"><span data-stu-id="e0bf7-137">Required</span></span> | <span data-ttu-id="e0bf7-138">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="e0bf7-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="e0bf7-139">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="e0bf7-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="e0bf7-140">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e0bf7-140">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="e0bf7-141">項目類型</span><span class="sxs-lookup"><span data-stu-id="e0bf7-141">Element type</span></span> | <span data-ttu-id="e0bf7-142">[**DrawingType**](drawingtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="e0bf7-142">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="e0bf7-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="e0bf7-143">Namespace</span></span>    | <span data-ttu-id="e0bf7-144">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="e0bf7-144">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="e0bf7-145">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="e0bf7-145">Schema name</span></span>  | <span data-ttu-id="e0bf7-146">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="e0bf7-146">Journal Reader</span></span>                                              |



 

 

 



