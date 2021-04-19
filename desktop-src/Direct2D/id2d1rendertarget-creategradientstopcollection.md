---
title: 'ID2D1RenderTarget CreateGradientStopCollection 方法 (D2d1 \_ 1 .h) '
description: 從 D2D1 梯度停用結構的指定陣列建立 ID2D1GradientStopCollection \_ \_ 。
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- CreateGradientStopCollection 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e149727650223f40a290d1ada40abc69f9033440
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380632"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a><span data-ttu-id="e676d-104">ID2D1RenderTarget：： CreateGradientStopCollection 方法</span><span class="sxs-lookup"><span data-stu-id="e676d-104">ID2D1RenderTarget::CreateGradientStopCollection methods</span></span>

<span data-ttu-id="e676d-105">從 [**D2D1 \_ 梯度 \_ 停**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)用結構的指定陣列建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 。</span><span class="sxs-lookup"><span data-stu-id="e676d-105">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures.</span></span>

### <a name="overload-list"></a><span data-ttu-id="e676d-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="e676d-106">Overload list</span></span>



| <span data-ttu-id="e676d-107">方法</span><span class="sxs-lookup"><span data-stu-id="e676d-107">Method</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="e676d-108">描述</span><span class="sxs-lookup"><span data-stu-id="e676d-108">Description</span></span>                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e676d-109">[**CreateGradientStopCollection (D2D1 \_ 梯度 \_ 停駐 \* 、D2D1 \_ GAMMA、D2D1 \_ 擴充 \_ 模式、ID2D1GradientStopCollection \* \*)**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e676d-109">[**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,D2D1\_GAMMA,D2D1\_EXTEND\_MODE,ID2D1GradientStopCollection\*\*)**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span></span> | <span data-ttu-id="e676d-110">從指定的漸層停駐點、色彩插補 gamma 和延伸模式建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 。</span><span class="sxs-lookup"><span data-stu-id="e676d-110">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops, color interpolation gamma, and extend mode.</span></span> <br/>                                                              |
| <span data-ttu-id="e676d-111">[**CreateGradientStopCollection (D2D1 \_ 梯度 \_ 停駐 \* 、ID2D1GradientStopCollection \* \*)**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e676d-111">[**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,ID2D1GradientStopCollection\*\*)**](https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)</span></span>                                                            | <span data-ttu-id="e676d-112">從指定的漸層停用 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) ，使用 [**D2D1 \_ GAMMA \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) 色彩插補 GAMMA 和 [夾具延伸模式] 來建立。</span><span class="sxs-lookup"><span data-stu-id="e676d-112">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops that uses the [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) color interpolation gamma and the clamp extend mode.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="e676d-113">範例</span><span class="sxs-lookup"><span data-stu-id="e676d-113">Examples</span></span>

<span data-ttu-id="e676d-114">下列範例會建立梯度停駐點的陣列，然後使用它們來建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)。</span><span class="sxs-lookup"><span data-stu-id="e676d-114">The following example creates an array of gradient stops, then uses them to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



<span data-ttu-id="e676d-115">下一個程式碼範例會使用 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 來建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)。</span><span class="sxs-lookup"><span data-stu-id="e676d-115">The next code example uses the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to create an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a><span data-ttu-id="e676d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e676d-116">Requirements</span></span>



| <span data-ttu-id="e676d-117">需求</span><span class="sxs-lookup"><span data-stu-id="e676d-117">Requirement</span></span> | <span data-ttu-id="e676d-118">值</span><span class="sxs-lookup"><span data-stu-id="e676d-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e676d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e676d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e676d-120"><dt>D2d1 \_ 1. h (包括 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="e676d-120"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="e676d-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e676d-121">Library</span></span><br/> | <dl> <span data-ttu-id="e676d-122"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e676d-122"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e676d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e676d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e676d-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e676d-124"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="e676d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e676d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e676d-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e676d-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="e676d-127">**D2D1 \_ 梯度 \_ 停駐點**</span><span class="sxs-lookup"><span data-stu-id="e676d-127">**D2D1\_GRADIENT\_STOP**</span></span>](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[<span data-ttu-id="e676d-128">如何建立線性漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="e676d-128">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="e676d-129">如何建立放射狀漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="e676d-129">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="e676d-130">筆刷概觀</span><span class="sxs-lookup"><span data-stu-id="e676d-130">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>
