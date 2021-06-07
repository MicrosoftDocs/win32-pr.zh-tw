---
description: 在日誌檔中包含影像的編碼二進位資料（如果有的話）。
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Image 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432580"
---
# <a name="image-element"></a><span data-ttu-id="fbbef-103">Image 元素</span><span class="sxs-lookup"><span data-stu-id="fbbef-103">Image Element</span></span>

<span data-ttu-id="fbbef-104">在日誌檔中包含影像的編碼二進位資料（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="fbbef-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="fbbef-105">定義</span><span class="sxs-lookup"><span data-stu-id="fbbef-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="fbbef-106">父項目</span><span class="sxs-lookup"><span data-stu-id="fbbef-106">Parent Elements</span></span>

[<span data-ttu-id="fbbef-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="fbbef-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="fbbef-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="fbbef-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="fbbef-109">子元素</span><span class="sxs-lookup"><span data-stu-id="fbbef-109">Child Elements</span></span>

<span data-ttu-id="fbbef-110">無。</span><span class="sxs-lookup"><span data-stu-id="fbbef-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="fbbef-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fbbef-111">Attributes</span></span>



| <span data-ttu-id="fbbef-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fbbef-112">Attribute</span></span>  | <span data-ttu-id="fbbef-113">類型</span><span class="sxs-lookup"><span data-stu-id="fbbef-113">Type</span></span>                      | <span data-ttu-id="fbbef-114">必要</span><span class="sxs-lookup"><span data-stu-id="fbbef-114">Required</span></span> | <span data-ttu-id="fbbef-115">描述</span><span class="sxs-lookup"><span data-stu-id="fbbef-115">Description</span></span>                                                                             | <span data-ttu-id="fbbef-116">可能的值</span><span class="sxs-lookup"><span data-stu-id="fbbef-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="fbbef-117">**離開**</span><span class="sxs-lookup"><span data-stu-id="fbbef-117">**Left**</span></span>   | <span data-ttu-id="fbbef-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="fbbef-118">**xs:integer**</span></span>            | <span data-ttu-id="fbbef-119">必要</span><span class="sxs-lookup"><span data-stu-id="fbbef-119">Required</span></span> | <span data-ttu-id="fbbef-120">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="fbbef-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="fbbef-121">任何整數。</span><span class="sxs-lookup"><span data-stu-id="fbbef-121">Any integer.</span></span>              |
| <span data-ttu-id="fbbef-122">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="fbbef-122">**Top**</span></span>    | <span data-ttu-id="fbbef-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="fbbef-123">**xs:integer**</span></span>            | <span data-ttu-id="fbbef-124">必要</span><span class="sxs-lookup"><span data-stu-id="fbbef-124">Required</span></span> | <span data-ttu-id="fbbef-125">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="fbbef-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="fbbef-126">任何整數。</span><span class="sxs-lookup"><span data-stu-id="fbbef-126">Any integer.</span></span>              |
| <span data-ttu-id="fbbef-127">**寬度**</span><span class="sxs-lookup"><span data-stu-id="fbbef-127">**Width**</span></span>  | <span data-ttu-id="fbbef-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="fbbef-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="fbbef-129">必要</span><span class="sxs-lookup"><span data-stu-id="fbbef-129">Required</span></span> | <span data-ttu-id="fbbef-130">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="fbbef-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="fbbef-131">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="fbbef-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="fbbef-132">**高度**</span><span class="sxs-lookup"><span data-stu-id="fbbef-132">**Height**</span></span> | <span data-ttu-id="fbbef-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="fbbef-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="fbbef-134">必要</span><span class="sxs-lookup"><span data-stu-id="fbbef-134">Required</span></span> | <span data-ttu-id="fbbef-135">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="fbbef-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="fbbef-136">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="fbbef-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="fbbef-137">項目資訊</span><span class="sxs-lookup"><span data-stu-id="fbbef-137">Element Information</span></span>



|  <span data-ttu-id="fbbef-138">元素</span><span class="sxs-lookup"><span data-stu-id="fbbef-138">Element</span></span>     | <span data-ttu-id="fbbef-139">值</span><span class="sxs-lookup"><span data-stu-id="fbbef-139">Value</span></span>                                                     |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="fbbef-140">項目類型</span><span class="sxs-lookup"><span data-stu-id="fbbef-140">Element type</span></span> | <span data-ttu-id="fbbef-141">[**ImageType**](imagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="fbbef-141">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="fbbef-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="fbbef-142">Namespace</span></span>    | <span data-ttu-id="fbbef-143">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="fbbef-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="fbbef-144">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="fbbef-144">Schema name</span></span>  | <span data-ttu-id="fbbef-145">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="fbbef-145">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="fbbef-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbbef-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbbef-147">**背景**</span><span class="sxs-lookup"><span data-stu-id="fbbef-147">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



