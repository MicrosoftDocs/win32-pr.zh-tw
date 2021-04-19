---
title: 'ID2D1RenderTarget PushLayer 方法 (D2d1 \_ 1 .h) '
description: 將指定的圖層新增至轉譯目標，使其接收所有後續的繪圖作業，直到呼叫 PopLayer 為止。
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- PushLayer 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979604"
---
# <a name="id2d1rendertargetpushlayer-methods"></a><span data-ttu-id="dc23a-104">ID2D1RenderTarget：:P ushLayer 方法</span><span class="sxs-lookup"><span data-stu-id="dc23a-104">ID2D1RenderTarget::PushLayer methods</span></span>

<span data-ttu-id="dc23a-105">將指定的圖層新增至轉譯目標，使其接收所有後續的繪圖作業，直到呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 為止。</span><span class="sxs-lookup"><span data-stu-id="dc23a-105">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span>

### <a name="overload-list"></a><span data-ttu-id="dc23a-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="dc23a-106">Overload list</span></span>



| <span data-ttu-id="dc23a-107">方法</span><span class="sxs-lookup"><span data-stu-id="dc23a-107">Method</span></span>                                                                                                                            | <span data-ttu-id="dc23a-108">描述</span><span class="sxs-lookup"><span data-stu-id="dc23a-108">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc23a-109">[**PushLayer (D2D1 \_ 層 \_ 參數&、ID2D1Layer \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="dc23a-109">[**PushLayer(D2D1\_LAYER\_PARAMETERS&,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span></span>  | <span data-ttu-id="dc23a-110">將指定的圖層新增至轉譯目標，使其接收所有後續的繪圖作業，直到呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 為止。</span><span class="sxs-lookup"><span data-stu-id="dc23a-110">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |
| <span data-ttu-id="dc23a-111">[**PushLayer (D2D1 \_ 層 \_ 參數 \* ，ID2D1Layer \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="dc23a-111">[**PushLayer(D2D1\_LAYER\_PARAMETERS\*,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span></span> | <span data-ttu-id="dc23a-112">將指定的圖層新增至轉譯目標，使其接收所有後續的繪圖作業，直到呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 為止。</span><span class="sxs-lookup"><span data-stu-id="dc23a-112">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="dc23a-113">備註</span><span class="sxs-lookup"><span data-stu-id="dc23a-113">Remarks</span></span>

<span data-ttu-id="dc23a-114">[**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))方法可讓呼叫端開始將轉譯重新導向至圖層。</span><span class="sxs-lookup"><span data-stu-id="dc23a-114">The [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method enables a caller to begin redirecting rendering to a layer.</span></span> <span data-ttu-id="dc23a-115">所有轉譯作業在圖層中都是有效的。</span><span class="sxs-lookup"><span data-stu-id="dc23a-115">All rendering operations are valid in a layer.</span></span> <span data-ttu-id="dc23a-116">圖層的位置會受到轉譯目標上設定的世界轉換影響。</span><span class="sxs-lookup"><span data-stu-id="dc23a-116">The location of the layer is affected by the world transform set on the render target.</span></span>

<span data-ttu-id="dc23a-117">每個 **PushLayer** 都必須有相符的 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="dc23a-117">Each **PushLayer** must have a matching [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) call.</span></span> <span data-ttu-id="dc23a-118">如果有比 **PushLayer** 呼叫更多的 **PopLayer** 呼叫，轉譯目標會置於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="dc23a-118">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="dc23a-119">如果在所有未處理的層上取出之前呼叫 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) ，轉譯目標會進入錯誤狀態，而且會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc23a-119">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned.</span></span> <span data-ttu-id="dc23a-120">您可以呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)來清除錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="dc23a-120">The error state can be cleared by a call to [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

<span data-ttu-id="dc23a-121">特定的 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 資源只能一次作用。</span><span class="sxs-lookup"><span data-stu-id="dc23a-121">A particular [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) resource can be active only at one time.</span></span> <span data-ttu-id="dc23a-122">換句話說，您無法呼叫 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 方法，然後緊接在另一個具有相同圖層資源的 **PushLayer** 方法之後。</span><span class="sxs-lookup"><span data-stu-id="dc23a-122">In other words, you cannot call a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method, and then immediately follow with another **PushLayer** method with the same layer resource.</span></span> <span data-ttu-id="dc23a-123">相反地，您必須使用不同的層級資源來呼叫第二個 **PushLayer** 方法。</span><span class="sxs-lookup"><span data-stu-id="dc23a-123">Instead, you must call the second **PushLayer** method with different layer resources.</span></span>

<span data-ttu-id="dc23a-124">如需範例，請參閱 [如何裁剪具有圖層的區域](how-to-clip-with-layers.md)。</span><span class="sxs-lookup"><span data-stu-id="dc23a-124">For an example, see [How to Clip a Region with Layers](how-to-clip-with-layers.md).</span></span>

<span data-ttu-id="dc23a-125">如果失敗，這個方法不會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc23a-125">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="dc23a-126">若要判斷繪圖作業 (如 **PushLayer**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。</span><span class="sxs-lookup"><span data-stu-id="dc23a-126">To determine whether a drawing operation (such as **PushLayer**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="dc23a-127">範例</span><span class="sxs-lookup"><span data-stu-id="dc23a-127">Examples</span></span>

<span data-ttu-id="dc23a-128">下列範例會使用圖層，將點陣圖裁剪成幾何遮罩。</span><span class="sxs-lookup"><span data-stu-id="dc23a-128">The following example uses a layer to clip a bitmap to a geometric mask.</span></span> <span data-ttu-id="dc23a-129">如需完整的範例，請參閱 [如何裁剪成幾何遮罩](how-to-clip-with-layers.md)。</span><span class="sxs-lookup"><span data-stu-id="dc23a-129">For the complete example, see [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="dc23a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc23a-130">Requirements</span></span>



| <span data-ttu-id="dc23a-131">需求</span><span class="sxs-lookup"><span data-stu-id="dc23a-131">Requirement</span></span> | <span data-ttu-id="dc23a-132">值</span><span class="sxs-lookup"><span data-stu-id="dc23a-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc23a-133">標頭</span><span class="sxs-lookup"><span data-stu-id="dc23a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="dc23a-134"><dt>D2d1 \_ 1. h (包括 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="dc23a-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="dc23a-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="dc23a-135">Library</span></span><br/> | <dl> <span data-ttu-id="dc23a-136"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc23a-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="dc23a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dc23a-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="dc23a-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc23a-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="dc23a-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc23a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc23a-140">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="dc23a-140">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="dc23a-141">圖層總覽</span><span class="sxs-lookup"><span data-stu-id="dc23a-141">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

<span data-ttu-id="dc23a-142">�</span><span class="sxs-lookup"><span data-stu-id="dc23a-142">�</span></span>

<span data-ttu-id="dc23a-143">�</span><span class="sxs-lookup"><span data-stu-id="dc23a-143">�</span></span>
