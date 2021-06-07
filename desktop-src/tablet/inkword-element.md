---
description: 包含筆記本便箋中指定筆墨單字的相關資訊，包括位置、替代項和實際筆墨資料。
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: InkWord 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dc9baea7cda0346e82c11331c45f453e61f192
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432390"
---
# <a name="inkword-element"></a><span data-ttu-id="b2e85-103">InkWord 元素</span><span class="sxs-lookup"><span data-stu-id="b2e85-103">InkWord Element</span></span>

<span data-ttu-id="b2e85-104">包含筆記本便箋中指定筆墨單字的相關資訊，包括位置、替代項和實際筆墨資料。</span><span class="sxs-lookup"><span data-stu-id="b2e85-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="b2e85-105">定義</span><span class="sxs-lookup"><span data-stu-id="b2e85-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="b2e85-106">父項目</span><span class="sxs-lookup"><span data-stu-id="b2e85-106">Parent Elements</span></span>

[<span data-ttu-id="b2e85-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="b2e85-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="b2e85-108">**折線圖**</span><span class="sxs-lookup"><span data-stu-id="b2e85-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="b2e85-109">子元素</span><span class="sxs-lookup"><span data-stu-id="b2e85-109">Child Elements</span></span>

[<span data-ttu-id="b2e85-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="b2e85-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="b2e85-111">**AlternateList**</span><span class="sxs-lookup"><span data-stu-id="b2e85-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="b2e85-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="b2e85-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="b2e85-113">**信賴度**</span><span class="sxs-lookup"><span data-stu-id="b2e85-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="b2e85-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="b2e85-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="b2e85-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b2e85-115">Attributes</span></span>



| <span data-ttu-id="b2e85-116">屬性</span><span class="sxs-lookup"><span data-stu-id="b2e85-116">Attribute</span></span>  | <span data-ttu-id="b2e85-117">類型</span><span class="sxs-lookup"><span data-stu-id="b2e85-117">Type</span></span>                      | <span data-ttu-id="b2e85-118">必要</span><span class="sxs-lookup"><span data-stu-id="b2e85-118">Required</span></span> | <span data-ttu-id="b2e85-119">描述</span><span class="sxs-lookup"><span data-stu-id="b2e85-119">Description</span></span>                                                                             | <span data-ttu-id="b2e85-120">可能的值</span><span class="sxs-lookup"><span data-stu-id="b2e85-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="b2e85-121">**離開**</span><span class="sxs-lookup"><span data-stu-id="b2e85-121">**Left**</span></span>   | <span data-ttu-id="b2e85-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b2e85-122">**xs:integer**</span></span>            | <span data-ttu-id="b2e85-123">必要</span><span class="sxs-lookup"><span data-stu-id="b2e85-123">Required</span></span> | <span data-ttu-id="b2e85-124">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="b2e85-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="b2e85-125">任何整數。</span><span class="sxs-lookup"><span data-stu-id="b2e85-125">Any integer.</span></span>              |
| <span data-ttu-id="b2e85-126">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="b2e85-126">**Top**</span></span>    | <span data-ttu-id="b2e85-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b2e85-127">**xs:integer**</span></span>            | <span data-ttu-id="b2e85-128">必要</span><span class="sxs-lookup"><span data-stu-id="b2e85-128">Required</span></span> | <span data-ttu-id="b2e85-129">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="b2e85-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="b2e85-130">任何整數。</span><span class="sxs-lookup"><span data-stu-id="b2e85-130">Any integer.</span></span>              |
| <span data-ttu-id="b2e85-131">**寬度**</span><span class="sxs-lookup"><span data-stu-id="b2e85-131">**Width**</span></span>  | <span data-ttu-id="b2e85-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b2e85-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b2e85-133">必要</span><span class="sxs-lookup"><span data-stu-id="b2e85-133">Required</span></span> | <span data-ttu-id="b2e85-134">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="b2e85-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="b2e85-135">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="b2e85-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="b2e85-136">**高度**</span><span class="sxs-lookup"><span data-stu-id="b2e85-136">**Height**</span></span> | <span data-ttu-id="b2e85-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b2e85-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b2e85-138">必要</span><span class="sxs-lookup"><span data-stu-id="b2e85-138">Required</span></span> | <span data-ttu-id="b2e85-139">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="b2e85-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="b2e85-140">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="b2e85-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="b2e85-141">筆墨單字的內部座標組應為英文計量單位，而您的應用程式必須使用2.54 的乘數，將寬度和高度值轉換為 Tablet PC 平臺 Api 所使用的 HIMETRIC 單位。</span><span class="sxs-lookup"><span data-stu-id="b2e85-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="b2e85-142">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b2e85-142">Element Information</span></span>



|  <span data-ttu-id="b2e85-143">元素</span><span class="sxs-lookup"><span data-stu-id="b2e85-143">Element</span></span>     | <span data-ttu-id="b2e85-144">值</span><span class="sxs-lookup"><span data-stu-id="b2e85-144">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="b2e85-145">項目類型</span><span class="sxs-lookup"><span data-stu-id="b2e85-145">Element type</span></span> | <span data-ttu-id="b2e85-146">[**InkWordType**](inkwordtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="b2e85-146">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="b2e85-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="b2e85-147">Namespace</span></span>    | <span data-ttu-id="b2e85-148">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="b2e85-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="b2e85-149">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="b2e85-149">Schema name</span></span>  | <span data-ttu-id="b2e85-150">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="b2e85-150">Journal Reader</span></span>                                              |



 

 

 



