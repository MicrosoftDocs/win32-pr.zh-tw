---
description: 繪圖或 InkWord 所使用的純量轉換。
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: ScalarTransform 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ed5f7d3b44456522b45c7243b15390b7c52433
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432430"
---
# <a name="scalartransform-element"></a><span data-ttu-id="95fde-103">ScalarTransform 元素</span><span class="sxs-lookup"><span data-stu-id="95fde-103">ScalarTransform Element</span></span>

<span data-ttu-id="95fde-104">[**繪圖**](drawing-element.md)或 [**InkWord**](inkword-element.md)所使用的純量轉換。</span><span class="sxs-lookup"><span data-stu-id="95fde-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="95fde-105">定義</span><span class="sxs-lookup"><span data-stu-id="95fde-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="95fde-106">父項目</span><span class="sxs-lookup"><span data-stu-id="95fde-106">Parent Elements</span></span>

[<span data-ttu-id="95fde-107">**繪圖**</span><span class="sxs-lookup"><span data-stu-id="95fde-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="95fde-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="95fde-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="95fde-109">子元素</span><span class="sxs-lookup"><span data-stu-id="95fde-109">Child Elements</span></span>

<span data-ttu-id="95fde-110">無。</span><span class="sxs-lookup"><span data-stu-id="95fde-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="95fde-111">屬性</span><span class="sxs-lookup"><span data-stu-id="95fde-111">Attributes</span></span>



| <span data-ttu-id="95fde-112">屬性</span><span class="sxs-lookup"><span data-stu-id="95fde-112">Attribute</span></span> | <span data-ttu-id="95fde-113">類型</span><span class="sxs-lookup"><span data-stu-id="95fde-113">Type</span></span>           | <span data-ttu-id="95fde-114">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-114">Required</span></span> | <span data-ttu-id="95fde-115">描述</span><span class="sxs-lookup"><span data-stu-id="95fde-115">Description</span></span> | <span data-ttu-id="95fde-116">可能的值</span><span class="sxs-lookup"><span data-stu-id="95fde-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="95fde-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="95fde-117">**Mat1**</span></span>  | <span data-ttu-id="95fde-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="95fde-118">**xs:decimal**</span></span> | <span data-ttu-id="95fde-119">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-119">Required</span></span> |             | <span data-ttu-id="95fde-120">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="95fde-120">Any decimal number.</span></span> |
| <span data-ttu-id="95fde-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="95fde-121">**Mat2**</span></span>  | <span data-ttu-id="95fde-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="95fde-122">**xs:decimal**</span></span> | <span data-ttu-id="95fde-123">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-123">Required</span></span> |             | <span data-ttu-id="95fde-124">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="95fde-124">Any decimal number.</span></span> |
| <span data-ttu-id="95fde-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="95fde-125">**Mat3**</span></span>  | <span data-ttu-id="95fde-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="95fde-126">**xs:decimal**</span></span> | <span data-ttu-id="95fde-127">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-127">Required</span></span> |             | <span data-ttu-id="95fde-128">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="95fde-128">Any decimal number.</span></span> |
| <span data-ttu-id="95fde-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="95fde-129">**Mat4**</span></span>  | <span data-ttu-id="95fde-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="95fde-130">**xs:decimal**</span></span> | <span data-ttu-id="95fde-131">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-131">Required</span></span> |             | <span data-ttu-id="95fde-132">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="95fde-132">Any decimal number.</span></span> |
| <span data-ttu-id="95fde-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="95fde-133">**Mat5**</span></span>  | <span data-ttu-id="95fde-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="95fde-134">**xs:decimal**</span></span> | <span data-ttu-id="95fde-135">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-135">Required</span></span> |             | <span data-ttu-id="95fde-136">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="95fde-136">Any decimal number.</span></span> |
| <span data-ttu-id="95fde-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="95fde-137">**Mat6**</span></span>  | <span data-ttu-id="95fde-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="95fde-138">**xs:decimal**</span></span> | <span data-ttu-id="95fde-139">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-139">Required</span></span> |             | <span data-ttu-id="95fde-140">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="95fde-140">Any decimal number.</span></span> |
| <span data-ttu-id="95fde-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="95fde-141">**Mat7**</span></span>  | <span data-ttu-id="95fde-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="95fde-142">**xs:decimal**</span></span> | <span data-ttu-id="95fde-143">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-143">Required</span></span> |             | <span data-ttu-id="95fde-144">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="95fde-144">Any decimal number.</span></span> |
| <span data-ttu-id="95fde-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="95fde-145">**Mat8**</span></span>  | <span data-ttu-id="95fde-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="95fde-146">**xs:decimal**</span></span> | <span data-ttu-id="95fde-147">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-147">Required</span></span> |             | <span data-ttu-id="95fde-148">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="95fde-148">Any decimal number.</span></span> |
| <span data-ttu-id="95fde-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="95fde-149">**Mat9**</span></span>  | <span data-ttu-id="95fde-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="95fde-150">**xs:decimal**</span></span> | <span data-ttu-id="95fde-151">必要</span><span class="sxs-lookup"><span data-stu-id="95fde-151">Required</span></span> |             | <span data-ttu-id="95fde-152">任何十進位數。</span><span class="sxs-lookup"><span data-stu-id="95fde-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="95fde-153">項目資訊</span><span class="sxs-lookup"><span data-stu-id="95fde-153">Element Information</span></span>



| <span data-ttu-id="95fde-154">元素</span><span class="sxs-lookup"><span data-stu-id="95fde-154">Element</span></span>      | <span data-ttu-id="95fde-155">值</span><span class="sxs-lookup"><span data-stu-id="95fde-155">Value</span></span>                                                                       |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="95fde-156">項目類型</span><span class="sxs-lookup"><span data-stu-id="95fde-156">Element type</span></span> | <span data-ttu-id="95fde-157">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="95fde-157">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="95fde-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="95fde-158">Namespace</span></span>    | <span data-ttu-id="95fde-159">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="95fde-159">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="95fde-160">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="95fde-160">Schema name</span></span>  | <span data-ttu-id="95fde-161">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="95fde-161">Journal Reader</span></span>                                                              |



 

 

 



