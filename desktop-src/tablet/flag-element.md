---
description: 包含與筆記本便箋區段相關聯之旗標的 base64 編碼點陣圖。
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: 旗標元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46508f9821379fbedb3291ba45d16dbdd0fb316f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432321"
---
# <a name="flag-element"></a><span data-ttu-id="f3ba0-103">旗標元素</span><span class="sxs-lookup"><span data-stu-id="f3ba0-103">Flag Element</span></span>

<span data-ttu-id="f3ba0-104">包含與筆記本便箋區段相關聯之旗標的 base64 編碼點陣圖。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="f3ba0-105">定義</span><span class="sxs-lookup"><span data-stu-id="f3ba0-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="f3ba0-106">父項目</span><span class="sxs-lookup"><span data-stu-id="f3ba0-106">Parent Elements</span></span>

[<span data-ttu-id="f3ba0-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="f3ba0-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="f3ba0-109">子元素</span><span class="sxs-lookup"><span data-stu-id="f3ba0-109">Child Elements</span></span>

<span data-ttu-id="f3ba0-110">無。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="f3ba0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f3ba0-111">Attributes</span></span>



| <span data-ttu-id="f3ba0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f3ba0-112">Attribute</span></span>  | <span data-ttu-id="f3ba0-113">類型</span><span class="sxs-lookup"><span data-stu-id="f3ba0-113">Type</span></span>                      | <span data-ttu-id="f3ba0-114">必要</span><span class="sxs-lookup"><span data-stu-id="f3ba0-114">Required</span></span> | <span data-ttu-id="f3ba0-115">描述</span><span class="sxs-lookup"><span data-stu-id="f3ba0-115">Description</span></span>                                                                             | <span data-ttu-id="f3ba0-116">可能的值</span><span class="sxs-lookup"><span data-stu-id="f3ba0-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="f3ba0-117">**離開**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-117">**Left**</span></span>   | <span data-ttu-id="f3ba0-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-118">**xs:integer**</span></span>            | <span data-ttu-id="f3ba0-119">必要</span><span class="sxs-lookup"><span data-stu-id="f3ba0-119">Required</span></span> | <span data-ttu-id="f3ba0-120">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="f3ba0-121">任何整數。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-121">Any integer.</span></span>              |
| <span data-ttu-id="f3ba0-122">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-122">**Top**</span></span>    | <span data-ttu-id="f3ba0-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-123">**xs:integer**</span></span>            | <span data-ttu-id="f3ba0-124">必要</span><span class="sxs-lookup"><span data-stu-id="f3ba0-124">Required</span></span> | <span data-ttu-id="f3ba0-125">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="f3ba0-126">任何整數。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-126">Any integer.</span></span>              |
| <span data-ttu-id="f3ba0-127">**寬度**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-127">**Width**</span></span>  | <span data-ttu-id="f3ba0-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f3ba0-129">必要</span><span class="sxs-lookup"><span data-stu-id="f3ba0-129">Required</span></span> | <span data-ttu-id="f3ba0-130">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="f3ba0-131">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="f3ba0-132">**高度**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-132">**Height**</span></span> | <span data-ttu-id="f3ba0-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f3ba0-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f3ba0-134">必要</span><span class="sxs-lookup"><span data-stu-id="f3ba0-134">Required</span></span> | <span data-ttu-id="f3ba0-135">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="f3ba0-136">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="f3ba0-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="f3ba0-137">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f3ba0-137">Element Information</span></span>



|  <span data-ttu-id="f3ba0-138">元素</span><span class="sxs-lookup"><span data-stu-id="f3ba0-138">Element</span></span>     | <span data-ttu-id="f3ba0-139">值</span><span class="sxs-lookup"><span data-stu-id="f3ba0-139">Value</span></span>                                                     |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="f3ba0-140">項目類型</span><span class="sxs-lookup"><span data-stu-id="f3ba0-140">Element type</span></span> | <span data-ttu-id="f3ba0-141">[**FlagType**](flagtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="f3ba0-141">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="f3ba0-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3ba0-142">Namespace</span></span>    | <span data-ttu-id="f3ba0-143">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="f3ba0-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="f3ba0-144">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="f3ba0-144">Schema name</span></span>  | <span data-ttu-id="f3ba0-145">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="f3ba0-145">Journal Reader</span></span>                                        |



 

 

 



