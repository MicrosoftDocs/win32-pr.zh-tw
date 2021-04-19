---
description: 包含段落。
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: 'Uments 的段落元素 (Windows.ui.xaml.doc.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993951"
---
# <a name="paragraph-element"></a><span data-ttu-id="55ceb-103">段落元素</span><span class="sxs-lookup"><span data-stu-id="55ceb-103">Paragraph Element</span></span>

<span data-ttu-id="55ceb-104">包含段落。</span><span class="sxs-lookup"><span data-stu-id="55ceb-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="55ceb-105">定義</span><span class="sxs-lookup"><span data-stu-id="55ceb-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="55ceb-106">父項目</span><span class="sxs-lookup"><span data-stu-id="55ceb-106">Parent Elements</span></span>

[<span data-ttu-id="55ceb-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="55ceb-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="55ceb-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="55ceb-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="55ceb-109">子元素</span><span class="sxs-lookup"><span data-stu-id="55ceb-109">Child Elements</span></span>

[<span data-ttu-id="55ceb-110">**線條**</span><span class="sxs-lookup"><span data-stu-id="55ceb-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="55ceb-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="55ceb-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="55ceb-112">屬性</span><span class="sxs-lookup"><span data-stu-id="55ceb-112">Attributes</span></span>



| <span data-ttu-id="55ceb-113">屬性</span><span class="sxs-lookup"><span data-stu-id="55ceb-113">Attribute</span></span>       | <span data-ttu-id="55ceb-114">類型</span><span class="sxs-lookup"><span data-stu-id="55ceb-114">Type</span></span>                      | <span data-ttu-id="55ceb-115">必要</span><span class="sxs-lookup"><span data-stu-id="55ceb-115">Required</span></span> | <span data-ttu-id="55ceb-116">描述</span><span class="sxs-lookup"><span data-stu-id="55ceb-116">Description</span></span>                                                                             | <span data-ttu-id="55ceb-117">可能的值</span><span class="sxs-lookup"><span data-stu-id="55ceb-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="55ceb-118">**離開**</span><span class="sxs-lookup"><span data-stu-id="55ceb-118">**Left**</span></span>        | <span data-ttu-id="55ceb-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="55ceb-119">**xs:integer**</span></span>            | <span data-ttu-id="55ceb-120">必要</span><span class="sxs-lookup"><span data-stu-id="55ceb-120">Required</span></span> | <span data-ttu-id="55ceb-121">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="55ceb-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="55ceb-122">任何整數。</span><span class="sxs-lookup"><span data-stu-id="55ceb-122">Any integer.</span></span>              |
| <span data-ttu-id="55ceb-123">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="55ceb-123">**Top**</span></span>         | <span data-ttu-id="55ceb-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="55ceb-124">**xs:integer**</span></span>            | <span data-ttu-id="55ceb-125">必要</span><span class="sxs-lookup"><span data-stu-id="55ceb-125">Required</span></span> | <span data-ttu-id="55ceb-126">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="55ceb-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="55ceb-127">任何整數。</span><span class="sxs-lookup"><span data-stu-id="55ceb-127">Any integer.</span></span>              |
| <span data-ttu-id="55ceb-128">**寬度**</span><span class="sxs-lookup"><span data-stu-id="55ceb-128">**Width**</span></span>       | <span data-ttu-id="55ceb-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="55ceb-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="55ceb-130">必要</span><span class="sxs-lookup"><span data-stu-id="55ceb-130">Required</span></span> | <span data-ttu-id="55ceb-131">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="55ceb-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="55ceb-132">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="55ceb-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="55ceb-133">**高度**</span><span class="sxs-lookup"><span data-stu-id="55ceb-133">**Height**</span></span>      | <span data-ttu-id="55ceb-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="55ceb-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="55ceb-135">必要</span><span class="sxs-lookup"><span data-stu-id="55ceb-135">Required</span></span> | <span data-ttu-id="55ceb-136">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="55ceb-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="55ceb-137">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="55ceb-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="55ceb-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="55ceb-138">**BlockNumber**</span></span> | <span data-ttu-id="55ceb-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="55ceb-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="55ceb-140">必要</span><span class="sxs-lookup"><span data-stu-id="55ceb-140">Required</span></span> | <span data-ttu-id="55ceb-141">區塊數目。</span><span class="sxs-lookup"><span data-stu-id="55ceb-141">Block number.</span></span>                                                                           | <span data-ttu-id="55ceb-142">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="55ceb-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="55ceb-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="55ceb-143">**LineNumber**</span></span>  | <span data-ttu-id="55ceb-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="55ceb-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="55ceb-145">必要</span><span class="sxs-lookup"><span data-stu-id="55ceb-145">Required</span></span> | <span data-ttu-id="55ceb-146">段落開始的行。</span><span class="sxs-lookup"><span data-stu-id="55ceb-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="55ceb-147">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="55ceb-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="55ceb-148">項目資訊</span><span class="sxs-lookup"><span data-stu-id="55ceb-148">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="55ceb-149">項目類型</span><span class="sxs-lookup"><span data-stu-id="55ceb-149">Element type</span></span> | <span data-ttu-id="55ceb-150">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="55ceb-150">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="55ceb-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="55ceb-151">Namespace</span></span>    | <span data-ttu-id="55ceb-152">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="55ceb-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="55ceb-153">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="55ceb-153">Schema name</span></span>  | <span data-ttu-id="55ceb-154">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="55ceb-154">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="55ceb-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="55ceb-155">Requirements</span></span>



| <span data-ttu-id="55ceb-156">需求</span><span class="sxs-lookup"><span data-stu-id="55ceb-156">Requirement</span></span> | <span data-ttu-id="55ceb-157">值</span><span class="sxs-lookup"><span data-stu-id="55ceb-157">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ceb-158">標頭</span><span class="sxs-lookup"><span data-stu-id="55ceb-158">Header</span></span><br/> | <dl> <span data-ttu-id="55ceb-159"><dt>Windows.ui.xaml.documents。h</dt></span><span class="sxs-lookup"><span data-stu-id="55ceb-159"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




