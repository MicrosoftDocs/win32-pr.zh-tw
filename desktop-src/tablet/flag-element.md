---
description: 包含與筆記本便箋區段相關聯之旗標的 base64 編碼點陣圖。
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: 旗標元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971018"
---
# <a name="flag-element"></a><span data-ttu-id="03b5c-103">旗標元素</span><span class="sxs-lookup"><span data-stu-id="03b5c-103">Flag Element</span></span>

<span data-ttu-id="03b5c-104">包含與筆記本便箋區段相關聯之旗標的 base64 編碼點陣圖。</span><span class="sxs-lookup"><span data-stu-id="03b5c-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="03b5c-105">定義</span><span class="sxs-lookup"><span data-stu-id="03b5c-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="03b5c-106">父項目</span><span class="sxs-lookup"><span data-stu-id="03b5c-106">Parent Elements</span></span>

[<span data-ttu-id="03b5c-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="03b5c-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="03b5c-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="03b5c-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="03b5c-109">子元素</span><span class="sxs-lookup"><span data-stu-id="03b5c-109">Child Elements</span></span>

<span data-ttu-id="03b5c-110">無。</span><span class="sxs-lookup"><span data-stu-id="03b5c-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="03b5c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="03b5c-111">Attributes</span></span>



| <span data-ttu-id="03b5c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="03b5c-112">Attribute</span></span>  | <span data-ttu-id="03b5c-113">類型</span><span class="sxs-lookup"><span data-stu-id="03b5c-113">Type</span></span>                      | <span data-ttu-id="03b5c-114">必要</span><span class="sxs-lookup"><span data-stu-id="03b5c-114">Required</span></span> | <span data-ttu-id="03b5c-115">描述</span><span class="sxs-lookup"><span data-stu-id="03b5c-115">Description</span></span>                                                                             | <span data-ttu-id="03b5c-116">可能的值</span><span class="sxs-lookup"><span data-stu-id="03b5c-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="03b5c-117">**離開**</span><span class="sxs-lookup"><span data-stu-id="03b5c-117">**Left**</span></span>   | <span data-ttu-id="03b5c-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="03b5c-118">**xs:integer**</span></span>            | <span data-ttu-id="03b5c-119">必要</span><span class="sxs-lookup"><span data-stu-id="03b5c-119">Required</span></span> | <span data-ttu-id="03b5c-120">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="03b5c-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="03b5c-121">任何整數。</span><span class="sxs-lookup"><span data-stu-id="03b5c-121">Any integer.</span></span>              |
| <span data-ttu-id="03b5c-122">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="03b5c-122">**Top**</span></span>    | <span data-ttu-id="03b5c-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="03b5c-123">**xs:integer**</span></span>            | <span data-ttu-id="03b5c-124">必要</span><span class="sxs-lookup"><span data-stu-id="03b5c-124">Required</span></span> | <span data-ttu-id="03b5c-125">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="03b5c-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="03b5c-126">任何整數。</span><span class="sxs-lookup"><span data-stu-id="03b5c-126">Any integer.</span></span>              |
| <span data-ttu-id="03b5c-127">**寬度**</span><span class="sxs-lookup"><span data-stu-id="03b5c-127">**Width**</span></span>  | <span data-ttu-id="03b5c-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="03b5c-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="03b5c-129">必要</span><span class="sxs-lookup"><span data-stu-id="03b5c-129">Required</span></span> | <span data-ttu-id="03b5c-130">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="03b5c-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="03b5c-131">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="03b5c-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="03b5c-132">**高度**</span><span class="sxs-lookup"><span data-stu-id="03b5c-132">**Height**</span></span> | <span data-ttu-id="03b5c-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="03b5c-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="03b5c-134">必要</span><span class="sxs-lookup"><span data-stu-id="03b5c-134">Required</span></span> | <span data-ttu-id="03b5c-135">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="03b5c-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="03b5c-136">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="03b5c-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="03b5c-137">項目資訊</span><span class="sxs-lookup"><span data-stu-id="03b5c-137">Element Information</span></span>



|              |                                                       |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="03b5c-138">項目類型</span><span class="sxs-lookup"><span data-stu-id="03b5c-138">Element type</span></span> | <span data-ttu-id="03b5c-139">[**FlagType**](flagtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="03b5c-139">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="03b5c-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="03b5c-140">Namespace</span></span>    | <span data-ttu-id="03b5c-141">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="03b5c-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="03b5c-142">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="03b5c-142">Schema name</span></span>  | <span data-ttu-id="03b5c-143">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="03b5c-143">Journal Reader</span></span>                                        |



 

 

 



