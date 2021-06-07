---
description: 包含筆記本便箋中的文字資訊。
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432313"
---
# <a name="text-element"></a><span data-ttu-id="77f01-103">Text 元素</span><span class="sxs-lookup"><span data-stu-id="77f01-103">Text Element</span></span>

<span data-ttu-id="77f01-104">包含筆記本便箋中的文字資訊。</span><span class="sxs-lookup"><span data-stu-id="77f01-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="77f01-105">定義</span><span class="sxs-lookup"><span data-stu-id="77f01-105">Definition</span></span>

<span data-ttu-id="77f01-106">搭配 [**內容**](content-element--journal-reader.md)使用時：</span><span class="sxs-lookup"><span data-stu-id="77f01-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="77f01-107">或者，搭配 [**TitleInfo**](titleinfo-element.md) 和 [**GroupNode**](groupnode-element.md)使用時：</span><span class="sxs-lookup"><span data-stu-id="77f01-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="77f01-108">父項目</span><span class="sxs-lookup"><span data-stu-id="77f01-108">Parent Elements</span></span>

[<span data-ttu-id="77f01-109">**內容**</span><span class="sxs-lookup"><span data-stu-id="77f01-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="77f01-110">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="77f01-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="77f01-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="77f01-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="77f01-112">子元素</span><span class="sxs-lookup"><span data-stu-id="77f01-112">Child Elements</span></span>

<span data-ttu-id="77f01-113">無。</span><span class="sxs-lookup"><span data-stu-id="77f01-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="77f01-114">屬性</span><span class="sxs-lookup"><span data-stu-id="77f01-114">Attributes</span></span>

<span data-ttu-id="77f01-115">搭配 [**TitleInfo**](titleinfo-element.md) 和 [**GroupNode**](groupnode-element.md)使用時，沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="77f01-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="77f01-116">搭配 [**內容**](content-element--journal-reader.md)使用時，屬性如下所示。</span><span class="sxs-lookup"><span data-stu-id="77f01-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="77f01-117">屬性</span><span class="sxs-lookup"><span data-stu-id="77f01-117">Attribute</span></span>  | <span data-ttu-id="77f01-118">類型</span><span class="sxs-lookup"><span data-stu-id="77f01-118">Type</span></span>                      | <span data-ttu-id="77f01-119">必要</span><span class="sxs-lookup"><span data-stu-id="77f01-119">Required</span></span> | <span data-ttu-id="77f01-120">描述</span><span class="sxs-lookup"><span data-stu-id="77f01-120">Description</span></span>                                                                             | <span data-ttu-id="77f01-121">可能的值</span><span class="sxs-lookup"><span data-stu-id="77f01-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="77f01-122">**離開**</span><span class="sxs-lookup"><span data-stu-id="77f01-122">**Left**</span></span>   | <span data-ttu-id="77f01-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="77f01-123">**xs:integer**</span></span>            | <span data-ttu-id="77f01-124">必要</span><span class="sxs-lookup"><span data-stu-id="77f01-124">Required</span></span> | <span data-ttu-id="77f01-125">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="77f01-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="77f01-126">任何整數。</span><span class="sxs-lookup"><span data-stu-id="77f01-126">Any integer.</span></span>              |
| <span data-ttu-id="77f01-127">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="77f01-127">**Top**</span></span>    | <span data-ttu-id="77f01-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="77f01-128">**xs:integer**</span></span>            | <span data-ttu-id="77f01-129">必要</span><span class="sxs-lookup"><span data-stu-id="77f01-129">Required</span></span> | <span data-ttu-id="77f01-130">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="77f01-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="77f01-131">任何整數。</span><span class="sxs-lookup"><span data-stu-id="77f01-131">Any integer.</span></span>              |
| <span data-ttu-id="77f01-132">**寬度**</span><span class="sxs-lookup"><span data-stu-id="77f01-132">**Width**</span></span>  | <span data-ttu-id="77f01-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="77f01-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="77f01-134">必要</span><span class="sxs-lookup"><span data-stu-id="77f01-134">Required</span></span> | <span data-ttu-id="77f01-135">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="77f01-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="77f01-136">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="77f01-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="77f01-137">**高度**</span><span class="sxs-lookup"><span data-stu-id="77f01-137">**Height**</span></span> | <span data-ttu-id="77f01-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="77f01-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="77f01-139">必要</span><span class="sxs-lookup"><span data-stu-id="77f01-139">Required</span></span> | <span data-ttu-id="77f01-140">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="77f01-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="77f01-141">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="77f01-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="77f01-142">項目資訊</span><span class="sxs-lookup"><span data-stu-id="77f01-142">Element Information</span></span>



|   <span data-ttu-id="77f01-143">元素</span><span class="sxs-lookup"><span data-stu-id="77f01-143">Element</span></span>           |   <span data-ttu-id="77f01-144">值</span><span class="sxs-lookup"><span data-stu-id="77f01-144">Value</span></span>                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f01-145">項目類型</span><span class="sxs-lookup"><span data-stu-id="77f01-145">Element type</span></span> | <span data-ttu-id="77f01-146">使用 [**GroupNode**](groupnode-element.md)和 [**TitleInfo**](titleinfo-element.md)元素的 Content 元素) 或 **xs： string** ([**TextType**](texttype-complex-type.md) complexType () </span><span class="sxs-lookup"><span data-stu-id="77f01-146">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="77f01-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="77f01-147">Namespace</span></span>    | <span data-ttu-id="77f01-148">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="77f01-148">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="77f01-149">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="77f01-149">Schema name</span></span>  | <span data-ttu-id="77f01-150">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="77f01-150">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




