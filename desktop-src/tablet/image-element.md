---
description: 在日誌檔中包含影像的編碼二進位資料（如果有的話）。
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Image 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975361"
---
# <a name="image-element"></a><span data-ttu-id="ec2d6-103">Image 元素</span><span class="sxs-lookup"><span data-stu-id="ec2d6-103">Image Element</span></span>

<span data-ttu-id="ec2d6-104">在日誌檔中包含影像的編碼二進位資料（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="ec2d6-105">定義</span><span class="sxs-lookup"><span data-stu-id="ec2d6-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="ec2d6-106">父項目</span><span class="sxs-lookup"><span data-stu-id="ec2d6-106">Parent Elements</span></span>

[<span data-ttu-id="ec2d6-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="ec2d6-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="ec2d6-109">子元素</span><span class="sxs-lookup"><span data-stu-id="ec2d6-109">Child Elements</span></span>

<span data-ttu-id="ec2d6-110">無。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="ec2d6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ec2d6-111">Attributes</span></span>



| <span data-ttu-id="ec2d6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ec2d6-112">Attribute</span></span>  | <span data-ttu-id="ec2d6-113">類型</span><span class="sxs-lookup"><span data-stu-id="ec2d6-113">Type</span></span>                      | <span data-ttu-id="ec2d6-114">必要</span><span class="sxs-lookup"><span data-stu-id="ec2d6-114">Required</span></span> | <span data-ttu-id="ec2d6-115">描述</span><span class="sxs-lookup"><span data-stu-id="ec2d6-115">Description</span></span>                                                                             | <span data-ttu-id="ec2d6-116">可能的值</span><span class="sxs-lookup"><span data-stu-id="ec2d6-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="ec2d6-117">**離開**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-117">**Left**</span></span>   | <span data-ttu-id="ec2d6-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-118">**xs:integer**</span></span>            | <span data-ttu-id="ec2d6-119">必要</span><span class="sxs-lookup"><span data-stu-id="ec2d6-119">Required</span></span> | <span data-ttu-id="ec2d6-120">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="ec2d6-121">任何整數。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-121">Any integer.</span></span>              |
| <span data-ttu-id="ec2d6-122">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-122">**Top**</span></span>    | <span data-ttu-id="ec2d6-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-123">**xs:integer**</span></span>            | <span data-ttu-id="ec2d6-124">必要</span><span class="sxs-lookup"><span data-stu-id="ec2d6-124">Required</span></span> | <span data-ttu-id="ec2d6-125">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="ec2d6-126">任何整數。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-126">Any integer.</span></span>              |
| <span data-ttu-id="ec2d6-127">**寬度**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-127">**Width**</span></span>  | <span data-ttu-id="ec2d6-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ec2d6-129">必要</span><span class="sxs-lookup"><span data-stu-id="ec2d6-129">Required</span></span> | <span data-ttu-id="ec2d6-130">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="ec2d6-131">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="ec2d6-132">**高度**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-132">**Height**</span></span> | <span data-ttu-id="ec2d6-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ec2d6-134">必要</span><span class="sxs-lookup"><span data-stu-id="ec2d6-134">Required</span></span> | <span data-ttu-id="ec2d6-135">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="ec2d6-136">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="ec2d6-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="ec2d6-137">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ec2d6-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="ec2d6-138">項目類型</span><span class="sxs-lookup"><span data-stu-id="ec2d6-138">Element type</span></span> | <span data-ttu-id="ec2d6-139">[**ImageType**](imagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="ec2d6-139">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="ec2d6-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec2d6-140">Namespace</span></span>    | <span data-ttu-id="ec2d6-141">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="ec2d6-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="ec2d6-142">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="ec2d6-142">Schema name</span></span>  | <span data-ttu-id="ec2d6-143">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="ec2d6-143">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="ec2d6-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec2d6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2d6-145">**背景**</span><span class="sxs-lookup"><span data-stu-id="ec2d6-145">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



