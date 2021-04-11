---
description: 包含便箋標題的位置和周框資訊（如果有的話）。
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: TitleArea 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c009d817af9679edda618dd0262c7cbb85a612ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945259"
---
# <a name="titlearea-element"></a><span data-ttu-id="a1d9d-103">TitleArea 元素</span><span class="sxs-lookup"><span data-stu-id="a1d9d-103">TitleArea Element</span></span>

<span data-ttu-id="a1d9d-104">包含便箋標題的位置和周框資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="a1d9d-105">定義</span><span class="sxs-lookup"><span data-stu-id="a1d9d-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="a1d9d-106">父項目</span><span class="sxs-lookup"><span data-stu-id="a1d9d-106">Parent Elements</span></span>

[<span data-ttu-id="a1d9d-107">**標題**</span><span class="sxs-lookup"><span data-stu-id="a1d9d-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="a1d9d-108">子元素</span><span class="sxs-lookup"><span data-stu-id="a1d9d-108">Child Elements</span></span>

<span data-ttu-id="a1d9d-109">無。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="a1d9d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a1d9d-110">Attributes</span></span>



| <span data-ttu-id="a1d9d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a1d9d-111">Attribute</span></span>  | <span data-ttu-id="a1d9d-112">類型</span><span class="sxs-lookup"><span data-stu-id="a1d9d-112">Type</span></span>                      | <span data-ttu-id="a1d9d-113">必要</span><span class="sxs-lookup"><span data-stu-id="a1d9d-113">Required</span></span> | <span data-ttu-id="a1d9d-114">描述</span><span class="sxs-lookup"><span data-stu-id="a1d9d-114">Description</span></span>                                                                             | <span data-ttu-id="a1d9d-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="a1d9d-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="a1d9d-116">**離開**</span><span class="sxs-lookup"><span data-stu-id="a1d9d-116">**Left**</span></span>   | <span data-ttu-id="a1d9d-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a1d9d-117">**xs:integer**</span></span>            | <span data-ttu-id="a1d9d-118">必要</span><span class="sxs-lookup"><span data-stu-id="a1d9d-118">Required</span></span> | <span data-ttu-id="a1d9d-119">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="a1d9d-120">任何整數。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-120">Any integer.</span></span>              |
| <span data-ttu-id="a1d9d-121">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="a1d9d-121">**Top**</span></span>    | <span data-ttu-id="a1d9d-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a1d9d-122">**xs:integer**</span></span>            | <span data-ttu-id="a1d9d-123">必要</span><span class="sxs-lookup"><span data-stu-id="a1d9d-123">Required</span></span> | <span data-ttu-id="a1d9d-124">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="a1d9d-125">任何整數。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-125">Any integer.</span></span>              |
| <span data-ttu-id="a1d9d-126">**寬度**</span><span class="sxs-lookup"><span data-stu-id="a1d9d-126">**Width**</span></span>  | <span data-ttu-id="a1d9d-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a1d9d-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a1d9d-128">必要</span><span class="sxs-lookup"><span data-stu-id="a1d9d-128">Required</span></span> | <span data-ttu-id="a1d9d-129">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="a1d9d-130">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="a1d9d-131">**高度**</span><span class="sxs-lookup"><span data-stu-id="a1d9d-131">**Height**</span></span> | <span data-ttu-id="a1d9d-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a1d9d-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a1d9d-133">必要</span><span class="sxs-lookup"><span data-stu-id="a1d9d-133">Required</span></span> | <span data-ttu-id="a1d9d-134">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="a1d9d-135">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="a1d9d-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="a1d9d-136">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a1d9d-136">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="a1d9d-137">項目類型</span><span class="sxs-lookup"><span data-stu-id="a1d9d-137">Element type</span></span> | <span data-ttu-id="a1d9d-138">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="a1d9d-138">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a1d9d-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1d9d-139">Namespace</span></span>    | <span data-ttu-id="a1d9d-140">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="a1d9d-140">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="a1d9d-141">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="a1d9d-141">Schema name</span></span>  | <span data-ttu-id="a1d9d-142">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="a1d9d-142">Journal Reader</span></span>                                                  |



 

 

 



