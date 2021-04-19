---
title: 'ID2D1RenderTarget CreateRadialGradientBrush 方法 (D2d1 .h) '
description: 建立 ID2D1RadialGradientBrush 物件，這個物件可以用來繪製具有放射狀漸層的區域。
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- CreateRadialGradientBrush 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 680cc981943e45eb32834e48151f391f6249cc1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981336"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a><span data-ttu-id="4e1bc-104">ID2D1RenderTarget：： CreateRadialGradientBrush 方法</span><span class="sxs-lookup"><span data-stu-id="4e1bc-104">ID2D1RenderTarget::CreateRadialGradientBrush methods</span></span>

<span data-ttu-id="4e1bc-105">建立 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 物件，這個物件可以用來繪製具有放射狀漸層的區域。</span><span class="sxs-lookup"><span data-stu-id="4e1bc-105">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) object that can be used to paint areas with a radial gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4e1bc-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="4e1bc-106">Overload list</span></span>



| <span data-ttu-id="4e1bc-107">方法</span><span class="sxs-lookup"><span data-stu-id="4e1bc-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="4e1bc-108">描述</span><span class="sxs-lookup"><span data-stu-id="4e1bc-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1bc-109">[**CreateRadialGradientBrush (D2D1 \_ 放射漸層 \_ \_ 筆刷 \_ 屬性&、ID2D1GradientStopCollection \* 、ID2D1RadialGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="4e1bc-109">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>                            | <span data-ttu-id="4e1bc-110">建立包含指定的漸層停駐點、沒有任何轉換，而且基底不透明度為1.0 的 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 。</span><span class="sxs-lookup"><span data-stu-id="4e1bc-110">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="4e1bc-111">[**CreateRadialGradientBrush (D2D1 \_ 放射漸層 \_ \_ 筆刷 \_ 屬性&、D2D1 \_ 筆刷 \_ 屬性&、ID2D1GradientStopCollection \* 、ID2D1RadialGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="4e1bc-111">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>   | <span data-ttu-id="4e1bc-112">建立 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) ，其中包含指定的漸層停駐點，並具有指定的轉換和基底不透明度。</span><span class="sxs-lookup"><span data-stu-id="4e1bc-112">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="4e1bc-113">[**CreateRadialGradientBrush (D2D1 \_ 放射漸層 \_ \_ 筆刷 \_ 屬性 \* 、D2D1 \_ 筆刷 \_ 屬性 \* 、ID2D1GradientStopCollection \* 、ID2D1RadialGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="4e1bc-113">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span> | <span data-ttu-id="4e1bc-114">建立 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) ，其中包含指定的漸層停駐點，並具有指定的轉換和基底不透明度。</span><span class="sxs-lookup"><span data-stu-id="4e1bc-114">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="4e1bc-115">範例</span><span class="sxs-lookup"><span data-stu-id="4e1bc-115">Examples</span></span>

<span data-ttu-id="4e1bc-116">如需範例，請參閱 [如何建立放射狀漸層筆刷](how-to-create-a-radial-gradient-brush.md)。</span><span class="sxs-lookup"><span data-stu-id="4e1bc-116">For an example, see [How to Create a Radial Gradient Brush](how-to-create-a-radial-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1bc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e1bc-117">Requirements</span></span>



| <span data-ttu-id="4e1bc-118">需求</span><span class="sxs-lookup"><span data-stu-id="4e1bc-118">Requirement</span></span> | <span data-ttu-id="4e1bc-119">值</span><span class="sxs-lookup"><span data-stu-id="4e1bc-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1bc-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4e1bc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4e1bc-121"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="4e1bc-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e1bc-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e1bc-122">Library</span></span><br/> | <dl> <span data-ttu-id="4e1bc-123"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e1bc-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="4e1bc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4e1bc-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="4e1bc-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e1bc-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e1bc-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e1bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1bc-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="4e1bc-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="4e1bc-128">如何建立放射狀漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="4e1bc-128">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="4e1bc-129">筆刷概觀</span><span class="sxs-lookup"><span data-stu-id="4e1bc-129">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="4e1bc-130">�</span><span class="sxs-lookup"><span data-stu-id="4e1bc-130">�</span></span>

<span data-ttu-id="4e1bc-131">�</span><span class="sxs-lookup"><span data-stu-id="4e1bc-131">�</span></span>
