---
description: 包含便箋標題的位置和周框資訊（如果有的話）。
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: TitleArea 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432190"
---
# <a name="titlearea-element"></a><span data-ttu-id="35778-103">TitleArea 元素</span><span class="sxs-lookup"><span data-stu-id="35778-103">TitleArea Element</span></span>

<span data-ttu-id="35778-104">包含便箋標題的位置和周框資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="35778-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="35778-105">定義</span><span class="sxs-lookup"><span data-stu-id="35778-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="35778-106">父項目</span><span class="sxs-lookup"><span data-stu-id="35778-106">Parent Elements</span></span>

[<span data-ttu-id="35778-107">**標題**</span><span class="sxs-lookup"><span data-stu-id="35778-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="35778-108">子元素</span><span class="sxs-lookup"><span data-stu-id="35778-108">Child Elements</span></span>

<span data-ttu-id="35778-109">無。</span><span class="sxs-lookup"><span data-stu-id="35778-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="35778-110">屬性</span><span class="sxs-lookup"><span data-stu-id="35778-110">Attributes</span></span>



| <span data-ttu-id="35778-111">屬性</span><span class="sxs-lookup"><span data-stu-id="35778-111">Attribute</span></span>  | <span data-ttu-id="35778-112">類型</span><span class="sxs-lookup"><span data-stu-id="35778-112">Type</span></span>                      | <span data-ttu-id="35778-113">必要</span><span class="sxs-lookup"><span data-stu-id="35778-113">Required</span></span> | <span data-ttu-id="35778-114">描述</span><span class="sxs-lookup"><span data-stu-id="35778-114">Description</span></span>                                                                             | <span data-ttu-id="35778-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="35778-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="35778-116">**離開**</span><span class="sxs-lookup"><span data-stu-id="35778-116">**Left**</span></span>   | <span data-ttu-id="35778-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="35778-117">**xs:integer**</span></span>            | <span data-ttu-id="35778-118">必要</span><span class="sxs-lookup"><span data-stu-id="35778-118">Required</span></span> | <span data-ttu-id="35778-119">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="35778-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="35778-120">任何整數。</span><span class="sxs-lookup"><span data-stu-id="35778-120">Any integer.</span></span>              |
| <span data-ttu-id="35778-121">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="35778-121">**Top**</span></span>    | <span data-ttu-id="35778-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="35778-122">**xs:integer**</span></span>            | <span data-ttu-id="35778-123">必要</span><span class="sxs-lookup"><span data-stu-id="35778-123">Required</span></span> | <span data-ttu-id="35778-124">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="35778-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="35778-125">任何整數。</span><span class="sxs-lookup"><span data-stu-id="35778-125">Any integer.</span></span>              |
| <span data-ttu-id="35778-126">**寬度**</span><span class="sxs-lookup"><span data-stu-id="35778-126">**Width**</span></span>  | <span data-ttu-id="35778-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="35778-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="35778-128">必要</span><span class="sxs-lookup"><span data-stu-id="35778-128">Required</span></span> | <span data-ttu-id="35778-129">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="35778-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="35778-130">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="35778-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="35778-131">**高度**</span><span class="sxs-lookup"><span data-stu-id="35778-131">**Height**</span></span> | <span data-ttu-id="35778-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="35778-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="35778-133">必要</span><span class="sxs-lookup"><span data-stu-id="35778-133">Required</span></span> | <span data-ttu-id="35778-134">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="35778-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="35778-135">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="35778-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="35778-136">項目資訊</span><span class="sxs-lookup"><span data-stu-id="35778-136">Element Information</span></span>



|   <span data-ttu-id="35778-137">元素</span><span class="sxs-lookup"><span data-stu-id="35778-137">Element</span></span>    | <span data-ttu-id="35778-138">值</span><span class="sxs-lookup"><span data-stu-id="35778-138">Value</span></span>                                                           |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="35778-139">項目類型</span><span class="sxs-lookup"><span data-stu-id="35778-139">Element type</span></span> | <span data-ttu-id="35778-140">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="35778-140">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="35778-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="35778-141">Namespace</span></span>    | <span data-ttu-id="35778-142">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="35778-142">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="35778-143">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="35778-143">Schema name</span></span>  | <span data-ttu-id="35778-144">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="35778-144">Journal Reader</span></span>                                                  |



 

 

 



