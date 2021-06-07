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
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432230"
---
# <a name="paragraph-element"></a><span data-ttu-id="35dbd-103">段落元素</span><span class="sxs-lookup"><span data-stu-id="35dbd-103">Paragraph Element</span></span>

<span data-ttu-id="35dbd-104">包含段落。</span><span class="sxs-lookup"><span data-stu-id="35dbd-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="35dbd-105">定義</span><span class="sxs-lookup"><span data-stu-id="35dbd-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="35dbd-106">父項目</span><span class="sxs-lookup"><span data-stu-id="35dbd-106">Parent Elements</span></span>

[<span data-ttu-id="35dbd-107">**內容**</span><span class="sxs-lookup"><span data-stu-id="35dbd-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="35dbd-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="35dbd-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="35dbd-109">子元素</span><span class="sxs-lookup"><span data-stu-id="35dbd-109">Child Elements</span></span>

[<span data-ttu-id="35dbd-110">**折線圖**</span><span class="sxs-lookup"><span data-stu-id="35dbd-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="35dbd-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="35dbd-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="35dbd-112">屬性</span><span class="sxs-lookup"><span data-stu-id="35dbd-112">Attributes</span></span>



| <span data-ttu-id="35dbd-113">屬性</span><span class="sxs-lookup"><span data-stu-id="35dbd-113">Attribute</span></span>       | <span data-ttu-id="35dbd-114">類型</span><span class="sxs-lookup"><span data-stu-id="35dbd-114">Type</span></span>                      | <span data-ttu-id="35dbd-115">必要</span><span class="sxs-lookup"><span data-stu-id="35dbd-115">Required</span></span> | <span data-ttu-id="35dbd-116">描述</span><span class="sxs-lookup"><span data-stu-id="35dbd-116">Description</span></span>                                                                             | <span data-ttu-id="35dbd-117">可能的值</span><span class="sxs-lookup"><span data-stu-id="35dbd-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="35dbd-118">**離開**</span><span class="sxs-lookup"><span data-stu-id="35dbd-118">**Left**</span></span>        | <span data-ttu-id="35dbd-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="35dbd-119">**xs:integer**</span></span>            | <span data-ttu-id="35dbd-120">必要</span><span class="sxs-lookup"><span data-stu-id="35dbd-120">Required</span></span> | <span data-ttu-id="35dbd-121">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="35dbd-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="35dbd-122">任何整數。</span><span class="sxs-lookup"><span data-stu-id="35dbd-122">Any integer.</span></span>              |
| <span data-ttu-id="35dbd-123">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="35dbd-123">**Top**</span></span>         | <span data-ttu-id="35dbd-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="35dbd-124">**xs:integer**</span></span>            | <span data-ttu-id="35dbd-125">必要</span><span class="sxs-lookup"><span data-stu-id="35dbd-125">Required</span></span> | <span data-ttu-id="35dbd-126">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="35dbd-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="35dbd-127">任何整數。</span><span class="sxs-lookup"><span data-stu-id="35dbd-127">Any integer.</span></span>              |
| <span data-ttu-id="35dbd-128">**寬度**</span><span class="sxs-lookup"><span data-stu-id="35dbd-128">**Width**</span></span>       | <span data-ttu-id="35dbd-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="35dbd-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="35dbd-130">必要</span><span class="sxs-lookup"><span data-stu-id="35dbd-130">Required</span></span> | <span data-ttu-id="35dbd-131">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="35dbd-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="35dbd-132">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="35dbd-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="35dbd-133">**高度**</span><span class="sxs-lookup"><span data-stu-id="35dbd-133">**Height**</span></span>      | <span data-ttu-id="35dbd-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="35dbd-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="35dbd-135">必要</span><span class="sxs-lookup"><span data-stu-id="35dbd-135">Required</span></span> | <span data-ttu-id="35dbd-136">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="35dbd-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="35dbd-137">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="35dbd-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="35dbd-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="35dbd-138">**BlockNumber**</span></span> | <span data-ttu-id="35dbd-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="35dbd-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="35dbd-140">必要</span><span class="sxs-lookup"><span data-stu-id="35dbd-140">Required</span></span> | <span data-ttu-id="35dbd-141">區塊數目。</span><span class="sxs-lookup"><span data-stu-id="35dbd-141">Block number.</span></span>                                                                           | <span data-ttu-id="35dbd-142">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="35dbd-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="35dbd-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="35dbd-143">**LineNumber**</span></span>  | <span data-ttu-id="35dbd-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="35dbd-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="35dbd-145">必要</span><span class="sxs-lookup"><span data-stu-id="35dbd-145">Required</span></span> | <span data-ttu-id="35dbd-146">段落開始的行。</span><span class="sxs-lookup"><span data-stu-id="35dbd-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="35dbd-147">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="35dbd-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="35dbd-148">項目資訊</span><span class="sxs-lookup"><span data-stu-id="35dbd-148">Element Information</span></span>



|  <span data-ttu-id="35dbd-149">元素</span><span class="sxs-lookup"><span data-stu-id="35dbd-149">Element</span></span>     | <span data-ttu-id="35dbd-150">值</span><span class="sxs-lookup"><span data-stu-id="35dbd-150">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="35dbd-151">項目類型</span><span class="sxs-lookup"><span data-stu-id="35dbd-151">Element type</span></span> | <span data-ttu-id="35dbd-152">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="35dbd-152">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="35dbd-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="35dbd-153">Namespace</span></span>    | <span data-ttu-id="35dbd-154">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="35dbd-154">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="35dbd-155">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="35dbd-155">Schema name</span></span>  | <span data-ttu-id="35dbd-156">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="35dbd-156">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="35dbd-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="35dbd-157">Requirements</span></span>



| <span data-ttu-id="35dbd-158">需求</span><span class="sxs-lookup"><span data-stu-id="35dbd-158">Requirement</span></span> | <span data-ttu-id="35dbd-159">值</span><span class="sxs-lookup"><span data-stu-id="35dbd-159">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dbd-160">標頭</span><span class="sxs-lookup"><span data-stu-id="35dbd-160">Header</span></span><br/> | <dl> <span data-ttu-id="35dbd-161"><dt>Windows.ui.xaml.documents。h</dt></span><span class="sxs-lookup"><span data-stu-id="35dbd-161"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




