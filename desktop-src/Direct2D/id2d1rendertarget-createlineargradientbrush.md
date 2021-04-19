---
title: 'ID2D1RenderTarget CreateLinearGradientBrush 方法 (D2d1 .h) '
description: 建立 ID2D1LinearGradientBrush 物件，以使用線性漸層繪製區域。
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- CreateLinearGradientBrush 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998747"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a><span data-ttu-id="cbf55-104">ID2D1RenderTarget：： CreateLinearGradientBrush 方法</span><span class="sxs-lookup"><span data-stu-id="cbf55-104">ID2D1RenderTarget::CreateLinearGradientBrush methods</span></span>

<span data-ttu-id="cbf55-105">建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 物件，以使用線性漸層繪製區域。</span><span class="sxs-lookup"><span data-stu-id="cbf55-105">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) object for painting areas with a linear gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="cbf55-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="cbf55-106">Overload list</span></span>



| <span data-ttu-id="cbf55-107">方法</span><span class="sxs-lookup"><span data-stu-id="cbf55-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="cbf55-108">描述</span><span class="sxs-lookup"><span data-stu-id="cbf55-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf55-109">[**CreateLinearGradientBrush (D2D1 \_ 線性漸層 \_ \_ 筆刷 \_ 屬性&、ID2D1GradientStopCollection \* 、ID2D1LinearGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="cbf55-109">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>                            | <span data-ttu-id="cbf55-110">建立包含指定的漸層停駐點、沒有任何轉換，而且基底不透明度為1.0 的 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 。</span><span class="sxs-lookup"><span data-stu-id="cbf55-110">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="cbf55-111">[**CreateLinearGradientBrush (D2D1 \_ 線性漸層 \_ \_ 筆刷 \_ 屬性&、D2D1 \_ 筆刷 \_ 屬性&、ID2D1GradientStopCollection \* 、ID2D1LinearGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="cbf55-111">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>   | <span data-ttu-id="cbf55-112">建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) ，其中包含指定的漸層停駐點，並具有指定的轉換和基底不透明度。</span><span class="sxs-lookup"><span data-stu-id="cbf55-112">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="cbf55-113">[**CreateLinearGradientBrush (D2D1 \_ 線性漸層 \_ \_ 筆刷 \_ 屬性 \* 、D2D1 \_ 筆刷 \_ 屬性 \* 、ID2D1GradientStopCollection \* 、ID2D1LinearGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="cbf55-113">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span> | <span data-ttu-id="cbf55-114">建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) ，其中包含指定的漸層停駐點，並具有指定的轉換和基底不透明度。</span><span class="sxs-lookup"><span data-stu-id="cbf55-114">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="cbf55-115">範例</span><span class="sxs-lookup"><span data-stu-id="cbf55-115">Examples</span></span>

<span data-ttu-id="cbf55-116">如需示範如何建立梯度停駐點，並使用它來定義線性漸層的範例，請參閱 [如何建立線性漸層筆刷](how-to-create-a-linear-gradient-brush.md)。</span><span class="sxs-lookup"><span data-stu-id="cbf55-116">For an example showing how to create a gradient stop collection and use it to define a linear gradient, see [How to Create a Linear Gradient Brush](how-to-create-a-linear-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf55-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbf55-117">Requirements</span></span>



| <span data-ttu-id="cbf55-118">需求</span><span class="sxs-lookup"><span data-stu-id="cbf55-118">Requirement</span></span> | <span data-ttu-id="cbf55-119">值</span><span class="sxs-lookup"><span data-stu-id="cbf55-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf55-120">標頭</span><span class="sxs-lookup"><span data-stu-id="cbf55-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cbf55-121"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="cbf55-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="cbf55-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="cbf55-122">Library</span></span><br/> | <dl> <span data-ttu-id="cbf55-123"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbf55-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="cbf55-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cbf55-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="cbf55-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbf55-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf55-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbf55-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf55-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="cbf55-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="cbf55-128">**CreateGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="cbf55-128">**CreateGradientStopCollection**</span></span>](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[<span data-ttu-id="cbf55-129">**ID2D1GradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="cbf55-129">**ID2D1GradientStopCollection**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[<span data-ttu-id="cbf55-130">**ID2D1LinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="cbf55-130">**ID2D1LinearGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[<span data-ttu-id="cbf55-131">**ID2D1RadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="cbf55-131">**ID2D1RadialGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[<span data-ttu-id="cbf55-132">如何建立線性漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="cbf55-132">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="cbf55-133">筆刷概觀</span><span class="sxs-lookup"><span data-stu-id="cbf55-133">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="cbf55-134">�</span><span class="sxs-lookup"><span data-stu-id="cbf55-134">�</span></span>

<span data-ttu-id="cbf55-135">�</span><span class="sxs-lookup"><span data-stu-id="cbf55-135">�</span></span>
