---
description: 繪圖或 InkWord 所使用的純量轉換。
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: ScalarTransform 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5853c0fab76cd5a4857ae0235127a2fe103872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985056"
---
# <a name="scalartransform-element"></a><span data-ttu-id="f7ce6-103">ScalarTransform 元素</span><span class="sxs-lookup"><span data-stu-id="f7ce6-103">ScalarTransform Element</span></span>

<span data-ttu-id="f7ce6-104">[**繪圖**](drawing-element.md)或 [**InkWord**](inkword-element.md)所使用的純量轉換。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="f7ce6-105">定義</span><span class="sxs-lookup"><span data-stu-id="f7ce6-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="f7ce6-106">父項目</span><span class="sxs-lookup"><span data-stu-id="f7ce6-106">Parent Elements</span></span>

[<span data-ttu-id="f7ce6-107">**繪圖**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="f7ce6-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="f7ce6-109">子元素</span><span class="sxs-lookup"><span data-stu-id="f7ce6-109">Child Elements</span></span>

<span data-ttu-id="f7ce6-110">無。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="f7ce6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f7ce6-111">Attributes</span></span>



| <span data-ttu-id="f7ce6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f7ce6-112">Attribute</span></span> | <span data-ttu-id="f7ce6-113">類型</span><span class="sxs-lookup"><span data-stu-id="f7ce6-113">Type</span></span>           | <span data-ttu-id="f7ce6-114">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-114">Required</span></span> | <span data-ttu-id="f7ce6-115">描述</span><span class="sxs-lookup"><span data-stu-id="f7ce6-115">Description</span></span> | <span data-ttu-id="f7ce6-116">可能的值</span><span class="sxs-lookup"><span data-stu-id="f7ce6-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="f7ce6-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-117">**Mat1**</span></span>  | <span data-ttu-id="f7ce6-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-118">**xs:decimal**</span></span> | <span data-ttu-id="f7ce6-119">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-119">Required</span></span> |             | <span data-ttu-id="f7ce6-120">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-120">Any decimal number.</span></span> |
| <span data-ttu-id="f7ce6-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-121">**Mat2**</span></span>  | <span data-ttu-id="f7ce6-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-122">**xs:decimal**</span></span> | <span data-ttu-id="f7ce6-123">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-123">Required</span></span> |             | <span data-ttu-id="f7ce6-124">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-124">Any decimal number.</span></span> |
| <span data-ttu-id="f7ce6-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-125">**Mat3**</span></span>  | <span data-ttu-id="f7ce6-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-126">**xs:decimal**</span></span> | <span data-ttu-id="f7ce6-127">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-127">Required</span></span> |             | <span data-ttu-id="f7ce6-128">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-128">Any decimal number.</span></span> |
| <span data-ttu-id="f7ce6-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-129">**Mat4**</span></span>  | <span data-ttu-id="f7ce6-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-130">**xs:decimal**</span></span> | <span data-ttu-id="f7ce6-131">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-131">Required</span></span> |             | <span data-ttu-id="f7ce6-132">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-132">Any decimal number.</span></span> |
| <span data-ttu-id="f7ce6-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-133">**Mat5**</span></span>  | <span data-ttu-id="f7ce6-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-134">**xs:decimal**</span></span> | <span data-ttu-id="f7ce6-135">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-135">Required</span></span> |             | <span data-ttu-id="f7ce6-136">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-136">Any decimal number.</span></span> |
| <span data-ttu-id="f7ce6-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-137">**Mat6**</span></span>  | <span data-ttu-id="f7ce6-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-138">**xs:decimal**</span></span> | <span data-ttu-id="f7ce6-139">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-139">Required</span></span> |             | <span data-ttu-id="f7ce6-140">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-140">Any decimal number.</span></span> |
| <span data-ttu-id="f7ce6-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-141">**Mat7**</span></span>  | <span data-ttu-id="f7ce6-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-142">**xs:decimal**</span></span> | <span data-ttu-id="f7ce6-143">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-143">Required</span></span> |             | <span data-ttu-id="f7ce6-144">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-144">Any decimal number.</span></span> |
| <span data-ttu-id="f7ce6-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-145">**Mat8**</span></span>  | <span data-ttu-id="f7ce6-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-146">**xs:decimal**</span></span> | <span data-ttu-id="f7ce6-147">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-147">Required</span></span> |             | <span data-ttu-id="f7ce6-148">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-148">Any decimal number.</span></span> |
| <span data-ttu-id="f7ce6-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-149">**Mat9**</span></span>  | <span data-ttu-id="f7ce6-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="f7ce6-150">**xs:decimal**</span></span> | <span data-ttu-id="f7ce6-151">必要</span><span class="sxs-lookup"><span data-stu-id="f7ce6-151">Required</span></span> |             | <span data-ttu-id="f7ce6-152">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="f7ce6-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="f7ce6-153">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f7ce6-153">Element Information</span></span>



|              |                                                                             |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="f7ce6-154">項目類型</span><span class="sxs-lookup"><span data-stu-id="f7ce6-154">Element type</span></span> | <span data-ttu-id="f7ce6-155">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="f7ce6-155">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="f7ce6-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="f7ce6-156">Namespace</span></span>    | <span data-ttu-id="f7ce6-157">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="f7ce6-157">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="f7ce6-158">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="f7ce6-158">Schema name</span></span>  | <span data-ttu-id="f7ce6-159">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="f7ce6-159">Journal Reader</span></span>                                                              |



 

 

 



