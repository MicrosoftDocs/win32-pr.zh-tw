---
title: ID2D1RenderTarget SetTransform 方法
description: 將指定的轉換套用至轉譯目標，並取代現有的轉換。 所有後續繪圖作業都會出現在已轉換的空間中。
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- SetTransform 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999733"
---
# <a name="id2d1rendertargetsettransform-methods"></a><span data-ttu-id="0b65a-105">ID2D1RenderTarget：： SetTransform 方法</span><span class="sxs-lookup"><span data-stu-id="0b65a-105">ID2D1RenderTarget::SetTransform methods</span></span>

<span data-ttu-id="0b65a-106">將指定的轉換套用至轉譯目標，並取代現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="0b65a-106">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="0b65a-107">所有後續繪圖作業都會出現在已轉換的空間中。</span><span class="sxs-lookup"><span data-stu-id="0b65a-107">All subsequent drawing operations occur in the transformed space.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0b65a-108">多載清單</span><span class="sxs-lookup"><span data-stu-id="0b65a-108">Overload list</span></span>



| <span data-ttu-id="0b65a-109">方法</span><span class="sxs-lookup"><span data-stu-id="0b65a-109">Method</span></span>                                                                                              | <span data-ttu-id="0b65a-110">描述</span><span class="sxs-lookup"><span data-stu-id="0b65a-110">Description</span></span>                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b65a-111">[**SetTransform (D2D1 \_ 矩陣 \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="0b65a-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="0b65a-112">將指定的轉換套用至轉譯目標，並取代現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="0b65a-112">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="0b65a-113">所有後續繪圖作業都會出現在已轉換的空間中。</span><span class="sxs-lookup"><span data-stu-id="0b65a-113">All subsequent drawing operations occur in the transformed space.</span></span> <br/> |
| <span data-ttu-id="0b65a-114">[**SetTransform (D2D1 \_ 矩陣 \_ 3X2 \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="0b65a-114">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="0b65a-115">將指定的轉換套用至轉譯目標，並取代現有的轉換。</span><span class="sxs-lookup"><span data-stu-id="0b65a-115">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="0b65a-116">所有後續繪圖作業都會出現在已轉換的空間中。</span><span class="sxs-lookup"><span data-stu-id="0b65a-116">All subsequent drawing operations occur in the transformed space.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="0b65a-117">範例</span><span class="sxs-lookup"><span data-stu-id="0b65a-117">Examples</span></span>

<span data-ttu-id="0b65a-118">下列範例會使用 **SetTransform** 方法，將旋轉套用至呈現目標。</span><span class="sxs-lookup"><span data-stu-id="0b65a-118">The following example uses the **SetTransform** method to apply a rotation to the render target.</span></span> <span data-ttu-id="0b65a-119">如需完整範例，請參閱 [如何旋轉物件](how-to-rotate.md)。</span><span class="sxs-lookup"><span data-stu-id="0b65a-119">For the complete example, see [How to Rotate an Object](how-to-rotate.md).</span></span>


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



<span data-ttu-id="0b65a-120">如需顯示如何轉換轉譯目標的其他範例，請參閱 [如何調整物件](how-to-scale.md)、 [如何扭曲物件](how-to-skew.md)，以及 [如何轉譯物件](how-to-translate.md)。</span><span class="sxs-lookup"><span data-stu-id="0b65a-120">For additional examples showing how to transform a render target, see [How to Scale an Object](how-to-scale.md), [How to Skew an Object](how-to-skew.md), and [How to Translate an Object](how-to-translate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b65a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b65a-121">Requirements</span></span>



| <span data-ttu-id="0b65a-122">需求</span><span class="sxs-lookup"><span data-stu-id="0b65a-122">Requirement</span></span> | <span data-ttu-id="0b65a-123">值</span><span class="sxs-lookup"><span data-stu-id="0b65a-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0b65a-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="0b65a-124">Library</span></span><br/> | <dl> <span data-ttu-id="0b65a-125"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b65a-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="0b65a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0b65a-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b65a-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b65a-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b65a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b65a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b65a-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="0b65a-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="0b65a-130">轉換總覽</span><span class="sxs-lookup"><span data-stu-id="0b65a-130">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="0b65a-131">如何旋轉物件</span><span class="sxs-lookup"><span data-stu-id="0b65a-131">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="0b65a-132">如何調整物件</span><span class="sxs-lookup"><span data-stu-id="0b65a-132">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="0b65a-133">如何扭曲物件</span><span class="sxs-lookup"><span data-stu-id="0b65a-133">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="0b65a-134">如何轉譯物件</span><span class="sxs-lookup"><span data-stu-id="0b65a-134">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="0b65a-135">如何將多個轉換套用至物件</span><span class="sxs-lookup"><span data-stu-id="0b65a-135">How to Apply Multiple Transforms to an Object</span></span>](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

