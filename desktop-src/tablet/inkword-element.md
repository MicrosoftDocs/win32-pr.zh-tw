---
description: 包含筆記本便箋中指定筆墨單字的相關資訊，包括位置、替代項和實際筆墨資料。
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: InkWord 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979011"
---
# <a name="inkword-element"></a><span data-ttu-id="c7629-103">InkWord 元素</span><span class="sxs-lookup"><span data-stu-id="c7629-103">InkWord Element</span></span>

<span data-ttu-id="c7629-104">包含筆記本便箋中指定筆墨單字的相關資訊，包括位置、替代項和實際筆墨資料。</span><span class="sxs-lookup"><span data-stu-id="c7629-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="c7629-105">定義</span><span class="sxs-lookup"><span data-stu-id="c7629-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="c7629-106">父項目</span><span class="sxs-lookup"><span data-stu-id="c7629-106">Parent Elements</span></span>

[<span data-ttu-id="c7629-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="c7629-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="c7629-108">**線條**</span><span class="sxs-lookup"><span data-stu-id="c7629-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="c7629-109">子元素</span><span class="sxs-lookup"><span data-stu-id="c7629-109">Child Elements</span></span>

[<span data-ttu-id="c7629-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="c7629-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="c7629-111">**AlternateList**</span><span class="sxs-lookup"><span data-stu-id="c7629-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="c7629-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="c7629-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="c7629-113">**信賴度**</span><span class="sxs-lookup"><span data-stu-id="c7629-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="c7629-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="c7629-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="c7629-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c7629-115">Attributes</span></span>



| <span data-ttu-id="c7629-116">屬性</span><span class="sxs-lookup"><span data-stu-id="c7629-116">Attribute</span></span>  | <span data-ttu-id="c7629-117">類型</span><span class="sxs-lookup"><span data-stu-id="c7629-117">Type</span></span>                      | <span data-ttu-id="c7629-118">必要</span><span class="sxs-lookup"><span data-stu-id="c7629-118">Required</span></span> | <span data-ttu-id="c7629-119">描述</span><span class="sxs-lookup"><span data-stu-id="c7629-119">Description</span></span>                                                                             | <span data-ttu-id="c7629-120">可能的值</span><span class="sxs-lookup"><span data-stu-id="c7629-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="c7629-121">**離開**</span><span class="sxs-lookup"><span data-stu-id="c7629-121">**Left**</span></span>   | <span data-ttu-id="c7629-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="c7629-122">**xs:integer**</span></span>            | <span data-ttu-id="c7629-123">必要</span><span class="sxs-lookup"><span data-stu-id="c7629-123">Required</span></span> | <span data-ttu-id="c7629-124">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="c7629-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="c7629-125">任何整數。</span><span class="sxs-lookup"><span data-stu-id="c7629-125">Any integer.</span></span>              |
| <span data-ttu-id="c7629-126">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="c7629-126">**Top**</span></span>    | <span data-ttu-id="c7629-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="c7629-127">**xs:integer**</span></span>            | <span data-ttu-id="c7629-128">必要</span><span class="sxs-lookup"><span data-stu-id="c7629-128">Required</span></span> | <span data-ttu-id="c7629-129">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="c7629-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="c7629-130">任何整數。</span><span class="sxs-lookup"><span data-stu-id="c7629-130">Any integer.</span></span>              |
| <span data-ttu-id="c7629-131">**寬度**</span><span class="sxs-lookup"><span data-stu-id="c7629-131">**Width**</span></span>  | <span data-ttu-id="c7629-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="c7629-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="c7629-133">必要</span><span class="sxs-lookup"><span data-stu-id="c7629-133">Required</span></span> | <span data-ttu-id="c7629-134">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="c7629-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="c7629-135">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="c7629-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="c7629-136">**高度**</span><span class="sxs-lookup"><span data-stu-id="c7629-136">**Height**</span></span> | <span data-ttu-id="c7629-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="c7629-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="c7629-138">必要</span><span class="sxs-lookup"><span data-stu-id="c7629-138">Required</span></span> | <span data-ttu-id="c7629-139">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="c7629-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="c7629-140">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="c7629-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="c7629-141">筆墨單字的內部座標組應為英文計量單位，而您的應用程式必須使用2.54 的乘數，將寬度和高度值轉換為 Tablet PC 平臺 Api 所使用的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="c7629-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="c7629-142">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c7629-142">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="c7629-143">項目類型</span><span class="sxs-lookup"><span data-stu-id="c7629-143">Element type</span></span> | <span data-ttu-id="c7629-144">[**InkWordType**](inkwordtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="c7629-144">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="c7629-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="c7629-145">Namespace</span></span>    | <span data-ttu-id="c7629-146">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="c7629-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="c7629-147">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="c7629-147">Schema name</span></span>  | <span data-ttu-id="c7629-148">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="c7629-148">Journal Reader</span></span>                                              |



 

 

 



