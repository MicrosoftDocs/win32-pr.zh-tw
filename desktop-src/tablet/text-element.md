---
description: 包含筆記本便箋中的文字資訊。
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945160"
---
# <a name="text-element"></a><span data-ttu-id="db53b-103">Text 元素</span><span class="sxs-lookup"><span data-stu-id="db53b-103">Text Element</span></span>

<span data-ttu-id="db53b-104">包含筆記本便箋中的文字資訊。</span><span class="sxs-lookup"><span data-stu-id="db53b-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="db53b-105">定義</span><span class="sxs-lookup"><span data-stu-id="db53b-105">Definition</span></span>

<span data-ttu-id="db53b-106">搭配 [**內容**](content-element--journal-reader.md)使用時：</span><span class="sxs-lookup"><span data-stu-id="db53b-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="db53b-107">或者，搭配 [**TitleInfo**](titleinfo-element.md) 和 [**GroupNode**](groupnode-element.md)使用時：</span><span class="sxs-lookup"><span data-stu-id="db53b-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="db53b-108">父項目</span><span class="sxs-lookup"><span data-stu-id="db53b-108">Parent Elements</span></span>

[<span data-ttu-id="db53b-109">**內容**</span><span class="sxs-lookup"><span data-stu-id="db53b-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="db53b-110">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="db53b-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="db53b-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="db53b-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="db53b-112">子元素</span><span class="sxs-lookup"><span data-stu-id="db53b-112">Child Elements</span></span>

<span data-ttu-id="db53b-113">無。</span><span class="sxs-lookup"><span data-stu-id="db53b-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="db53b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="db53b-114">Attributes</span></span>

<span data-ttu-id="db53b-115">搭配 [**TitleInfo**](titleinfo-element.md) 和 [**GroupNode**](groupnode-element.md)使用時，沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="db53b-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="db53b-116">搭配 [**內容**](content-element--journal-reader.md)使用時，屬性如下所示。</span><span class="sxs-lookup"><span data-stu-id="db53b-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="db53b-117">屬性</span><span class="sxs-lookup"><span data-stu-id="db53b-117">Attribute</span></span>  | <span data-ttu-id="db53b-118">類型</span><span class="sxs-lookup"><span data-stu-id="db53b-118">Type</span></span>                      | <span data-ttu-id="db53b-119">必要</span><span class="sxs-lookup"><span data-stu-id="db53b-119">Required</span></span> | <span data-ttu-id="db53b-120">描述</span><span class="sxs-lookup"><span data-stu-id="db53b-120">Description</span></span>                                                                             | <span data-ttu-id="db53b-121">可能的值</span><span class="sxs-lookup"><span data-stu-id="db53b-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="db53b-122">**離開**</span><span class="sxs-lookup"><span data-stu-id="db53b-122">**Left**</span></span>   | <span data-ttu-id="db53b-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="db53b-123">**xs:integer**</span></span>            | <span data-ttu-id="db53b-124">必要</span><span class="sxs-lookup"><span data-stu-id="db53b-124">Required</span></span> | <span data-ttu-id="db53b-125">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="db53b-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="db53b-126">任何整數。</span><span class="sxs-lookup"><span data-stu-id="db53b-126">Any integer.</span></span>              |
| <span data-ttu-id="db53b-127">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="db53b-127">**Top**</span></span>    | <span data-ttu-id="db53b-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="db53b-128">**xs:integer**</span></span>            | <span data-ttu-id="db53b-129">必要</span><span class="sxs-lookup"><span data-stu-id="db53b-129">Required</span></span> | <span data-ttu-id="db53b-130">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="db53b-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="db53b-131">任何整數。</span><span class="sxs-lookup"><span data-stu-id="db53b-131">Any integer.</span></span>              |
| <span data-ttu-id="db53b-132">**寬度**</span><span class="sxs-lookup"><span data-stu-id="db53b-132">**Width**</span></span>  | <span data-ttu-id="db53b-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="db53b-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="db53b-134">必要</span><span class="sxs-lookup"><span data-stu-id="db53b-134">Required</span></span> | <span data-ttu-id="db53b-135">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="db53b-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="db53b-136">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="db53b-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="db53b-137">**高度**</span><span class="sxs-lookup"><span data-stu-id="db53b-137">**Height**</span></span> | <span data-ttu-id="db53b-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="db53b-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="db53b-139">必要</span><span class="sxs-lookup"><span data-stu-id="db53b-139">Required</span></span> | <span data-ttu-id="db53b-140">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="db53b-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="db53b-141">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="db53b-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="db53b-142">項目資訊</span><span class="sxs-lookup"><span data-stu-id="db53b-142">Element Information</span></span>



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db53b-143">項目類型</span><span class="sxs-lookup"><span data-stu-id="db53b-143">Element type</span></span> | <span data-ttu-id="db53b-144">使用 [**GroupNode**](groupnode-element.md)和 [**TitleInfo**](titleinfo-element.md)元素的 Content 元素) 或 **xs： string** ([**TextType**](texttype-complex-type.md) complexType () </span><span class="sxs-lookup"><span data-stu-id="db53b-144">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="db53b-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="db53b-145">Namespace</span></span>    | <span data-ttu-id="db53b-146">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="db53b-146">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="db53b-147">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="db53b-147">Schema name</span></span>  | <span data-ttu-id="db53b-148">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="db53b-148">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




